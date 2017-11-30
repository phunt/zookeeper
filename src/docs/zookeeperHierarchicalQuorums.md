---
layout: page
title: defaulttitle
---


# Introduction to hierarchical quorums
{:.no_toc}

---
* TOC
{:toc}
---

This document gives an example of how to use hierarchical quorums. The basic idea is
very simple. First, we split servers into groups, and add a line for each group listing
the servers that form this group. Next we have to assign a weight to each server.

The following example shows how to configure a system with three groups of three servers
each, and we assign a weight of 1 to each server:
{% highlight c linenos %}
{% raw %}

    group.1=1:2:3
    group.2=4:5:6
    group.3=7:8:9

    weight.1=1
    weight.2=1
    weight.3=1
    weight.4=1
    weight.5=1
    weight.6=1
    weight.7=1
    weight.8=1
    weight.9=1
{% endraw %}
{% endhighlight %}

When running the system, we are able to form a quorum once we have a majority of votes from
a majority of non-zero-weight groups. Groups that have zero weight are discarded and not
considered when forming quorums. Looking at the example, we are able to form a quorum once
we have votes from at least two servers from each of two different groups.


