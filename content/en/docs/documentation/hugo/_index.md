---
title: "Hugo"
weight: 1
description: >
  Documentation is not additional task, its part of the job
categories: [Devops]
tags: [Documentation]
---


For installing hugo

https://github.com/gohugoio/hugo/releases/tag/v0.138.0

rakesh@rakesh-ws:/tmp$ wget https://github.com/gohugoio/hugo/releases/download/v0.138.0/hugo_extended_0.138.0_linux-amd64.deb
rakesh@rakesh-ws:/tmp$ sudo dpkg -i hugo_extended_0.138.0_linux-amd64.deb 

rakesh@rakesh-ws:/tmp$ hugo version
hugo v0.138.0-ad82998d54b3f9f8c2741b67356813b55b3134b9+extended linux/amd64 BuildDate=2024-11-06T11:22:34Z VendorInfo=gohugoio

rakesh@rakesh-ws:/data/knowledge-base$ hugo serve