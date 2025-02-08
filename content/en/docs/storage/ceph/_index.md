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


### Architecture 




## installation


--skip-monitoring-stack
https://docs.ceph.com/en/squid/cephadm/services/monitoring/#disabling-monitoring

Ceph Dashboard is now available at:

	     URL: https://ceph-01:8443/
	    User: admin
	Password: admin@123

Enabling client.admin keyring and conf on hosts with "admin" label
Saving cluster configuration to /var/lib/ceph/a435810c-a656-11ef-be9c-555e7832e56b/config directory
Enabling autotune for osd_memory_target
You can access the Ceph CLI as following in case of multi-cluster or non-default config:

	sudo /usr/sbin/cephadm shell --fsid a435810c-a656-11ef-be9c-555e7832e56b -c /etc/ceph/ceph.conf -k /etc/ceph/ceph.client.admin.keyring

Or, if you are only running a single cluster on this host:

	sudo /usr/sbin/cephadm shell 

Please consider enabling telemetry to help improve Ceph:

	ceph telemetry on

For more information see:

	https://docs.ceph.com/en/latest/mgr/telemetry/

Bootstrap complete.


## For extending new ceph host 

ceph cephadm get-pub-key

Get the public key and put it in the authorized_keys of root user

