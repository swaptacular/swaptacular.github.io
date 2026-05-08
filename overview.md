---
layout: page
title: Learn more
order_number: 1
---

The Swaptacular project consists of three main parts:

1. A decentralized network architecture.
2. A set of interoperability protocols.
3. Reference implementations for the interoperability protocols.

Together, these parts define how independent organizations can operate
interoperable currency and payment systems without relying on a
centralized ledger.


## The network architecture

In Swaptacular's network architecture, there are five types of nodes:

1. **Accounting Authorities** maintain account balances and form the
   backbone of the network.
2. **Currency Issuers** create currencies and issue money into
   circulation. In Swaptacular, they are also called *debtors*.
3. **Debtors Agents** connect currency issuers to accounting
   authorities. They may also act as guarantors for debtors.
4. **Currency Holders** make and receive payments. In Swaptacular,
   they are also called *creditors*.
5. **Creditors Agents** connect currency holders to accounting
   authorities. They may also facilitate [automated currency exchanges
   between creditors](/2024/07/04/automated-currency-exchanges/).

<div class="message">
  <img src="/images/swpt_basic_network.svg" alt="Swaptacular Basic Network">
</div>

The diagram above shows the simplest possible Swaptacular network.
Note that different network nodes (accounting authorities, creditors
agents, debtors agents) can be operated by different organizations or
individuals. Thus, much like the Internet itself, **Swaptacular's
network is decentralized by design.**

A key point is that one *creditors agent* can connect *currency
holders* to many different *accounting authorities*. The following
diagram illustrates the connections that can exist between different
types of nodes in a real-world network:

<div class="message">
  <img src="/images/swpt_complex_nework.svg" alt="Swaptacular Real-world Network">
</div>

This second diagram shows two different creditors agents, each
connecting currency holders to multiple accounting authorities. It
also shows two debtors agents connecting currency issuers to the same
accounting authority.


## Interoperability protocols

At the core of Swaptacular's network architecture is the [Swaptacular
Messaging Protocol](/public/docs/protocol.pdf), which governs the
communication between accounting authorities, debtors agents, and
creditors agents.

The protocol uses [two-phase
commit](https://en.wikipedia.org/wiki/Two-phase_commit_protocol) to
coordinate payments reliably throughout the network. This makes it
possible to implement automated currency exchanges in the spirit of
[Circular Multilateral Barter](/public/docs/cmb-general.pdf), thereby
reducing reliance on dominant reserve currencies.

In order to allow currency holders to use a client application of
their choice, Swaptacular recommends creditors agents to follow the
[Payments Web API Specification](/public/docs/swpt_creditors/redoc.html).

Because interchangeability between currency-issuing applications is
less critical, Swaptacular does not currently define a standard
*Issuing Web API*.

Swaptacular takes interoperability between independent implementations
seriously and provides precise, clear, and concise specifications for
every important aspect of the system:

* [Swaptacular Messaging Protocol](/public/docs/protocol.pdf)
* [JSON Serialization for the Swaptacular Messaging
  Protocol](/public/docs/protocol-json.pdf)
* [STOMP Message Transport for the Swaptacular Messaging
  Protocol](/public/docs/swpt-stomp.pdf)
* [Swaptacular SSL/TLS Certificates](/public/docs/swpt-certificates.pdf)
* [RootConfigData JSON Documents](/public/docs/root-config-data.pdf)
* [The "swpt" URI Scheme](/public/docs/swpt-uri-scheme.pdf)
* [Digital Coins in Swaptacular](/public/docs/digital-coin-urls.pdf)
* [CoinInfo JSON Documents](/public/docs/coin-info-documents.pdf)
* [Payment Requests and Transfers in
  Swaptacular](/public/docs/payment-requests.pdf)
* [PR-zero Payment Request Documents](/public/docs/pr0-documents.pdf)
* [Payments Web API Specification](/public/docs/swpt_creditors/redoc.html)


## Reference implementations

* [Accounting Authority](https://github.com/swaptacular/swpt_accounts)
* [Debtors Agent](https://github.com/swaptacular/swpt_debtors)
* [Creditors Agent](https://github.com/swaptacular/swpt_creditors)
* [Automated Currency Exchanges](https://github.com/swaptacular/swpt_trade)
* [Service that manages OAuth2 login and consent](https://github.com/swaptacular/swpt_login)
* [Currency Issuer UI](https://github.com/swaptacular/swpt_debtors_ui)
* [Currency Holder UI](https://github.com/swaptacular/swpt_creditors_ui)
* [Swaptacular Web API reverse proxy](https://github.com/swaptacular/swpt_apiproxy)
* [STOMP protocol client and server](https://github.com/swaptacular/swpt_stomp)
* [Managing Swaptacular certificate authorities](https://github.com/swaptacular/swpt_ca_scripts)

All reference implementations aim to:

1. Be correct.
2. Remain as simple as possible.
3. Be useful in real-world deployments.
4. Demonstrate that horizontally scalable implementations are indeed
   possible.

For testing, you can [install and run a full set of Swaptacular
network nodes on your
laptop](/2024/07/07/under-the-hood-running-everything-together/).

You can also **[deploy Swaptacular to Kubernetes
clusters](/2025/09/18/ready-for-production/)**.

<div class="lead message">
  👉 <a href="/show-me/">Show me</a> Swaptacular in action!
</div>
