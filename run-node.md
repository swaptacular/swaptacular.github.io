---
layout: page
title: Run your own node
---

Like the Internet, Swaptacular is decentralized by nature. Companies
and individuals can run their own Swaptacular servers and connect them
to servers operated by others. [There are several types of
nodes](/overview/), each serving a different role in the network:

* creditors agent nodes
* accounting authority nodes
* debtors agent nodes

If you have decided to run your own Swaptacular node, there are
several ways to do so. The best approach depends on your goals. Below
are the most common scenarios, listed from the simplest to the most
advanced:


## Let someone else run a creditors agent node for you

Running your own *creditors agent node* allows you [to offer automated
currency exchanges to your
users](/2024/07/04/automated-currency-exchanges/). Most importantly,
it enables you to collect a small fee from each completed exchange.

The easiest way to get started is to let `swaptacular.org` run the
node for you. We are committed to keeping this service free, and we
rely on donations to support it.


## Run a creditors agent node yourself

If you prefer not to depend on a third party, you can [deploy a
creditors agent node on your own Kubernetes
cluster](https://github.com/swaptacular/swpt-k8s-config). We strive to
make this option as simple and straightforward as possible.

Once your creditors agent node is up and running, you should connect
it to at least one [accounting authority node from the public
list](#public-list-of-accounting-authority-nodes).


## Run an accounting authority node

Running your own *accounting authority node* helps ensure the
long-term reliability of the digital currencies it manages. The
recommended approach is to [deploy it on your own Kubernetes
cluster](https://github.com/swaptacular/swpt-k8s-config). In most
cases, you will also want to run a *creditors agent node* and a
*debtors agent node*, either on the same cluster or on separate ones.

Once your accounting authority node is operational, please contact us
so we can add it to the [public list of accounting authority
nodes](#public-list-of-accounting-authority-nodes). This will allow
others to discover your node and — subject to your approval — connect
to it.

**Note:** To create a root SSL certificate for your accounting
authority node, you must first obtain a unique *accounting authority
prefix*. The currently recommended method is to randomly select a
hexadecimal number between `0x10000000` and `0x1000ffff` that does not
match any existing *serialNumber* in the public list.


## Public list of accounting authority nodes

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>serial&#8203;Number</th>
      <th>Added</th>
      <th>Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="/public/infobundles/example.zip">Example node</a></td>
      <td><code>10000000</code></td>
      <td>2026-04-12</td>
      <td>out of service</td>
    </tr>
  </tbody>
</table>

**Note:** Click on the name of the node to download its [info-bundle
file](https://github.com/swaptacular/swpt_ca_scripts).


<div>
  <h2>Want to know more?</h2>
  <ul class="related-posts">
  {% for node in site.tags.intro %}
    {% unless node.tags contains 'overview' %}
      <li>
        <h3>
          <a href="{{ node.url }}">
            {{ node.title }}
          </a>
          <small>{{ node.date | date_to_string }}</small>
        </h3>
      </li>
    {% endunless %}
  {% endfor %}
  </ul>
</div>
