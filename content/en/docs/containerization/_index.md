---
title: "Containerization"
weight: 1
description: >
  Containertization 
categories: [devops]
tags: [containerization]
---

certain things which i didn't focus before starting container.

# Introduction to containerization
not a technology rather terminology --> group of linux core concepts 

# Why containerization 
  why containers - what problem does it solves?
  isolation (Process/network) --> gives security 
  Resource limiting 
  Environment management(dependencies)
    portability 

# why its only possible to run linux containers in linux --?

windows - also have kernel to run windows containers


# linux Kernel 
GNU General Public License (GPL)
https://www.redhat.com/en/topics/linux/what-is-the-linux-kernel

Kernel (github link)

everything in linux is a file


# difference between kernel and OS 

# what is available in linux kernel

kernel talks to hardware directly 
    memory management 
    process management 
    file system 
    drivers 
    core networking - iptables 
    ...

is it possilbe to run kernel alone in a machine 
    http://www.linuxfromscratch.org/

Operating system 
  Netplan package 
  firewalld package 
  Gnome package 
  service/process management - systemd <--upstart <--sysVinit

Distributions 
  ubuntu
  redhat
  fedora
  centos
  rockylinux

Package format
  deb
  rpm

package manager
  apt
  snap
  DNF 
  zypper

Benifets of package manager
  dependency management 
  version control
  installation/updates/deletion


Service managers 
  systemd
  runtime 
  

unshare 
namespaces 
Isolation
Resource sharing 
cgroups



Application containers/linux containers 


containers - group of features available in linux 

open-platform - not opensource 
containers - isolated environment 

application containers -- alternatives 

build - ship - deploy 