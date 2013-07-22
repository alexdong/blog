---
layout: post
title: "Browser fingerprint, randomness of hashing algorithm, rate limiting as meta-tool and KPI for local government"
date: 2013-07-22 22:58
comments: true
categories: 
- links
---

[fast browser fingerprint using javascript](https://github.com/Valve/fingerprintjs)
> Fingerprinting is a technique, outlined in the research by Electronic Frontier Foundation, of anonymously identifying a web browser with accuracy of up to 94%.  
> Browser is queried its agent string, screen color depth, language, installed plugins with supported mime types, timezone offset and other capabilities, such as local storage and session storage. Then these values are passed through a hashing function to produce a fingerprint that gives weak guarantees of uniqueness.  
> No cookies are stored to identify a browser.

[Awesome data visualization of the randomness of different hashing algorithm](http://programmers.stackexchange.com/questions/49550/which-hashing-algorithm-is-best-for-uniqueness-and-speed): Murmur seems to be pretty good.  The images is one of the best of its kind. 

[Rate Limiting and Velocity Checking](http://www.codinghorror.com/blog/2009/02/rate-limiting-and-velocity-checking.html): Rate limiting is one of the hadful meta tools that are easy to deploy yet much more effective to prevent possible attacks.   
> I was shocked how little comprehensive information was out there on rate limiting and velocity checking for software developers, because they are your first and most important line of defense against a broad spectrum of possible attacks. It's amazing how many attacks you can mitigate or even defeat by instituting basic rate limiting.

[KPI dashboard for your community and local government](http://knightlab.northwestern.edu/2013/07/15/clay-johnson-on-creative-technologists-designing-with-empathy-and-news-as-a-community-service/)
> When I talk about my book, the one question I ask consistently is “Who here knows the child poverty rate of the area they live in?” And nobody knows. Nor does anybody know the direction it’s moving! But I think fairly soon, we’re going to see healthy community key indicators coming up and getting reported on, and it’s going to change the way the newsroom works a bit.
