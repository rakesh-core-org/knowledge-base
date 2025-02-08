---
title: "Installation"
weight: 1
description: >
  Ceph multi-node installation
categories: [devops]
tags: [Storage]
---



## installation methods.

1. cephadm (recommended and official method)

## System requirements [Reference](https://docs.ceph.com/en/squid/cephadm/install/#requirements)
1. podman/docker -- not all versions are supported
1. raw storage 
1. Make sure IP address is static and have FQDN 



Install cephadm via repository manager https://download.ceph.com/debian-squid/

```
wget -q -O- 'https://download.ceph.com/keys/release.asc' | sudo apt-key add -
sudo apt-add-repository 'deb https://download.ceph.com/debian-reef/ jammy main'
apt-get update
apt-get install cephadm
cephadm version
```

```
apt install ceph-common
```
Reference: https://docs.ceph.com/en/latest/install/get-packages/

## Bootstrap [reference](https://docs.ceph.com/en/squid/cephadm/install/#running-the-bootstrap-command)

`cephadm bootstrap --mon-ip *<mon-ip>* --ssh-user core`
 --ssh-private-key 
 --ssh-public-key
--cluster-name
--skip-monitoring-stack

configuration directory: /etc/ceph 


### Ceph cli

cephadm shell--> bash shell in a container (contains all ceph packages, not on the host)


[converting a host to admin](https://docs.ceph.com/en/squid/cephadm/install/#adding-hosts)

`ceph orch host label add *<host>* _admin`


[remove a host](https://docs.ceph.com/en/squid/cephadm/host-management/#removing-hosts)

ceph orch host drain *<host>*
ceph orch osd rm status
ceph orch host rm <host>

Incase of offline server, remove forcefully

ceph orch host rm <host> --offline --force

[maintenance](https://docs.ceph.com/en/squid/cephadm/host-management/#maintenance-mode)

ceph orch host maintenance enter <hostname> [--force] [--yes-i-really-mean-it]
ceph orch host maintenance exit <hostname>


## ssh key management
ceph cephadm generate-key
ceph cephadm get-pub-key
ceph cephadm clear-key

ceph config-key set mgr/cephadm/ssh_identity_key -i <key>
ceph config-key set mgr/cephadm/ssh_identity_pub -i <pub>


to reload manager daemon --> `ceph mgr fail `

ceph cephadm set-user <user>  --> default is root 



## list all attached devices 

ceph orch device ls 
