---
author: alexdong
comments: true
date: 2012-10-05 05:00:23
layout: post
slug: git-pull-vs-git-rebase-its-about-different-engineering-cultures
title: 'git pull vs. git rebase: it''s about different engineering cultures'
wordpress_id: 178
categories:
- code
- startup
---

It's not often for me to become interested in technology itself these days. But the discussion between git pull and git rebase has interested me a lot.  Not for its own technology details but more as a tool to either loose or strengthen an engineering culture.

git pull encourages a rather loose, relax and, in the long run, ad-hoc manner of team work.  This suits startup cultures quite well.   It's fast to learn and easy for people who migrate from older version controls like subversions to learn.  Engineers works on his own little branch. He has no reason to integrate with other people's code until the very end of one's little project is finished.  The commit history ends up having messages that describes more about the code and less about the reason and thinking behind this list of patches.  For example, if you happen to follow the resque project, you'll realize that [a commit message like this](https://github.com/defunkt/resque/commit/832fb9d696c4367ae17d99aaa2ef6b43268605c5) is not really that helpful. 7 lines of changes.  One line comment without explaining why the 'destroy' is delayed.

git rebase encourages comparatively stricter engineering culture. One has to pay attention to not only his code, but also the commit histories.  Projects like linux kernel uses it to enforce a culture of [ keep clean history](http://www.mail-archive.com/dri-devel@lists.sourceforge.net/msg39091.html). Linus even wrote up what a good commit would look like [here. ](https://github.com/torvalds/subsurface/blob/master/README#L161)  I can see how this could be very helpful in a project where the code needs to be maintained 15 years later by totally different set of people.  A clean history, instead of a loose list of incremental functional changes, will provide more context in the long run.  As a sample,[ check out this patch](http://git.kernel.org/?p=linux/kernel/git/torvalds/linux-2.6.git;a=commit;h=ce57e981f2b996aaca2031003b3f866368307766) by Linus for a firmware related patch. [4 lines](http://git.kernel.org/?p=linux/kernel/git/torvalds/linux-2.6.git;a=blobdiff;f=drivers/base/firmware_class.c;h=81541452887bd3ce5d868909e3fb753fb3d6b124;hp=e85763de928f096e46cbfd74abb69c064e5c2101;hb=ce57e981f2b996aaca2031003b3f866368307766;hpb=e1cc485262846dcad931bf85ee655cbbb815bfe6) of changes, 8 lines of comments on the commit.


