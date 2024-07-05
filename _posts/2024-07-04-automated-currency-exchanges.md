---
layout: post
title: Automated Currency Exchanges
description: >
  Explains how automated exchanges between different currencies work
  in Swaptacular.
author: Evgeni Pandurski
tags: [intro]
published: false
---

I am happy to announce that after months of hard work, I have
successfully implemented a service that [creditors agents](/overview/)
can install and run, which can perform automatic exchanges between
gazillion of currencies, without using a "master" reserve currency.

For quite some time, the [My wallet app]({{
site.app_demo.creditors_webapp}}) allowed users to set an exchange
policy for every currency in their wallet, so that the creditors agent
could arrange mutually beneficial currency exchanges between users:

<!--more-->

<div class="message" id="peg-tree">
  <img src="/images/modify-exchange-policy.png"
       style="display: block; width: 50%; margin: auto"
       alt="Modify exchange policy dialog"
       >
</div>

But until very recently, this functionality was missing, and all
exchange policies set by users were ignored. [Not
anymore](https://github.com/swaptacular/swpt_trade).

## How does it work?

In a [a previous post](/2022/07/03/what-is-a-currency-peg/) I
explained that Swaptacular currencies can be pegged to other
Swaptacular, and non-Swaptacular currencies, forming a "tree" of
currency pegs.

Thus, the exchange rates between most Swaptacular currencies are
known, fixed, and **explicitly approved by currency holders**.
Therefore, the creditors agent knows:

1. The fixed price of each currency. (This price is set by the issuer
   of the currency.)
2. How much of each currency, each user is willing to sell.
3. How much of each currency, each user is willing to buy.

Having all this information makes our job much easier, compared to
traditional currency exchanges, where matching seller and buyer prices
is a major issue. In our case, we should simply look for [a possible
circular trade](/public/docs/cmb-general.pdf):

<div class="message" id="peg-tree">
  <img src="/images/circular-trade.png"
       alt="Example circular trade"
       >
</div>

If the picture above reminds you of the proverbial penny, which goes
from hand to hand, in a circle, paying troublesome old debts &mdash;
you are spot on. Here the idea is the same, but with several important
generalizations:

1. "Trading circles" are found automatically, using a relatively
   simple algorithm. The number of participants in a trading circle
   can be very big, but can also be as small as 2.

3. We can clear debts incurred not in one, but in many different
   currencies.

4. In addition to paying old debts, each trading circle can also
   create new debts.

   Note that this point is very important: In Swaptacular, creating
   new debt and issuing new money in circulation is actually the same
   thing. Also, paying old debts is the same as taking money out of
   circulation. Therefore, **we need to constantly do both**.

The crux of the matter here is that circular trades are *always*
arranged according to the exchange polices set by the currency
holders. Thus, every automatically arranged circular trade is, by
design, beneficial for all of the participants.


## What's in it for the creditors agent?

We know that the *creditors agent*'s job is to maintain the
infrastructure of servers which enables currency holders (aka
creditors) to trade, and make payments in gazillion of different
currencies. It is only fair that there should be some reward for this!

For every circular trade that the creditors agent arranges, a small
portion of the traded amounts will be retained as a reward. Thus, as
time passes, the creditors agent will end up holding some amounts of a
huge number of different currencies. Fortunately, the creditors agent
can use its own "automated currency exchanges" services, to trade the
currencies that it does not need, for currencies that it does need.
This process has not been automated yet, but I have plans to automate
it in the future.