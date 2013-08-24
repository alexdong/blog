---
author: alexdong
comments: true
date: 2012-09-04 22:30:20
layout: post
slug: what-wrong-with-university-database-prepare-for-future
title: What’s wrong with universities database class and how to prepare for the future?
wordpress_id: 113
categories:
- code
- bestof
---

Every computer science or engineering graduate has learned the basics of relational database. This will certainly include some "advanced" skills like JOIN, or COUNT with GROUP BY, or sub-queries and probably certainly TRANSACTIONS. Students believe that they need to use these features in their real work.

How wrong!

Amazon's e-commerce site uses [key-value, consistent hashing](http://the-paper-trail.org/blog/consistency-and-availability-in-amazons-dynamo/) and "always-write-succeed", instead of transactions, as described in [this ground-breaking paper](http://www.allthingsdistributed.com/2007/10/amazons_dynamo.html).  Reddit, one of the world's most popular site uses[ only two tables](http://kev.inburke.com/kevin/reddits-database-has-two-tables/):


> they keep a Thing Table and a Data Table. Everything in Reddit is a Thing: users, links, comments, subreddits, awards, etc. Things keep common attribute like up/down votes, a type, and creation date. The Data table has three columns: thing id, key, value. There’s a row for every attribute. There’s a row for title, url, author, spam votes, etc. When they add new features they didn’t have to worry about the database anymore. They didn’t have to add new tables for new things or worry about upgrades. Easier for development, deployment, maintenance.

The price is you can’t use cool relational features. There are no joins in the database and you must manually enforce consistency. No joins means it’s really easy to distribute data to different machines. You don’t have to worry about foreign keys are doing joins or how to split the data up. Worked out really well. Worries of using a relational database are a thing of the past.


In the age of big data, it's very rare that the database these students will work on in the future will stay on only one disk. As soon as the data expands physical machine boundary, all **those beautiful normalization,  join, sub-queries and transactions all become completely useless.**

To prepare the students for future, I strongly recommend the universities also teaching the students these:



	
  * How to denormalize databases.  Teach them redis. Get them to think about how NOT to use lock. Teach them the master and slave concepts.

	
  * Explain how[ MongoDB's sharding](http://www.mongodb.org/display/DOCS/Sharding+Introduction) works.  Let students work out how to pick the right index and keys to shard on.

	
  * Experiment with Google App Engine, particularly the [DataStore](https://developers.google.com/appengine/docs/python/gettingstartedpython27/usingdatastore) so the students know the basic of BigTable and think more carefully on how to pick the best row id.

	
  * Play around with Riak.  Think about how [vector clock](http://wiki.basho.com/Vector-Clocks.html) works. What the "[eventual consistency](http://www.allthingsdistributed.com/2008/12/eventually_consistent.html)" really means.


([Again](http://alexdong.com/learn-a-language-you-wont-use-in-work/), if you are a student and you have read *any* of the above paper. Drop me a message. I've got a job for you. )
