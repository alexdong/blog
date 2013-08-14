---
layout: post
title: "Mosquito's mouthpiece, fallible human being, SSL Forward secrecy and a webhook debug tool"
date: 2013-08-07 21:58
comments: true
categories: 
- links
---

[Here’s What Happens Inside You When a Mosquito Bites](http://phenomena.nationalgeographic.com/2013/08/06/heres-what-happens-inside-you-when-a-mosquito-bites/)
Absolutely stunning series of short microscope video on how flexible and intelligent the mosquito's mouthpart is. 

[Ubuntu Forums are back up and a post mortem](http://blog.canonical.com/2013/07/30/ubuntu-forums-are-back-up-and-a-post-mortem/)
Security is hard because fallible people are always a weak part of the chain. 
> A forum moderator account was "stolen", then the attacker uses XSS to gain admin permissions. 

[SSL Labs: Deploying Forward Secrecy](http://blog.ivanristic.com/2013/06/ssl-labs-deploying-forward-secrecy.html)
> In the context of mass surveillance, however, the RSA key exchange is a serious liability. Your adversaries might not have your private key today, but what they can do now is record all your encrypted traffic. Eventually, they might obtain the key in one way or another (e.g., by bribing someone, obtaining a warrant, or by breaking the key after sufficient technology advances) and, at that time, they will be able to go back in time to decrypt everything.
> ...
> but generates session keys in such a way that only the two parties involved in the communication can obtain them. No one else can, even if they have access to the server's private key. 
The article provides a good entry-leve description to SSL's support of 
Forward Secrecy using DHE and ECDHE algorithm.  The author also has a follow-up 
post on how to configure Apache, Nginx and OpenSSL to support Forward Secrecy. 

[localtunnel: Expose your local web server to the Internet](https://github.com/progrium/localtunnel): A must have tool to debug webhooks. 

