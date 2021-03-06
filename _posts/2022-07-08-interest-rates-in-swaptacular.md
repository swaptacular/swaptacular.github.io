---
layout: post
title: Interest Rates in Swaptacular
description: >
  Explains why interest rates are important for managing a currency in
  the long run. Also, why paying interest is sometimes predatory and
  sometimes is not.
author: Evgeni Pandurski
tags: [intro]
---

In Spectacular, the issuer of each digital currency can publicly
declare an interest rate, which will be applied to all accounts in the
given currency. For example: If I create my own currency, and I
declare an interest rate of 5% on it, then for everyone that holds my
currency (and therefore I owe them something in return), every year,
there will be an automatic 5% increase in the amount that I owe them.

<!--more-->

The issuer can even declare a *negative interest rate*. For example:
If I set an interest rate of -5% for my currency, then every year,
there will be an automatic 5% *decrease* in the amount that I owe to
my creditors.

This ability of issuers to control the interest rate on their
currencies is very important, indeed. It allows the issuers to
indirectly influence the amount of their currency in
circulation.

Imagine somebody whose digital currency is very popular, stable, and
highly trusted. Inevitably, people will start hoarding this currency,
using it more and more as a store of value, and less and less to buy
things with it. Depending on the situation, this may, or may not be
what the issuer wants. For example:

* If the issuer sells durable goods, he/she will most probably need to
  keep some amount of goods in store. Normally, the more currency
  there is in circulation, the more goods must be kept in store, to
  back the issued currency. In this situation, lowering the interest
  rate, even to a negative number, is a reasonable thing to do. This
  would discourage hoarding, and encourage buying of the issuer's
  goods.

* If the issuer has enough collateral, in the form of real estate, to
  back the currency, but he/she urgently needs money for investment or
  servicing debt, then increasing the interest rate might be a clever
  thing to do. This would encourage the hoarding of the issuer's
  currency, and may allow him/her to issue more
  [IOUs](https://en.wikipedia.org/wiki/IOU) into existence.

## Isn't charging interest a bad thing?

Well, it depends. It can be a very bad thing. Especially when powerful
people legitimize the perpetual robing of powerless people, by calling
the process "payment of lawful debt".

But this is not the case in Swaptacular!

In Swaptacular, the debtors (the issuers of digital currencies)
determine the interest rate that they pay to their creditors. You see,
if a debtor feels that the interest rate on his debt is too high, he
can simply lower it, even to a rather negative number. Obviously, by
doing so, the issuer may totally destroy the confidence in his
currency, but nevertheless, this is a perfectly legal thing to do.

<div class="message">

  <b>Note:</b> The current reference implementation restricts annual
  interest rates between -50% and 100%. This prevents currency issuers
  from setting extremely negative interest rates, so as to effectively
  abolish their existing obligations; or from setting huge positive
  interest rates by mistake.

</div>
