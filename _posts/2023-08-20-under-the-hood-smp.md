---
layout: post
title: Under the Hood — SMP
description: >
  Explains the basics of the Swaptacular Messaging Protocol.
author: Evgeni Pandurski
tags: [under-the-hood]
published: false
---

In [a previous post](/2023/08/03/under-the-hood-message-transport/) I
explained how peers in Swaptacular’s network use the STOMP message transport
protocol, to send Swaptacular Messaging Protocol messages to each other.

In this post will try to explain how the [Swaptacular Messaging
Protocol](/public/docs/protocol.pdf) (SMP) works.

<!--more-->

TODO: Explain debtor_id, creditor_id, account_balance.

<div class="message">
  <img src="/images/smp-configure-account.svg"
       alt="Creating an account, and then deleting it">
</div>

TODO: Explain config_data, negligible_amount, scheduled_for_deletion.

<div class="message">
  <img src="/images/smp-commit-transfer.svg"
       alt="Creating an account, and then deleting it">
</div>

TODO: Explain coordinator_type, coordinator_request_id, account identifiers,
min/max_lock_amount, lock_amount, transfer_note, committed_amount,
acquired_amount.

TODO: Explain that debtors use the same protocol, but creditor_id is zero
for debtors' accounts.