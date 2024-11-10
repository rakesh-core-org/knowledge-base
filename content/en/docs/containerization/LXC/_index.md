---
title: "LXC"
weight: 2
description: >
  Linux containers
categories: [devops]
tags: [containerization]
---

Linux containers are light weight containers, whereas docker is application container.
LXC were very useful  for local testing and development.

## About lxd

LXD is the utility through which we install and manage LXC

## Install LXC via snap

`snap install lxd`

## For listing all available images in repository

`lxc image list images:`

## Launch an LXC 

`lxc launch ubuntu:focal --vm foreman-001`
`lxc launch ubuntu:noble --vm lxc-001`

lxc launch images:ubuntu/24.04/desktop ubuntu --vm -c limits.cpu=4 -c limits.memory=8GiB --console=vga

## Connect to lxc container 

`lxc exec foreman-001 -- bash`

login and allow permit root login here 
vim /etc/ssh/sshd_config

enable password authentication here `/etc/ssh/sshd_config.d/60-cloudimg-settings.conf`

restart sshd service 

change root password 

## Set limits for container 

`lxc profile set default limits.memory 2GB`

## show profile config 

`lxc profile show default`


## Forward port from container to host (similar to docker)

`lxc network forward port add lxdbr0 <HOSTIP> tcp <HOSTPORT> <CONTAINER_IP> <CONTAINERPORT>`


## describing all opened/used host ports 

`lxc network forward show lxdbr0 <HOSTIP>`


##  Rename a container 

first stop the running container and move 

lxc move {current-container-name} {new-container-name}


## Add storage drive to lxc container 

`lxc config device add ceph-002 cephdrive01 disk source=/dev/sdb path=/dev/sdb`

## For removing the drive 

`lxc config device remove ceph-002 cephdrive01`