---
author: alexdong
comments: true
date: 2012-09-05 22:31:32
layout: post
slug: how-much-unit-tests-is-enough
title: How much unit tests is enough?
wordpress_id: 117
categories:
- code
---

[Kent Beck](http://en.wikipedia.org/wiki/Kent_Beck) had this perfect answer for this question at [StackOverflow](http://stackoverflow.com/questions/153234/how-deep-are-your-unit-tests/153565#153565):


> I get paid for code that works, not for tests, so my philosophy is to** test as little as possible to reach a given level of confidence** (I suspect this level of confidence is high compared to industry standards, but that could just be hubris). If I don't typically make a kind of mistake (like setting the wrong variables in a constructor), I don't test for it. I do tend to make sense of test errors, so I'm extra careful when I have logic with complicated conditionals. When coding on a team, I modify my strategy to carefully test code that we, collectively, tend to get wrong.

Different people will have different testing strategies based on this philosophy, but that seems reasonable to me given the immature state of understanding of how tests can best fit into the inner loop of coding. Ten or twenty years from now we'll likely have a more universal theory of which tests to write, which tests not to write, and how to tell the difference. In the meantime, experimentation seems in order.
