---
title: "Kubespray"
weight: 2
description: >
  Deploy kubernetes cluster
---

sudo apt install python3-pip
pip install ruamel-yaml --break-system-packages

pip install ansible-core==2.16.13 --break-system-packages
pip install ansible==9.12.0 --break-system-packages


ansible-playbook -i inventory/mycluster/hosts.yml cluster.yml -b -v --ask-become-pass -e kubeconfig_localhost=true

If kubeconfig_localhost: false then login to one of the control plane and download the file /etc/kubernetes/admin.conf

in server value replace 127.0.0.1 by actual IP address of the control plane.


export KUBECONFIG=/home/rakesh/.kube/corecluster.yaml