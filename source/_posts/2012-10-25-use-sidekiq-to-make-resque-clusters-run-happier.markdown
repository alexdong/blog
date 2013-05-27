---
author: alexdong
comments: true
date: 2012-10-25 14:19:05
layout: post
slug: use-sidekiq-to-make-resque-clusters-run-happier
title: Use sidekiq to make resque clusters run happier
wordpress_id: 225
categories:
- code
---

Resque is a single-thread, single-process, fork-based process. Running lots of them incurs serious swapping. There have been proposals of running [jruby](http://blog.carbonfive.com/2011/09/16/improving-resques-memory-efficiency/) to solve this problem but looks like Sidekq and the upcoming Ruby 3.0 offer a cleaner solution.


> Sidekiq uses multithreading so it is much more memory efficient than Resque (which forks a new process for every job). You'll find that you might need 50 200MB resque processes to peg your CPU whereas one 300MB Sidekiq process will peg the same CPU and perform the same amount of work. Please see my blog post on Resque's memory efficiency and how I was able to shrink a Carbon Five client's resque processing farm from 9 machines to 1 machine.


via [mperham/sidekiq](https://github.com/mperham/sidekiq).
