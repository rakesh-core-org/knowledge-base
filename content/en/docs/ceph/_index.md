---
title: "Ceph"
weight: 6
description: >
  Ceph storage
categories: [devops]
tags: [Storage]
---

# Ceph storage cluster

Once ceph storage cluster is deployed we can configure below 
ceph is based on RADOS - Reliable Autonomic Distributed Object Store. which handles storage, distribution and replication of data accross cluster 

        uses CRUSH algorithm - how and where the data is stored
## configurations 

- OSD - > each OSD is backed by  a single storage device
- monitor -> cluster membership, authentication, 
- manager -> provides interface to external monitoring and management system

OSD backend - Bluestore 
        Metadata management with RocksDB(key/value database)

ceph file system runs ceph metadata server 
ceph object storage run ceph rados gateway daemon

Authentication - cephx

Ceph can be used for below scenarios
- object store 
- Block store 
- file system 


monitors - maintains map of cluster (atlease 3 monitors)
        - not heavy cpu usage
managers - state of ceph cluster, storage utilization,performance metrics , dashboard and api (atleast 2 managers required)
        - not heavy cpu usage
OSD - store data, replication, (atleast 3 osd required)
MSD - cpu intensive 