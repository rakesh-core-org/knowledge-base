---
title: "Openstack"
weight: 3
---

## Why openstack is complicated

We are seeing openstack as a whole single (project)package, but in reality it is not.
On the other hand, if you think openstack is a collection of multiple projects, then you are right and wrong too. OOPS!! Don't believe me? wait. 
    
Forget everything! Think Openstack like a framework, it integrates multiple projects(Already existing) together. If you are familiar with microservices, openstack will look similar to that. Nova, keystone, neutron ironic, glance were all microservices, each has its own scope of roles and responsibility. 

## How to approach neutron

Lets take an example of Neutron project. How would you approach it? Directly reading neutron documentation? Then you will be in a rabbit hole. Good thing about openstack docs is its clear, bad thing is its very clear :). 

If you want to start openstack neutron, please don’t start with neutron. Neutron is just a wrapper for many packages. Before that you need to understand atleast basics of below

- OSI model
- Vlan, vxlan
- Subnet
- DHCP(dnsmasq)
- DNS
- Network Switches
- Layer 3
- Overlay tunnel
- Network namespaces
- Mechanism drivers
    - Linux bridge 
    - OVN
- Type driver
    - vlan
    - vxlan
- QOS
- Network Protocols
- keepalived (HA for network node)

and much more.

Understanding these is important, because you cannot deploy openstack alone in any organization. This requires support from your network team, storage team, Hardware team and much more. In order to give/ask for requirement itself you need to understand each terminology and underlying technology. Orelse forget about fixing the issue, we don't even know where the issue it. 

#Openstack #Devops #metal #MAAS #networking #virtualization
Follow me to learn more on openstack related topics 

## How about vendor support?

Many companies are offering openstack support for deploying and managing but they are too costly. Every vendor follows their own way of deploying and managing openstack. Like Redhat customized the opensource openstack and they will deploy their own customized version of openstack (It means vendor-lock-in). Vexxhost is an another vendor who forces to deploy openstack through their own opensource deployment method Atmosphere. Nowhere in openstack's official documentation mentioned about atmosphere.(It means vendor-lock-in). 

Once you allow vendor to manage your private cloud, you determine the initial quotation, post then vendor determines the price for each task. You will not be a position to negotiate.

TLDR: if you want to deploy openstack then you want to learn a lot and manage it within your organization is the best way still its the most complicated way and the most time consuming way. If you are lucky you will get a good vendor support. 

## Why most of openstack deployment failing?

Openstack provides different options to choose from, inorder to pick the correct option we need to know what each does. Lets take an example of mechanism drivers, we can enable linux bridge, open vswitch and many more. we can choose one or many. Point here is without knowing what each project does how to pick the right one for your project?

Without understanding the basics, if you are lucky enough you can deploy openstack. On day 2 your ticking bomb starts it can explode at anytime. 

What will you do if new VM is not launching?
Where will you check if instance is not getting IP? 

In next 6 months openstack will release a new version, how will you upgrade each openstack projects?

## Basics of openstack 

    Virtualization 
    Storage 
    Networking 
    Message queue 
    database 
    Operating system 
    ntp


## How to manage openstack in a better way

1. Attend/Watch openinfra meet.
1. Implement monitoring/logging solution.

Follow me


## Supporting Infrastructure applications

 - HAProxy
 - keepalived
 - rabbitmq
 - mysql

## How to get deploy openstack 

You can deploy openstack using many different methods. For the first time if you want to learn, then manual deployment is the best approach, so that you can understand what services you are deploying and how its configured. For deploying production grade you can pick any stable available deployment method mentioned in the docs. 

Makesure the choosen deployment method is capable enough to deploy the necesary projects which you need.

If your employees have enough knowledge on ansible, then its better to pick openstack-ansible.
If your employees have enough knowledge on kubernetes, then pick openstack-helm. Don't pick and lock with unknown deployment method. 

Downside could be, openstack-ansible may be slow to execute playbooks if your infrastructure grows and if you have not using tags properly. Due to this you don't need to switch the deployment method which you are not comfortable with.

