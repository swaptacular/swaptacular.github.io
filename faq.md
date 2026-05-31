---
layout: page
title: FAQ
order_number: 3
---

## Is Swaptacular similar to barter?

In many ways — yes.

Compared to *direct barter*, Swaptacular is simply less direct.
Instead of exchanging goods or services immediately, participants earn
currency tokens, which they can later use to obtain goods, services,
or other tokens.

The existence of currency tokens allows Swaptacular to implement
[automated currency
exchanges](/2024/07/04/automated-currency-exchanges/), greatly
expanding the possibilities for trade.

<hr>

Compared to *organized barter networks*, where a central operator
manages a common ledger, Swaptacular is more decentralized. In such
systems, the operator controls credit issuance, which can lead to
imbalances when credit is extended more readily to some participants
than to others.

In Swaptacular, there is no single shared ledger. Each business
maintains its own ledger and [extends credit only to trusted
partners](/2022/07/05/swaptaculars-network-of-trust/). This reduces
dependence on centralized credit allocation and allows businesses to
join and trade more independently.

As a result, **the network can grow organically**, scaling to many
thousands of businesses with minimal central administration.

<div class="message">
  Note: In Swaptacular, barter operators that <a href="/run-node/">run
  their own creditors agent nodes</a> can collect a small fee from
  each exchange their node arranges. These exchanges are fully
  automated and require no manual intervention.
</div>


## Is Swaptacular meant only for small businesses?

While Swaptacular is designed with small businesses in mind, *it
scales very well in both participant size and network size.*

In Swaptacular, digital currencies issued by large businesses can be
used and traded just as easily as the currencies issued by small
businesses. Moreover, because the network is decentralized, [large
businesses can deploy their own Swaptacular nodes](/overview/) to
manage the currencies they issue — retaining full control over their
financial and technical infrastructure.

This ability to run currency-managing servers as part of a broader
decentralized network opens up additional possibilities for a wider
range of institutions, including barter operators,
[LETS](https://en.wikipedia.org/wiki/Local_exchange_trading_system)
administrators, commercial banks, municipalities, and states.

We believe Swaptacular can greatly benefit **barter operators**
focused on business-to-business trade, complementing their existing
services with a scalable business-to-customer solution. Operators that
provide a customer-facing digital trade network may gain a significant
competitive advantage as the barter economy evolves.

We also believe Swaptacular can help **LETS administrators** build
more resilient trading communities. Establishing a local exchange
network requires substantial effort, and successful communities often
face governance challenges as they grow. Swaptacular makes this
transition smoother: as communities expand, participants can gradually
rely less on a shared “common currency” and more on participant-issued
currencies.

<div class="message">
  Note: Combined with administrator-maintained
  <a href="{{ site.app_demo.map_url }}" target="_blank">custom maps</a>
  linking to participants’ public profiles or webpages, Swaptacular
  can provide much of the infrastructure needed for an emerging local
  exchange network.
</div>


## What about taxes?

Different jurisdictions may classify Swaptacular transactions
differently and may apply very different tax rules.

However, businesses providing goods and services in exchange for
digital tokens are not a new phenomenon. Gift cards and similar
stored-value instruments have long been used in commerce.

The tax treatment of such transactions is therefore often comparable
to the treatment of **gift card transactions**, although the details
depend on the specific legal and tax framework.

You should consult your accountant or tax advisor to understand how
these transactions are treated in your jurisdiction.


## Is Swaptacular similar to the banking system?

To some extent — yes.

Like Swaptacular, [commercial banks issue their own digital
currencies](/2022/07/03/what-is-a-currency-peg/) (bank deposits),
which holders can transfer to others and exchange for deposits issued
by other banks (via bank transfers).

To facilitate inter-bank exchanges, the central bank maintains a
centralized settlement system that uses bank reserves. Bank reserves
nowadays are usually implemented through a shared ledger operated by
the central bank.

However, the banking system has two important constraints:

* Businesses cannot issue their own currencies directly. Instead, they
  must rely on banks as intermediaries, typically by *borrowing funds
  with interest.*

* The banking system relies on a central bank — a legally privileged
  institution that wields *significant power over the broader
  economy.*

These constraints do not apply to Swaptacular. In some sense, each
issuer in Swaptacular **acts as its own central bank**, with its
currency backed by its ability to produce goods and services. At the
same time, these “central banks” can engage in [automated currency
exchanges](/2024/07/04/automated-currency-exchanges/) among
themselves, without relying on a reserve system for settlement.

<div class="message">
  Note: In Swaptacular, <a href="/2022/07/08/interest-rates-in-swaptacular/">
  issuers of digital currencies can declare an interest rate</a>, but
  the way this works is fundamentally different from how bank loans
  work.
</div>

## Is Swaptacular similar to Bitcoin?

Not really. Digital currencies issued in Swaptacular **do not rely on
a shared cryptographic ledger.**

Bitcoin, like many other cryptocurrencies, maintains a shared ledger.
In Swaptacular, there is no single shared ledger — each business
maintains its own ledger and extends credit only to trusted partners.

By design, Bitcoin issuance is not directly tied to real-world
economic production. In Swaptacular, currency issuance is backed by
the ability to produce goods and services.

To settle a Bitcoin transfer, the transaction must be validated by the
global network. In Swaptacular, currency issuers can deploy their own
Swaptacular nodes to manage their currencies — retaining complete
control over their critical financial infrastructure.

Taken together, this means Swaptacular does not define a global
reserve currency. That is outside its scope. Instead, it relies on
[automated currency
exchanges](/2024/07/04/automated-currency-exchanges/) among many
currencies.

<div class="message">
  Note: It could be argued that there are some architectural
  similarities between Swaptacular and the Bitcoin <em>Lightning
  Network</em>. However, Swaptacular is focused on local
  multi-currency trading networks, rather than a global payment
  infrastructure.
</div>


## Are shared ledgers bad?

Not necessarily.

Shared ledgers can be an extremely effective way to organize economic
exchange, especially within communities whose members broadly agree on
the rules under which the ledger is maintained. Many successful
systems rely on shared ledgers.

However, shared ledgers tend to face growing governance challenges as
they expand.

As new participants join the system, their **economic interests often
diverge** from those of earlier participants. In particular, newer
participants usually favor easier access to credit and liquidity,
while earlier ones tend to favor preserving the value of existing
claims.

Because a shared ledger requires system-wide rules, these conflicts
become increasingly difficult to resolve in a way that satisfies
everyone.

Over time, large shared-ledger systems tend to converge toward one of
two outcomes:

* The system becomes rigid and resistant to adaptation, causing
  participants to gradually abandon it in favor of alternative systems.

* The system keeps expanding by issuing increasing amounts of credit
  to new participants, who in turn often commit part of their future
  productivity to servicing existing claims through interest payments
  or other financial obligations. Over time, this can create dynamics
  similar to those of a pyramid structure, in which the continued
  functioning of the system depends on ongoing expansion.

Depending on how the system is governed, these dynamics can unfold
over years, decades, or even centuries.

Swaptacular avoids these problems by allowing multiple currencies and
credit relationships to coexist and cooperate via [automated currency
exchanges](/2024/07/04/automated-currency-exchanges/), rather than
requiring all participants to rely on a single shared ledger governed
by universal rules.


## Who can run a Swaptacular node?

Anyone can run a Swaptacular node — [the software is free and open
source.]({{ site.github.repo }})

<div class="lead message">
  👉 See how to <a href="/run-node/">run your own node</a>.
</div>
