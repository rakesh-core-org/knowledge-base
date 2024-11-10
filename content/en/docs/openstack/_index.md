---
title: "Openstack"
weight: 2
description: >
  Private cloud
categories: [Cloud]
tags: [PrivateCloud]
---


## Setup 

```
lxc launch ubuntu:noble --vm openstack-ctl-01 -c limits.cpu=8 -c limits.memory=16GiB

lxc launch ubuntu:noble --vm openstack-data-01 -c limits.cpu=8 -c limits.memory=16GiB

lxc launch ubuntu:noble --vm openstack-hypervisor-01 -c limits.cpu=8 -c limits.memory=16GiB

lxc launch ubuntu:noble --vm openstack-mgnt-01 -c limits.cpu=8 -c limits.memory=16GiB

lxc launch ubuntu:noble --vm openstack-deployment -c limits.cpu=8 -c limits.memory=16GiB
```

