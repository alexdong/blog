---
layout: post
title: "Many Stairs to Climb, Mozilla's RR, Fingerprints of election thieves and Layout in Flipboard"
date: 2014-03-28 17:34
comments: true
categories: 
- links
---

[Many Stairs to Climb – 2](http://www.simoneast.com/burton/?p=322)

From Simon East's Rephotographing project. Simon scanned some 130-year-old
panorama photos of Dunedin. Then he built a beautifully slider 
interface that allows side-by-side comparison between 1880 and 2014. 
 (Via: [Jinty MacTavish](https://twitter.com/jintymact/status/449385660172886016))


[Mozilla's RR debugger](http://rr-project.org)

> rr aspires to be your primary debugging tool, replacing — well, enhancing — gdb. You record a failure once, then debug the recording, deterministically, as many times as you want. Every time the same execution is replayed.
> Remember, you're debugging the recorded trace deterministically; not a live, nondeterministic execution. The replayed execution's address spaces, register contents, syscall data etc are exactly the same in every run.
(Via: [antirez](https://twitter.com/antirez/status/449189188223918080))

[Finding the statistical fingerprints of election thieves](http://www.santafe.edu/news/item/pnas-thurner-fingerprints-election-thieves/)

> In fair elections, a nation's voting pattern tends to feature one cluster, showing a general trend of voter turnout and vote for the victorious party (though some nations' regional voter preferences can distort it). Rigged ones show a cluster, but with a smear of votes toward the upper right for incremental fraud. Extreme fraud has a second, smaller, completely separate cluster at the top right corner, signifying up to 100 percent turnout and votes for the winner.
(Via: [jeresig](https://twitter.com/jeresig/status/449227101678223361))

[Layout in Flipboard - For Web & Windows](http://engineering.flipboard.com/2014/03/web-layouts/)

The Duplo page layout engine searches between 2000 to 6000 candidate layouts for the best fit. It takes three steps to come up with a layout for a page:
1) create 2000+ layouts in a decision tree structure
2) select layout and apply content: It uses Branch and bound to shrink the candidate set, then it uses a dozen of heuristic like [Perlin noise](http://en.wikipedia.org/wiki/Perlin_noise) to maintain an organic feel between pages. 
3) refining layout by aligning the DOM elements to baseline grids
(Via: [AlanInteractive](https://twitter.com/AlanInteractive/status/449355010464165888))
