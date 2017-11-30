---
layout: page
title: defaulttitle
---


# ZooKeeper Quota's Guide
{:.no_toc}

### A Guide to Deployment and Administration
{:.no_toc}
---
* TOC
{:toc}
---

## Quotas {#zookeeper_quotas}

ZooKeeper has both namespace and bytes quotas. You can use the ZooKeeperMain class to setup quotas.
ZooKeeper prints _WARN_ messages if users exceed the quota assigned to them. The messages
are printed in the log of the ZooKeeper.

**

    $ bin/zkCli.sh -server host:port**

The above command gives you a command line option of using quotas.

### Setting Quotas

You can use
_setquota_ to set a quota on a ZooKeeper node. It has an option of setting quota with
-n (for namespace)
and -b (for bytes).

The ZooKeeper quota are stored in ZooKeeper itself in /zookeeper/quota. To disable other people from
changing the quota's set the ACL for /zookeeper/quota such that only admins are able to read and write to it.

### Listing Quotas

You can use
_listquota_ to list a quota on a ZooKeeper node.

### Deleting Quotas

You can use
_delquota_ to delete quota on a ZooKeeper node.


