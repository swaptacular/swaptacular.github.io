---
layout: post
title: Ready for Production!
description: >
  Announces that Swaptacular nodes can be easily deployed to Kubernetes
  clusters.
author: Evgeni Pandurski
tags: [intro]
---

While most of Swaptacular’s components have long been stable and
reliable, orchestrating them to work seamlessly together [is no easy
task](/2024/07/07/under-the-hood-running-everything-together/) —
especially when scalability and high availability come into play. The
challenge intensifies even further given that Swaptacular is a
financial application, with many security-critical admin tasks.

Luckily, [Kubernetes](https://kubernetes.io/) is designed to solve
exactly these kinds of problems!

<!--more-->

After months of learning and tinkering with endless YAML files, I came
up with a flexible [template for deploying Swaptacular nodes to
Kubernetes clusters](https://github.com/swaptacular/swpt-k8s-config).
This template includes detailed step-by-step instructions, enabling
anyone with a good grasp of Kubernetes to deploy their own
[Swaptacular nodes](/overview/) in a production.

> 👉 [Click here for full
> details!](https://github.com/swaptacular/swpt-k8s-config)


**Important note:** [The service responsible for automated currency
exchanges](/2024/07/04/automated-currency-exchanges/) has not yet
reached version 1.0. While major changes are unlikely, some
adjustments — possibly backward-incompatible ones — may still be
necessary. **Edit:** The exchange service has reached version 1.0
(March 28, 2026).
