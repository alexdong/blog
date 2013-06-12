---
layout: post
title: "Standing ovation model and its application on user acquisition"
date: 2013-06-03 07:53
categories: 
- startup
- marketing
---

The [Standing Ovation Problem](http://www2.econ.iastate.edu/tesfatsi/StandingOvation.MillerPage.pdf) is a social science model that is extremely simple yet "provides a rich domain to explore the world".  Here is how a SOP is defined:

> A brilliant economics lecture ends and the audience begins to applaud. The applause builds and tentatively, a few audience members may or may not decide to stand. Does a standing ovation ensue or does the enthusiasm fizzle?

You can watch Scott explains the theory in this [18-minutes video](https://class.coursera.org/modelthinking-2012-002/lecture/11) but here is the gist of the theory. The following 6 factors have a strong impact on whether a standing ovation happens or not. 

> 1. Higher quality
> 2. Lower Threshold: how easy the audiences are to be satisfied. 
> 3. Larger Peer Effects: how likely the audiences are influenced by each other. 
> 4. More variation
> 5. Use celebrities
> 6. Big groups. 

The first three are self explainable and in most cases out of our control. What's more fascinating are 4-6. Let's dive into each one a bit more. 

First, **more variation**. Let's say there are two groups. Each group has 6 people. Here is the number of other people who has to stand up before one stand up: `(1, 1, 1,  2, 2, 2)`. This basically says that for three people in the group, if they see one person stand up, they will stand up. The other three needs two people. Say we have a second group like this `(0, 1, 2, 3, 4, 5)`. `0` means the person will stand up no matter how others behave and `5` means that dude is really reluctant to change his body position unless almost everyone is doing it. Which one of these two groups will be more likely to pull a standing ovation? Yes, the second one even though it has a difficulty score of `2.5` whereas the first group has only `1.5`.  

The difference? The second group has a more varied group so that a cascading effect can happen; also it has the `0` [movement](http://www.ted.com/talks/derek_sivers_how_to_start_a_movement.html) guy. Without any of these two factors, getting the second group to all stand up would be hard. 

Second, **use celebrities**.  The model uses celebrities to describe the people sitting at the front rows. They are not necessarily celebrities per se but they share the same traits which is they can't see other people's behavior yet everyone else can see theirs.  This gives them the power as 'magnifiers'.  [^Academics]

Third, **big groups**.  If people come in groups, let's say the wife stands up, there is a pretty high chance that the husband would get his bum up.  If we have an audience like this one: `{1: 0%, 2: 30%, 3: 30%, 4: 20%, 5: 10%, 6: 10%}`, which is a group that's hard to please. Having a couple to stand up would be sufficient to *tip* the whole audience over even if no one would stand up without two other people do it before them. 

To apply this theory to user acquisition is a fun exercise. If we have a software product that makes it really easy for people to have a link blog[^WeAreBuildingOne], basically to share interesting links in the form of a blog like [DaringFireball](http://daringfireball.net/linked/), here is a list of things that could be done to help getting new user sign ups:

* Besides getting onto the radar of big social news sites, finding many topic niches where people tie closely together would be important too. Say targeting niches where there is at least a forum for people to hang out. 
* Groups with larger peer effects would be the natural candidates. These are the groups where people pays lots of attention to each other and eager to jump onto the new bandwagon. 
* For each group, find out who are the celebrities and get them to use the service first. Then we can go after the other group members by leveraging the first batch of 'celebrities'

[^Academics]: The people sit in the last role is defined as academics, which I find quite funny. The nature of the academics is that they can see everyone yet no one can see them. Which means that they have the perfect information yet zero influence. 
[^WeAreBuildingOne]: [Aldo Cortesi](http://corte.si) and I are building one such a service at the moment. If you are interested to have one when we launch it, please follow us on twitter as [@alexdong](http://twitter.com/alexdong) and [@cortesi](http://twitter.com/cortesi). 