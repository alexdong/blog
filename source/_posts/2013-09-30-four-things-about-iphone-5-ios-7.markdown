---
layout: post
title: "Four iPhone 5/iOS 7 technical improvements that caught my eyes"
date: 2013-09-30 10:22
comments: true
categories: 
- technology
- strategy
- links
---

There have been a lot of articles written about the new iPhone 5 so here I will skip all the fluffy stuff and focus on four technical changes that have caught my eyes.

First, the new 64-bit CPU and the [Object-C runtime changes](http://www.mikeash.com/pyblog/friday-qa-2013-09-27-arm64-and-you.html). This is the real deal. 

> Objective-C objects are contiguous chunks of memory. The first pointer-sized piece of that memory is the isa. Traditionally, the isa is a pointer to the object`s class. 

> ARM64 running iOS currently uses only 33 bits of a pointer, leaving 31 bits for other purposes. Class pointers are also aligned, meaning that a class pointer is guaranteed to be divisible by 8, which frees up another three bits, leaving 34 bits of the isa available for other uses. Apple's ARM64 runtime takes advantage of this for some great performance improvements.

> Probably the important performance improvement is an inline reference count. On ARM64, 19 bits of the isa field go to holding the object's reference count inline. That means that the procedure for retaining an object simplifies to only one instruction instead of five. 

> My casual benchmarking indicates that basic object creation and destruction takes about 380ns on a 5S running in 32-bit mode, while it's only about 200ns when running in 64-bit mode. 

Then we have the new [M7 chip](http://www.macrumors.com/2013/09/24/inside-apples-a7-chip-m7-motion-coprocessor-and-more-from-the-iphone-5s/). This new chip makes it possible to use a few sensors without waking up the whole "computer". But if you look inside the chip, you'll see that it's only a consolidation rather than a revolutionary step as some media painted. It still doesn't include the "active display" or "touchless control" features that the [Moto X](http://www.anandtech.com/show/7235/moto-x-review/4) has. 
>  M7, which is actually an ARM Cortex-M3 part from NXP running at 180 MHz. The chip allows for low-power collection of motion data drawn from a Bosch Sensortec accelerometer, an STMicroelectronics gyroscope, and an AKM magnetometer.

> After collecting information from the accelerometer, gyroscope, and magnetometer, the M7 performs some matrix math processing magic to produce an absolute orientation of the phone relative to the world. This data is then passed to the A7 in a neat package, probably in the form of three headings (roll, pitch, and yaw). 

> Using the A7 to monitor this sort of data would be mega-overkill, so the M7 was introduced to maintain a constant, low-power watch over these sensors.

Next is the [Multi-Path TCP](http://www.multipath-tcp.org) support for Siri. (See the [qz coverage](http://qz.com/126642/apples-ios7-includes-a-surprise-a-ticket-to-the-next-generation-of-the-internet/) for less-technical discussions. ) 

> MultiPath TCP (MPTCP) is an effort towards enabling the simultaneous use of several IP-addresses/interfaces by a modification of TCP that presents a regular TCP interface to applications, while in fact spreading data across several subflows. 

> Benefits of this include better resource utilization, better throughput and smoother reaction to failures.
The multipath-tcp website also has a nice video demo of the technology. 

> We did a little demo of MultiPath TCP used over Ethernet/WiFi/3G on our Linux Kernel implementation. We start an ssh-session with X-redirection and launch xscreensaver demo on the distant MPTCP-capable server. We then turn off Ethernet and WiFi and thanks to MultiPath TCP the ssh-session is able to handover the traffic to 3G without interrupting the user-experience. Without our MPTCP Linux Kernel the session would simply stop working and the user would need to restart the ssh-session.

The last one is the two new background execution modes for apps. According to the [developer doc](https://developer.apple.com/library/ios/releasenotes/General/WhatsNewIniOS/Articles/iOS7.html):

> Apps that regularly update their content by contacting a server can register with the system and **be launched periodically to retrieve that content in the background**. To register, include the UIBackgroundModes key with the fetch value in your app’s Info.plist file. Then, when your app is launched, call the setMinimumBackgroundFetchInterval: method to determine how often it receives update messages. Finally, you must also implement the application:performFetchWithCompletionHandler: method in your app delegate.

> Apps that use **push notifications to notify the user that new content is available can fetch the content in the background**. To support this mode, include the UIBackgroundModes key with the remote-notification value in your app’s Info.plist file. You must also implement the application:didReceiveRemoteNotification:fetchCompletionHandler: method in your app delegate.
