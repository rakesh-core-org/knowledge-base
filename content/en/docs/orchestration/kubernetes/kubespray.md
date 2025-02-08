---
title: "Kubespray"
weight: 2
description: >
  Deploy kubernetes cluster
---


```
sudo apt install python3-pip
pip install ruamel-yaml --break-system-packages

pip install ansible-core==2.16.13 --break-system-packages
pip install ansible==9.12.0 --break-system-packages



declare -a IPS=(192.168.122.4 192.168.122.5 192.168.122.6 192.168.122.7)
CONFIG_FILE=inventory/corecluster/hosts.yml python3.12 contrib/inventory_builder/inventory.py ${IPS[@]}
```

vim ~/kubespray/inventory/corecluster/group_vars/all/containerd.yml

```
containerd_registries_mirrors:
 - prefix: container-registry.rakicloud.org
   mirrors:
    - host: https://container-registry.rakicloud.org
      capabilities: ["pull", "resolve"]
      skip_verify: false

# containerd_max_container_log_line_size: -1

containerd_registry_auth:
  - registry: container-registry.rakicloud.org
    username: admin
    password: Harbor12345
```


ansible-playbook -i inventory/corecluster/hosts.yml cluster.yml -b -v --ask-become-pass -e kubeconfig_localhost=true

If kubeconfig_localhost: false then login to one of the control plane and download the file /etc/kubernetes/admin.conf

in server value replace 127.0.0.1 by actual IP address of the control plane.


export KUBECONFIG=/home/rakesh/.kube/corecluster.yaml

# Post deployment 

> In all kubernetes host, add tls verify to skip. this step mabe optional if you have a valid certificate. Or figure out how to pass this via kubespray

`sudo vim /etc/containerd/config.toml`

```
[plugins."io.containerd.grpc.v1.cri".registry.configs."container-registry.rakicloud.org".tls]
        insecure_skip_verify = true

```
`sudo systemctl restart containerd`