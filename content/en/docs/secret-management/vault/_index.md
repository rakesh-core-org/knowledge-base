---
title: "Vault"
weight: 10
description: >
  Secret Management
categories: [devops]
tags: [Secrets]
---

Why we need a vault? what problem does it solve 
similar solutions 
  keypass 
paid
installation method 

  vault dedicated --> hosted service by HCP 
  install vault CLI client and server or just client  
Access via UI, HTTP API, CLI 

vault - various pluggable components 

backup method 

HA method 

ngrok --connect to database testing 

workload become ephermeral and short lived -- long-lived static creds makes security threat 


tokens, API keys, passwords, certificates

vault token associated with client-policy 

policy is path-based

policy rules --> contains actions 

Plus point of vault: 
  secure secret storage -- consul 
  dynamic secret 
  data encryption 
  leasing and renewal 
  revoke provided secrets 
  
  

KV store 
  write and read
  update and delete 
  restore 


database password rotation 
  postgresql
  mongodb 
  

