---
layout: post
title: Under the Hood — Digital Coins
description: >
  Explains how Swaptacular's digital coins work.
author: Evgeni Pandurski
tags: [under-the-hood]
published: false
---

In [a previous post](/2023/09/02/under-the-hood-payments-web-api/) I
outlined how Swaptacular's Payments Web API works. In this post, I will talk
about Swaptacular's *digital coins*.

Every Swaptacular currency is uniquely identified by its *debtor ID* (a
64-bit integer number). In principal, the only thing that you need to know
in order to create an account with a given currency, is the currency's
debtor ID. In practice however, before you decide to create an account, you
will want to see more information about the currency: the name of the
currency, the currency unit, the exchange rate with other currencies, etc.

<!--more-->

To solve this inconvenience, Swaptacular defines a reliable *decentralized*
way to obtain basic information about Swaptaclar currencies.

## Digital coins

A "digital coin" is a special kind of link, that points to a document which
describes a particular Swaptacular currency. There are 3 important
specifications which deal with this topic:

- [The "swpt" URI Scheme](/public/docs/swpt-uri-scheme.pdf)

  This specification defines how Swaptacular currencies and Swaptacular
  accounts can be represented by [Uniform Resource Identifiers
  ](https://en.wikipedia.org/wiki/Uniform_Resource_Identifier) (URI).
  
  For example, the URI `swpt:1234` represents the Swaptacular currency with
  debtor ID 1234; and the URI `swpt:1234/example-account` represents some
  random account with that currency.

- [Digital Coins in Swaptacular](/public/docs/digital-coin-urls.pdf)

  This specification defines all the nitty-gritty details of how digital
  coins work in Swaptacular.

  For example, the digital coin `https://example.com/foo#swpt:1234` tells
  that the document that describes the `swpt:1234` currency, can be found at
  URL `https://example.com/foo`.

  Note that any information received via a random `https://` connection can
  not be considered 100% trustworthy for financial applications. Therefore,
  the obtained information must always be verified prior to receiving
  payments to a newly created account.

  By explicitly including the debtor ID in the digital coin (notice the
  `#swpt:1234` thing at the end), the obtained information can be verified
  automatically, without requiring any further actions from the user.

- [CoinInfo JSON Documents](/public/docs/coin-info-documents.pdf)

  This specification defines one of the standard document formats
  ([JSON](https://en.wikipedia.org/wiki/JSON)-based) that can be used for
  describing Swaptacular currencies. Note that, if need be, other document
  formats may also be standardized in the future.

  For example, the following file:
  
        {
          "type": "CoinInfo",
          "debtorName": "Example Currency",
          "summary": "This is an example currency.\n",
          "debtorHomepage": {
            "uri": "https://www.example-currency.com/"
          },
          "amountDivisor": 100,
          "decimalPlaces": 2,
          "unit": "USD",
          "peg": {
            "type": "Peg",
            "exchangeRate": 1,
            "debtorIdentity": {
              "type": "DebtorIdentity",
              "uri": "swpt:666"
            },
            "latestDebtorInfo": {
              "uri": "https://www.usa.gov/USD"
            },
            "display": {
              "type": "PegDisplay",
              "amountDivisor": 100,
              "decimalPlaces": 2,
              "unit": "USD"
            }
          },
          "debtorIdentity": {
            "type": "DebtorIdentity",
            "uri": "swpt:1234"
          },
          "latestDebtorInfo": {
            "uri": "https://example.com/foo"
          },
          "revision": 1
        }

  describes a currency named "Example Currency", which is pegged to the US
  dollar with 1-to-1 exchange ratio (the URIs and debtor IDs are made-up).

  Note that the document that describes a given currency will most likely be
  hosted on a server operated by the [debtors agent node](/overview/) which
  is responsible for managing the currency. A limited number of well-known
  currencies (like the USD), will have well-known debtor IDs, and their
  descriptions will be immutable and hosted on well-known locations.

## Sharing digital coins

Because Swaptacular's digital coins really are just URLs, and therefore can
be easily copied, they are more similar to **photographs of physical
coins**, than to the physical coins themselves: Having a photograph of a
physical coin does not make you an owner of a coin, but allows you to
recognize this kind of coins when somebody wants to pay you with them.

To make the "photograph" metaphor complete, Swaptacular's digital coins will
most often will presented as [QR
codes](https://en.wikipedia.org/wiki/QR_code). Once you have scanned the
digital coin (the QR code) of a given currency with your phone, you can
create an account with that currency, and you can accept and make payments
in it.

Note however, that when a stranger introduces you to a new digital coin, the
dangers are similar to the dangers when a stranger introduces you to an
unknown foreign currency: You could be tricked by fraudsters, and be paid
with worthless coins.

For this reason, it is generally a bad idea to share digital coins via
unauthenticated email messages. Instead, the recommenced way of sharing
digital coins is to scan their QR codes directly from paper, or from a
computer screen. This gives a physical context to the act of receiving very
important information, from a potentially untrustworthy source.