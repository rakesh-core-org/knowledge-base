---
title: "KVM"
weight: 5
description: >
  KVM
categories: [Cloud]
tags: [nocloud]
---


vSphere offers a maximum of 12TB of RAM per host with a maximum of 64 hosts per cluster


# Create virtual machine using command
virt-install \
-n k8s4 \
--description "kubernetes worker node" \
--os-variant=ubuntu24.04 \
--ram=8224 \
--vcpus=4 \
--disk path=/var/lib/libvirt/images/k8s4.img,bus=virtio,size=100 \
--graphics none \
--location /data/ISO/ubuntu-24.04.1-live-server-amd64.iso,kernel=casper/vmlinuz,initrd=casper/initrd \
--network network=default \
--extra-args='console=tty0 console=ttyS0,115200n8 serial autoinstall ds=nocloud' \
--cloud-init user-data=/data/knowledge-base/content/en/docs/virtualization/cloud-init.yaml