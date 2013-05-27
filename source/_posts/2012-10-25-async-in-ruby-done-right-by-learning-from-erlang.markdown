---
author: alexdong
comments: true
date: 2012-10-25 14:26:42
layout: post
slug: async-in-ruby-done-right-by-learning-from-erlang
title: Async in Ruby done right by learning from Erlang
wordpress_id: 228
categories:
- code
---

I wrote about [learning a language you won't use in work](http://alexdong.com/learn-a-language-you-wont-use-in-work/), mainly because by doing so, you'll gain understanding of the "right way" to do things.  [Perspective](http://alexdong.com/alan-kay-normal-considered-harmful/) sometimes worth a lot more than people expected. Celluloid is a Ruby project that seems to get async model right by taking ideas from Erlang and implement them.


> By combining concurrency with object oriented programming, Celluloid frees you up from worry about where to use threads and locks. Celluloid combines them together into a single concurrent object oriented programming model, encapsulating state in concurrent objects and thus avoiding many of the problems associated with multithreaded programming. Celluloid provides many features which make concurrent programming simple, easy, and fun:

Automatic "deadlock-free" synchronization: Celluloid uses a concurrent object model which combines method dispatch and thread synchronization. Each actor is a concurrent object running in its own thread, and **every method invocation is wrapped in a fiber that can be suspended whenever it calls out to other actors, and resumed when the response is available**. This means methods which are waiting for responses from other actors, external messages, or other system events (including I/O with Celluloid::IO) can be suspended and will never block other methods that are ready to run. This won't prevent bugs in Celluloid, bugs in other thread-safe libraries you use, and even certain "dangerous" features of Celluloid from causing your program to deadlock, but in general, programs built with Celluloid will be naturally immune to deadlocks.

Fault-tolerance: Celluloid has taken to **heart many of Erlang's ideas about fault-tolerance in order to enable self-healing applications**. The central idea: have you tried turning it off and on again? Celluloid takes care of rebooting subcomponents of your application when they crash, whether it's a single actor, or large (potentially multi-tiered) groups of actors that are all interdependent. This means rather that worrying about rescuing every last exception, you can just sit back, relax, and let parts of your program crash, knowing Celluloid will automatically reboot them in a clean state. Celluloid provides its own implementation of the **core fault-tolerance concepts in Erlang including linking, supervisors, and supervision groups.**


via [celluloid/celluloid](https://github.com/celluloid/celluloid).
