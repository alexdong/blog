---
layout: post
title: "Rob Malda on social news, Hemingway's eye, InnoDB's full text search and Etsy's crack down on SSL CAs."
date: 2013-08-08 22:40
comments: true
categories: 
- links
---

[Tim B. Lee interviewed Rob Malda](http://www.washingtonpost.com/blogs/the-switch/wp/2013/08/07/slashdot-founder-rob-malda-on-why-there-wont-be-another-hacker-news/): The part of social news, the problem with hacker news and twitter are the most interesting bits to me. 
> I did not premeditate anything. I just winged it, and when I saw problems I triaged them. The Slashdot system was very much evolved and not designed.   One thing I learned is don’t spend your entire life playing predictive defense against attacks that will never happen. Real people are very clever. If they choose to attack you they’ll attack you in ways you can’t predict.
> Most people are just purely passive consumers, and that’s okay. I think a lot of people in this space obsess too much over trying to convert passives into actives. Some people are just wired to be that kind of person. Others aren’t. That’s okay.
> With more and more voices, you tend toward broader subjects. Eventually it becomes less and less interesting. But what’s interesting to [me] isn’t always the thing that’s most lucrative. I had a pretty strong belief that the population of Slashdot users was relatively fixed. That makes for a crappy business model. You want to have a million really good users and be done? How does make the chart go up and to the right?

[Hemingway lookalike contest](http://www.huffingtonpost.com/2013/08/01/hemingway-lookalike-contest_n_3690493.html?utm_hp_ref=arts): [Aldo](http://corte.si) described Hemingway using following terms: "full of action, well seasoned, brilliant, paranoid, depressed and committed suicide".  I found only the real photo captures all these characters. The participants seems to lack one of these "action, brilliant or depressed".  I happend to notice that his left eye seems to lack the paranoid and a color of brilliance. [Turned out](http://answers.yahoo.com/question/index?qid=20070916132644AAArXuY) "Hemingway's left eye was defective from birth ... In May of 1918, Hemingway wanted to join the Army but could not due to a defective left eye which he inherited from his mother."

[Performance evaluation of InnoDB's Full-text search in Mysql 5.6](http://www.mysqlperformanceblog.com/2013/07/31/innodb-full-text-search-in-mysql-5-6-part-3/): disappointing. Slow to index. Slow to query. It bloats the code base. I don't know why this feature needs to be built in the first place. 
>  InnoDB FTS fills a need for those people who want the features and capabilities of InnoDB but can’t modify their existing applications or who just don’t have enough FTS traffic to justify building out a Sphinx/Solr/Lucene-based solution.

[Reducing The Roots of Some Evil](http://codeascraft.com/2013/07/16/reducing-the-roots-of-some-evil/): SSL CA is in such a mess that company like Etsy is manually trimming down the number of CA they trust. This sounds good but feels a bit unscalable. 
