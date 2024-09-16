---
layout: post
title:  "Bitcoin Lightning Network Flaws"
date:   2024-05-23 00:00:00 -0700
categories: technology cryptocurrencies Bitcoin Lightning-Network
---

<!-- Research Links and Notes
https://www.truthcoin.info/blog/lightning-limitations/


https://lightning.network/lightning-network-paper.pdf


https://medium.com/@jonaldfyookball/mathematical-proof-that-the-lightning-network-cannot-be-a-decentralized-bitcoin-scaling-solution-1b8147650800


Topics:
 - LN cannot scale to entire world
 - LN cannot be controlled by average person
 - LN is not intuitive
 - LN for merchents sucks
 - LN for every day use sucks 
-->

The Bitcoin Lightning Network (LN) is a system built on top of the Bitcoin blockchain that allows for faster and cheaper transactions using micropayment channels. The rationale is that the Bitcoin blockchain is too expensive and limited to serve as a payment system for billions of people making day-to-day transactions like buying coffee. Instead a few on-chain transactions can be made to open a payment channel between two notes and handle an infinite amount of micropayments through that payment channel, never touching the Bitcoin blockchain.

See a high level diagram here:
![Bitcoin Lighting Network Diagram](/assets/img/bitcoin-ln-1.png)
This diagram came from [bitcoin.design](https://bitcoin.design/guide/how-it-works/liquidity/)



