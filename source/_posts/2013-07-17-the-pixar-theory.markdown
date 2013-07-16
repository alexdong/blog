---
layout: post
title: "The pixar theory, Authentic Design, Problem with Apple's Ad and Malware hidden in JPG Headers"
date: 2013-07-17 09:56
comments: true
categories: 
- links
---

[The Pixar Theory](http://jonnegroni.com/2013/07/11/the-pixar-theory/): When Steve Jobs said he lives at the intersection of technology and humanity, I guess in his mind he didn't see a particularly bright future. 
> Every Pixar movie is connected. I explain how, and possibly why. Several months ago, I watched a fun-filled video on Cracked.com that introduced the idea (at least to me) that all of the Pixar movies actually exist within the same universe. Since then, I’ve obsessed over this concept, working to complete what I call “The Pixar Theory,” a working narrative that ties all of the Pixar movies into one cohesive timeline with a main theme. 

[In 20 Years, We’re All Going To Realize This Apple Ad Is Nuts](http://www.fastcodesign.com/1673020/in-20-years-we-re-all-going-to-realize-this-apple-ad-is-nuts): I like this article but let's keep in mind that the reality is rarely as dramatic or black-and-white as reporters love to write in. 
>  the fundamental interactions behind our gadgets are designed to constantly lure us back into the four-inch world, nudging us with vibration, push notifications, and impromptu xylophone solos to almost touch all of the people in our lives doing the same thing on another four-inch screen somewhere else.

[Authentic Design](http://www.smashingmagazine.com/2013/07/16/authentic-design/): A good landscape overview to separate the concept of "flat design", "minimalist design" from "authenticity in design".  The author has done a good job guiding one through the history of design movements in the last two centuries.  I like his definition of authentic design. 
> In its desire for authenticity, the Modern design movement curbed the ornamental excess of the 19th century, making design fit the age of mass production. 
>
> (In late 19 century) The idea was to highlight beauty of form in objects that were purely functional. For the modern design movement, decoration was not necessary. Beauty and elegance were to emerge from the design of the content itself, not from a superficial coat of decoration.
> 
>  Authentic design is about using materials without masking them in fake textures, showcasing their strengths instead of trying to hide their weaknesses. Authentic design is about doing away with features that are included only to make a product appear familiar or desirable but that otherwise serve no purpose.
> 
>  "Its artless shape gave it a certain naive innocence that suggested authenticity, just as the early versions of the Land Rover had the kind of credibility that comes with a design based on a technically ingenious idea rather than the desire to create a seductive consumer product." --  Deyan Sudjic commented on the design of the iconic Anglepoise lamp
>
> Design whose beauty lies in function is not the same thing as minimalist style. With the former, the designer seeks to remove the superfluous, to make the product easier to understand, to make it perform better and to make the most of its medium. The latter seeks to create a minimalist aesthetic, to give the object an aura of simplicity and cleanliness. One is a fundamental principle of design, the other a stylistic choice.
> 
> It would be a mistake to rigidly apply a minimalist design aesthetic to an interface as a style in the hope of making the interface simpler and more digitally “authentic.” For example, ruthlessly eliminating visuals such as shadows, colors and varied background styles would not necessarily make an interface easier to use. In some cases, it would achieve the opposite by undermining hierarchy and focus, which were established by those very shadows and background colors.

[Malware Hidden Inside JPG EXIF Headers](http://blog.sucuri.net/2013/07/malware-hidden-inside-jpg-exif-headers.html): I like PHP for its flexibility. You just modify a file and you're done. But with that flexibility comes with huge security risks. In fact the security holes in PHP has scared me away from wordpress into Jekyll.  This backdoor is possible because this strange decision to make a string replace be able to execute a file. 
> preg_replace has a hidden and tricky option where if you pass the “/e” modifier it will execute the content (eval), instead of just searching/replacing.
