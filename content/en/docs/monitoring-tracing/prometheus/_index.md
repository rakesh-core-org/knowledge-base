---
title: "Prometheus"
weight: 1
description: >
  Collect metrics 
categories: [devops]
tags: [Monitoring]
---

# Reference architecture 

# Features of prometheus

multi-dimentional data model 
promql 
pull mode over http 
service discovery/static config 

What is a timeseries database? 

## Metrics 
Metrics --> numerical measurement 


## components in prometheus 

1. prometheus server 
2. client libraties 
3. exporters 
4. alert manager 


## Installation of prometheus 


## explanation of prometheus config file 

override global values for each scrape target 


# prometheus rules 


# Use of expression browser 


custom_app_number_of_requests_endpoint1{user="user1", location="Germany"} = 1 
custom_app_number_of_requests_endpoint1{user="user1", location="India", code="200"} = 1 
custom_app_number_of_requests_endpoint1{user="user2", method="POST"} = 2 


count(custom_app_number_of_requests_endpoint1{code="404"})


## metric types 
1. counter 
2. gauge 
3. histogram 
4. summary 

## jobs and instances 

  AUto added lables job, instance 
  https://prometheus.io/docs/prometheus/latest/feature_flags/#extra-scrape-metrics
  
## prometheus itself is an application 