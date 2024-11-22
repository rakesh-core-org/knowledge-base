---
title: "Openstack"
weight: 1
description: >
  Private cloud
categories: [Cloud]
tags: [PrivateCloud]
---



Each project will have its own database 
3 API layer 
its own backend system 
one or more services running 

## Setup 

```
lxc launch ubuntu:noble --vm openstack-ctl-01 -c limits.cpu=8 -c limits.memory=16GiB

lxc launch ubuntu:noble --vm openstack-data-01 -c limits.cpu=8 -c limits.memory=16GiB

lxc launch ubuntu:noble --vm openstack-hypervisor-01 -c limits.cpu=8 -c limits.memory=16GiB

lxc launch ubuntu:noble --vm openstack-mgnt-01 -c limits.cpu=8 -c limits.memory=16GiB

lxc launch ubuntu:noble --vm openstack-deployment -c limits.cpu=8 -c limits.memory=16GiB
```

