---
title: "Foreman"
weight: 2
description: >
  Installation steps of foreman
---


Reference guide: [Foreman installation](https://theforeman.org/manuals/3.10/index.html#:~:text=2.1-,Installation,-2.2%20Puppet%20Management)



Initial admin password will be in `/etc/foreman-installer/scenarios.d/foreman-answers.yaml`


`echo insecure >> ~/.curlrc`

Add this if it shows certificate error while doing curl 


`lxc launch ubuntu:noble --vm foreman -c limits.cpu=8 -c limits.memory=16GiB`