---
author: alexdong
comments: true
date: 2013-01-22 22:39:58
layout: post
slug: one-fundamental-difference-between-elasticsearch-and-solr
title: One fundamental difference between ElasticSearch and Solr
wordpress_id: 355
categories:
- code
- bestof
---

**important update**: The recent release of Solr 4 has addressed the difference mentioned below. Now Solr handles replication similarly to ElasticSearch. Even better, a transaction log has been added for durabilities. So please be aware that the information below is more a comparison between ElasticSearch and Solr 3.  

Most of the articles comparing ElasticSearch and Solr fall into two groups.

The first group would give some performance test and declare one outperforms the other. Like [this one](http://blog.socialcast.com/realtime-search-solr-vs-elasticsearch/) from socialcast.  If you dig deeper though, you'll realize that it's not a fair comparison. The ElasticSearch's read will waste too much time in routing with the default 5 shards settings;  For Solr, you are not supposed to call IndexWriter#commit for every write request anyway. The author also ignored the fact that Solr 4's soft commit would make search while indexing a lot faster.

The second group provides feature-by-feature comparison like the [Sematext one](http://blog.sematext.com/2012/08/23/solr-vs-elasticsearch-part-1-overview/).  This does provide a more comprehensive view on what's available in each package. Let's be honest, most of the features can be implemented given enough time.  I'm sure ElasticSearch will have a proper SpellChecker soon and it won't take too long for Solr to have a percolate feature implemented.  Unfortunately, this hides the fundamental architectural differences between the two, which is actually crucial for people to decide which one to choose.

Actually, there is only one fundamental difference here but it does have far reaching consequences on how each would perform. **The difference is how the distributed replication works**.

To understand this, you have to look at Lucene's index on disk first. Lucene stores its search index in immutable segments and then **as more documents are indexed, these immutable segments will be merged into new, and more efficient, ones.**  Inevitably, this will incur non-trivial disk read/write. It'll be slow.  Within Lucene, this usually happens when a commit call happens. (To keep things easier, let's ignore the difference between soft and hard commit in Solr 4 for now. )

Both ElasticSearch and Solr use Lucene to store their search index but how the changes replicated to different servers differ.

**Solr** will **copy the new segment file to different servers**. This works great when you don't need to add new documents to your search index too often.  But in the age of an endless stream of contents keep flowing in and the needs for near real time search, this decision is seriously holding us back.

You see, there is an **inherent conflict on how often to call commit** here.  If you want your new content to show up in other search shards, you want to call commit as often as possible so that new segments can be created and copied over. However, if you want to index fast, you want to avoid, or at least delay, commit at all cost so that you can keep indexing stuff without cleaning up the disks.

**ElasticSearch solved this problem by sending the same document to be indexed by all the search shards.**  To be more precise, all the replica shards. This way, you will never need to call commit to get your index shipped to other server. You can index as many as you like and still have all information available to all replica shards.

One important result of this approach is that ElasticSearch offers a much **robust single server deployment by having a write ahead log**. Even if you kill it brutally, you know the dash 9 thing, a single node ElasticSearch would still be able to recover, replay and keep going. Try that with Solr and you'll have to manually fix the corrupted index.

Another important consequence  is that it's relatively easy to have a **High Availability built-in.  **If the primary shard goes down, one of the replicas can take over and elect itself to be the primary without causing too much troubles because all replica shards have already had the same content.

There is one minor downside to this approach though. If your application has a high rate of modification to the same document, then that change might arrive at the replica out of sequence. This can be addressed by using versioning but I really doubt a search engine will have such a high modification rate.

I hope this clarifies things a bit. I also hope that now if you look at the feature-by-feature comparison, you would appreciate the differences better by understanding what's the rational behind them.
