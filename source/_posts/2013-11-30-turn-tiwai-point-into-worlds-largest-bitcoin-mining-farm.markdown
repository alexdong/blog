---
layout: post
title: "Turn Tiwai Point into the world's largest Bitcoin mining farm"
date: 2013-11-30 20:49
published: false
comments: true
categories: 
- fun
---

The [Tiwai Point Aluminium Smelter](http://en.wikipedia.org/wiki/Tiwai_Point) is one of the 
largest industrial facilities in New Zealand.
Between 2008 and 2013, aluminium prices fell by more than 30 percent. The owner, Rio Tinto, has 
threatened to close the Tiwai Point smelter if it can't get a cheaper deal for electricity 
from retailer Meridian, or the Government fails to give it a substantial subsidy. 
The Smelter consumes about 15% of all electricities NZ generates. So there have been lots of 
discussions of what NZ should do if Rio Tinto does shut it down.

Here is a crazy idea. How about build a large a Bitcoin mining farm to use the electricity?  
This started as a [joke](https://twitter.com/farmgeek/status/406637109521305601) on 
Twitter but after thinking about it for a while, it actually makes good sense. 

Let's start with the technical side of the bitcoin mining business first. 

You can think of the Bitcoin system as a global ledger and each transaciton 
as a switch from asset to liability in this ledger.  The Bitcoin miners play the roles of 
the central banks except that there are [thousands](http://millybitcoin.com/how-many-people-are-bitcoin-mining/) 
of these "central banks" out there competing to perform the "clearing house" 
function for every transaction that happens in the Bitcoin universe. 

The task of these clearing houses is very simple: they group a set of transactions together into a block,  
perform some checks and then put a stamp on it. The key step here is to "perform some check". 
This involves guessing a random number in, say, a trillion possibilities. There is no smart here. 
It's only about how fast you can brutal-force through all the possibilities and 
how cheap you can do this. 

Of all those thousands participants, only the fastest one 
will win the transaction. All the rest, despite the fact that they might be half
way through, will simply throw away the existing work and start again. 

Here, the speed is determined by two factors: pure luck and the speed of the guess. 
The luck is mathmatically gauranteed to be equal, or, more accurately, random. 
Even with the fastest computer, you might still lose to a tiny computer in one's garage.
You might think that this is a terribly competitive game to get yourself into. 
But it is a fierce competition only in the sense that it's a game of lottery
where only thousand of people buys and there are hundreds of chances to win
everyday. 


So the real factor you can control is how fast you can guess. 
Once you've invested in the hardware, the main running cost is
the electricity bill, which Tiwai Point seems to have plenty of.

It's a common mistake to think that as we getting closer to the hard limit of 
[21-million Bitcoins](http://bitcoin.stackexchange.com/questions/161/how-many-bitcoins-will-there-eventually-be), 
there will be no money left to be made for the miners.  Since a Bitcoin transaction won't 
succeed until it's processed by a miner. People who want 
a faster transaction, instead of waiting 7 hours, will usually offer a transaction fee.
According to the [Bitcoin website](https://en.bitcoin.it/wiki/Transaction_fees): 

> It is envisioned that over time the cumulative effect of collecting transaction fees 
> will allow somebody creating new blocks to "earn" more bitcoins than will be mined 
> from new bitcoins created by the new block itself. This is also an incentive to keep 
> trying to create new blocks even if the value of the newly created block from 
> the mining activity is zero in the far future.


