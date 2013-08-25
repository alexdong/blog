---
author: alexdong
comments: true
date: 2012-09-03 21:27:03
layout: post
slug: learn-a-language-you-wont-use-in-work
title: Learn a language you won't use in work
wordpress_id: 110
categories:
- book
- code
- bestof
---

Today I had a chat with one of our most talented engineers who could code front-end animation effect that I wouldn't even believe it's possible.   When I started programming, it was assembly. Then c, c++, java/c#.  The new generation of programmers, however, start with html/javascript.

You know, the high level stuff.

When I asked him what he would love to play with, his answer was node.js. And that is worrying.  It's not that node.js is not cool.  Or it's not fast. Rather, it's the lack of the understanding of both **low-level stuff** like paging and locking, which one can only learn by programming in C,  and **functional programming** stuffs that allow building a complex system using macro and chain-up-functions.  So here is what I would recommend a junior engineer to read:

To have a firm grasp of low level programming concepts. **Read the redis source code** and read the common unix system calls.  [Redis: under the hood](http://pauladamsmith.com/articles/redis-under-the-hood.html) and [Redis Architecture](http://www.enjoythearchitecture.com/redis-architecture) are two excellent resources to get started. Alternatively, read [nginx](http://www.nginxguts.com/) or [varnish](http://en.wikipedia.org/wiki/Varnish_cache) source code, which is reasonable well written too.

To appreciate the beauty and power of functional programming,** learn yourself some [clojure](http://www.clojurebook.com/) or erlang.** Clojure is more robust as a functional programming language with excellent jvm support. [Erlang,](http://shop.oreilly.com/product/9780596518189.do) on the other hand, offers a great lesson on how to construct a robust distributed concurrent system. This lesson will still hold true even if you're coding in C.  Like the [Curiosity on Mars](http://jlouisramblings.blogspot.co.nz/2012/08/getting-25-megalines-of-code-to-behave.html).

(If you are a fresh graduate and you have finished any of the above book or link, drop me your CV. I've got a job for you. )
