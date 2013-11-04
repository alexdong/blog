---
layout: post
title: "Responding to peer review, lisp as a meta language, future of blogging is linking and technology has lost its golden child image. "
date: 2013-07-04 16:47
comments: true
categories: 
- links
---

[Responding to peer review](http://matt.might.net/articles/peer-review-rebuttals/): Some concrete examples of how to write rebuttals to peer reviews. Sometime I do wish that on internet, we can construct our discourse following these guidelines. 
> However you decide to reply to a reviewer, several principles always apply:
> 
> 1. Be polite. Lashing out at a negative reviewer is not going to change their opinion.
> 2. Be conciliatory. If a reviewer is wrong, don't say they're wrong. Say "there seems to be a misunderstanding." If the misunderstanding arose from poor presentation, admit it and offer to fix it.
> 3. Be thorough. Don't dodge any points or refuse to answer any questions. If the reviewers found a flaw, admit the flaw and offer a fix (if you can find one).

[Interview with Marc Battyani](http://lisp-univ-etc.blogspot.co.nz/2013/06/lisp-hackers-marc-battyani.html?m=1): There are high performance programming languages like C, there are highly expressive languages like Python. And there are Lisp, which is expressive enough to be used as a DSL to generate code for high performance systems. 
> Domain Specific Language Compilers and various other tools written in Common Lisp. [...] on 10Gb/s Ethernet market data packets coming from exchanges like the NASDAQ we process the IP/UDP/multicast network stack, extract the messages from the packets, parse/decode/filter/normalize those messages, maintain the indexed order book data structures, aggregate the price levels per stock, generate output messages and finally send them to a server through PCI-express or 10Gb/s Ethernet network stacks. The nice thing is that we do all that fully pipelined at a rate of one message every 12 nanoseconds! To have an idea of how fast it is, in 12 ns the light will only travel 3.6 meters (11.8 ft). Another way to view this performance is that the system can process 83 Millions of financial messages per second without any queuing.

[The future of blogging platform is ... a linking service](https://news.ycombinator.com/item?id=5968822):  Well said. 
> The underlying value proposition by any sort of blogging engine (Posthaven, Medium, Svbtle, et al) is limited to a network, ease of use, and a good design. For most tech people, ease of use is a non-factor (you can extol 'distractions-free design', but you can put vim or Byword in full-screen mode) -- and I think the way people are reading is shifting away from individual sites and towards external services to the extent that design isn't a huge factor (everything looks the same in NewsBlur or Instapaper.)
> [...]
> I can't help thinking that the winner of this nouveau publishing spectrum isn't going to be a hosting service, but a linking service. You might never get Patrick McKenzie to blog on your platform (because why would he?) but you can always link to his material.

[Technology: we can change our leadership, or we can quit.](http://michaelochurch.wordpress.com/2013/06/24/technology-we-can-change-our-leadership-or-we-can-quit/)
> Technology has lost its “golden child” image, with piñatas of Google buses being beaten to shit in San Francisco, invasions of privacy making national headlines, and an overall sense in the country that our leadership’s exceptionalist reputation as the “good” nouveau riche is not deserved and must end. To put it bluntly, the rest of the country doesn’t like us– any of us– anymore. We’ve lost that good faith, in technology, that allowed us to be rich (well, a few of us) and not hated, even in the midst of a transformational, generation-eating recession. 2013 will be remembered as the year when popular opinion of “Silicon Valley” imploded.
