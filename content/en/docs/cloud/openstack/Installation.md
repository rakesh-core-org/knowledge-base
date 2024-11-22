---
title: "Multi-node installation"
weight: 1
description: >
  Lets install openstack multinode installation
categories: [Cloud]
tags: [PrivateCloud]
---

Install Dalamation release 

### Infrastructure configured

|           | controller node | compute node | block storage|object storage|
|----------|----------|----------|----------------------|----------------|
| Storage  | 100GB  | 500GB  |500 GB|500GB|
| Memory   | 8 GB  | 16 GB  |8 GB|8GB|
| vcpu      | 8     | 8     |4|4|
|Network interface| 1   |   1|1|1|


### Pending

Auto add DNS without modifying hosts file
#### Configure static ip address in kvm

[Reference](https://www.cyberciti.biz/faq/linux-kvm-libvirt-dnsmasq-dhcp-static-ip-address-configuration-for-guest-os/)

```
virsh net-edit default
virsh net-destroy default
virsh net-start default
```

Go for a turn-off and start it back

ssh core@openstack-controller-01.rakesh.core

Add host entry in all nodes 

`sudo vim /etc/hosts`

```
192.168.122.10 	openstack-controller-01	openstack-controller-01.rakesh.core
192.168.122.20	openstack-compute-01	openstack-compute-01.rakesh.core
192.168.122.30	openstack-block-storage-01	openstack-block-storage-01.rakesh.core
192.168.122.40	openstack-deployment	openstack-deployment.rakesh.core
```

ssh core@openstack-controller-01.rakesh.core
ssh core@openstack-compute-01.rakesh.core
ssh core@openstack-block-storage-01.rakesh.core

### Disable firewall


Install NTP packages in controller node 
add allow for the specified subnet

Install NTP package in other nodes
comment out the default ntp pool
restart the ntp service


### validate
chronyc sources


### install mysql
change the bind address 
restart the service 
configure root password 


## install rabbitmq

enable management

sudo rabbitmq-plugins enable rabbitmq_management

### install memcached


## install etcd (not installing)

centralized store for configuration management 
service discovery 
elect leader 

## openstack services 

### keystone service 

install openstack client

sudo apt  install python3-openstackclient