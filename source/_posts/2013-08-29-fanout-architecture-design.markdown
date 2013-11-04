---
layout: post
title: "Fanout architecture design, Apache spark, algorithms beats Moore's law and Linux's SO_REUSEPORT"
date: 2013-08-29 23:07
comments: true
categories: 
- links
---

[Fanout architecture design guides from Google (pdf)](http://static.googleusercontent.com/external_content/untrusted_dlcp/research.google.com/en/us/people/jeff/Berkeley-Latency-Mar2012.pdf): If a server has an average 1-ms latency but has a 1% chance of taking longer than 1 second to finish a request, spreading a request across 100 such servers would mean that 63% requests will take more than 1 second.  This paper introduces some good engineering practices for designing a fanout architecture. 

[Apache Spark project](http://spark.incubator.apache.org/): When memory is so cheap, why don't run mapreduce in memory? 
> Spark was initially developed for two applications where placing data in memory helps: iterative algorithms, which are common in machine learning, and interactive data mining. In both cases, Spark can run up to 100x faster than Hadoop MapReduce. However, you can use Spark for general data processing too. 

[Progress in Algorithms Beats Moore’s Law](http://agtb.wordpress.com/2010/12/23/progress-in-algorithms-beats-moore%E2%80%99s-law/):
From 1988 to 2003, solving the same model using linear programming sees an improvement by a factor of roughly 43 million.  
> Of this, a factor of roughly 1,000 was due to increased processor speed, whereas a factor of roughly 43,000 was due to improvements in algorithms! 

[Linux kernel 3.9 introduced SO_REUSEPORT](http://freeprogrammersblog.vhex.net/post/linux-39-introdued-new-way-of-writing-socket-servers/2): This patch allows multiple processes to bind to the same IP. This opens up the possibility of uninterrupted server upgrade by gradually replacing old processes with new ones.  This used to be a big selling point for erlang, but now languages like Ruby, Python or node.js would be able to do it too. 
