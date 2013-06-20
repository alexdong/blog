---
layout: post
title: "Python on LLVM, Sequencing tuatara genome, the Pragmatic web and cost of a computer on your face"
date: 2013-06-19 08:04
comments: true
categories: 
- links
---

[Numba vs. Cython: Take 2](http://jakevdp.github.io/blog/2013/06/15/numba-vs-cython-take-2/): The author compares different python implementations for N dimension pairwise distance.  Numba stands out brilliantly: *a single function decorator results in a 1300x speedup of simple Python code. I'm becoming more and more convinced that Numba is the future of fast scientific computing in Python.* Two things makes it so fast: 1) no dynamic type checking; 2) a new `autojit` that leverages the llvm;  (Via: [Nick Philips](https://twitter.com/monsterlemon))

[Why sequence the tuatara genome?](http://sciblogs.co.nz/tuataragenome/): New Zealand scientists are starting to sequencing tuarara genome. Here is why it's so important: *Modern birds descend from one branch in the diverse group we call dinosaurs, but each of those ten thousand species are dinosaurs. The tuatara, on the other hand, are the only living members of a lineage that separated from other reptiles more than 200 million years ago.*  (If you can't see the graph, it's [here](http://sciblogs.co.nz/tuataragenome/files/2013/06/tree_graph.png))

[Paul Irish on Chrome Moving to Blink](http://alistapart.com/blog/post/paul-irish-on-chrome-moving-to-blink): The part I really like: *Let me take a moment to provide my own perspective on Dart. :) Now, as you know, I’m a JavaScript guy, so early on, I took a side and and considered Dart an enemy. JavaScript should win; Dart is bad! But then I came to realize the Dart guys aren’t just setting out to improve the authoring and scalability of web application development. They also really want the web to win. Now I’ve recently spoke about how The Mobile Web Is In Trouble, and clarified that my priorities are seeing it provide a fantastic user experience to everyone. For me, seeing the mobile web be successful trumps language wars and certainly quibbling over syntax. So I’m happy to see developers embrace the authoring advantages of Coffeescript, the smart subset of JavaScript strict mode, the legendary Emscripten & asm.js combo, the compiler feedback of TypeScript and the performance ambitions of Dart. It’s worth trying out technologies that can leapfrog the current expectations of the user experience that we can deliver. Our web is worth it.*

[To justify having a computer on your face for everyone to see would have to deliver spectacular results.](http://plc.vc/google-glass): *if Google Glass would let you see 10x better than 20:20 vision then it might be a compelling proposition.  The problem Google Glass has is that it simply isn’t much better than a smart phone, and it comes as a huge price – having something on your face.*
