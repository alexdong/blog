---
layout: post
title: "Digital photo printing, Shadow DOM, Local newspaper as civic duty and the brilliance of javascript"
date: 2013-08-08 22:06
comments: true
categories: 
- links
---

[Digital photo printing: 10 years after](http://petapixel.com/2013/07/25/digital-photo-printing-10-years-after/):
> Is anyone still printing photos? 
> Research firm InfoTrends did a survey of Internet connected households in EU, and photo printing went up 11% in 2012 compared to 2007-2008. Similarly, U.S.-based online photo printing has become a big deal, growing by about 20% annually between 2007-2012 according to market research firm IbisWorld. Three significant reasons for this growth are: the adoption of digital cameras, ability to transport photos online, and the increase in broadband and mobile Internet connections.
> 48% of the online photo printing market in the U.S. being prints on paper..   11.2% canvas and frame prints; 19.7% photobooks

[Why I subscribe to the Ann Arbor Chronicle](http://blog.jonudell.net/2012/10/30/why-i-subscribe-to-the-ann-arbor-chronicle/): My ideal local newspaper in 2020 will be one run by volunteers, locals vote for issues to be covered and volunteers would write subjective report. Ann Arbor Chronicle's donation increase over the last a few years seems to confirm the possibility of this. 
> Launched in September 2008, the Ann Arbor Chronicle is an online newspaper that focuses on civic affairs and local government coverage. Although we’d likely be classified by most folks as “new media,” in many ways we embrace an ethos that runs contrary to current trends: Longer, in-depth articles; an emphasis on factual accuracy and thoroughness, not speed; and an assumption that our readers are thoughtful, intelligent and engaged in this community.

[What the Heck is Shadow DOM?](http://glazkov.com/2011/01/14/what-the-heck-is-shadow-dom/): HTML's own way for building custom controls. The idea is there could a hidden dom structure that's normally hidden from javascript and css. The custom control author can choose to expose some of it via psuedo-selectors. `<input type="slider">`, `<video>` are good examples. More concrete use cases can be found [here](http://wiki.whatwg.org/wiki/Component_Model_Use_Cases). 

[Staring at the Sun: Dalvik vs. ASM.js vs. Native](https://blog.mozilla.org/javascript/2013/08/01/staring-at-the-sun-dalvik-vs-spidermonkey/): Javascript does have the promise of a popular language. It's messy. It's ugly. It has layers and layers of patches yet everytime you feel it has hit a wall, a project like [asm.js](http://asmjs.org) will come and lift it into stratosphere. 
Sometimes I do hope that WebOS would make it to the end if the [webkit issues were that easy to solve](http://www.theverge.com/2012/6/5/3062611/palm-webos-hp-inside-story-pre-postmortem). I sincerely wish FireFox and Mozilaa best luck in breaking up the walled gardens. 
> 1. Asm.js is reasonably competitive with native C++ code on ARM. Even discarding the one score where asm.js did better, it executes at around 70% of the speed of native C++ code. These results suggest that apps with high performance needs can use asm.js as the target of choice for critical hot-path code, achieving near native performance.
> 2. Asm.js competes very well on mobile performance compared to Dalvik. Even throwing out the benchmarks that are highly favourable to asm.js (binary-trees and fasta), there seems to be a consistent 10-50% speedup over comparable Dalvik code.

