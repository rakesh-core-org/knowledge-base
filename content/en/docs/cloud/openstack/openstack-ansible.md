---
title: "Openstack Ansible OSA"
weight: 1
description: >
  Deploy openstack using openstack ansible
categories: [Cloud]
tags: [PrivateCloud]
---

### Possible deployment options 
https://www.openstack.org/software/project-navigator/deployment-tools

### Other vendow supported deployments 
https://github.com/vexxhost/atmosphere
https://docs.redhat.com/en/documentation/red_hat_openstack_services_on_openshift/18.0

You can directly deploy in the host or deploy in container LXC(makesure you have enough knowledge before using it. orelse you are unwantedly adding another layer of complexity)

### Pre-requirements
1. Go for it, if you have knowledge in Ansible
1. Ansible controller node
1. installation method cannot changed in future


### virtual environment 
1. for each project python virtual environment is created

### Document links naming format
Openstack-ansible-landing      https://docs.openstack.org/openstack-ansible/latest/
For a specific version         https://docs.openstack.org/openstack-ansible/zed/


Deployment direct link https://docs.openstack.org/project-deploy-guide/openstack-ansible/latest/
For a specific version https://docs.openstack.org/project-deploy-guide/openstack-ansible/2024.1/

                       https://docs.openstack.org/project-deploy-guide/kolla-ansible/2024.2/


### Github repository structure

https://github.com/openstack/openstack-ansible/tree/master  -- Clone or fork it. unmaintained branches will be deleted
    bootstraps roles/collections/
    copies sshkeys /creates if not exists
    installs certain system packages 
    configures openstack-ansible binary
In docs they haven't specified much on what this script is doing 


https://github.com/openstack/openstack-ansible-plugins


https://github.com/openstack/openstack-ansible-os_nova
https://github.com/openstack/openstack-ansible-os_horizon


All roles specific configurations were available in https://docs.openstack.org/project-deploy-guide/openstack-ansible/latest/configure.html#openstack-service-roles

https://docs.openstack.org/openstack-ansible-os_cinder/latest/
https://docs.openstack.org/openstack-ansible-os_keystone/latest/



### Lets modify openstack_user_config.yml as per our need 
