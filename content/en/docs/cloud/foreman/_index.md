---
title: "Foreman"
weight: 2
description: >
  Installation steps of foreman
---

## About foreman

- Foreman UI
- smart proxy 
- pupet server 
- tftp
- DNS
- DHCP 

## pre-requirement
- puppet 6 or later

Executing: foreman-rake upgrade:run
  Success!
  * Foreman is running at https://foreman-controller-01.rakesh.core
      Initial credentials are admin / UWRYhVwYNXAKdGTw
  * Foreman Proxy is running at https://foreman-controller-01.rakesh.core:8443




Reference guide: [Foreman installation](https://theforeman.org/manuals/3.10/index.html#:~:text=2.1-,Installation,-2.2%20Puppet%20Management)



Initial admin password will be in `/etc/foreman-installer/scenarios.d/foreman-answers.yaml`


`echo insecure >> ~/.curlrc`

Add this if it shows certificate error while doing curl 


`lxc launch ubuntu:noble --vm foreman -c limits.cpu=8 -c limits.memory=16GiB`




### Provisioning templates 

Preseed --> ubuntu 
kickstart --> RHEL
AutoYaST --> suse

#### Description of Foreman Provisioning Templates
Foreman provides three types of provisioning templates to automate the installation process for different Linux distributions:

* **Preseed**: A pre-configured template for Ubuntu installations, which simplifies the installation process by automatically answering all prompts and configuring the system according to your needs.
* **Kickstart**: A templating engine specifically designed for RHEL (Red Hat Enterprise Linux) installations. Kickstart scripts enable automated unattended installation of RHEL systems, reducing the time and effort required for setup.
* **AutoYaST**: Foreman's AutoYaST template is a powerful tool for automating SUSE Linux Enterprise Server (SLES) installations. It provides an efficient way to configure and deploy SLES systems without manual intervention.

These provisioning templates significantly streamline the process of setting up new servers, reducing administrative overhead and ensuring consistency across your infrastructure.

