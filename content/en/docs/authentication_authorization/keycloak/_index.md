---
title: "Keycloak"
weight: 
description: >
  Feasable way to bring authentication to our application
---

## CUSTOMIZE LOGIN PAGE 

```
sudo docker run --rm -p 8080:8080 -e KC_BOOTSTRAP_ADMIN_USERNAME=admin -e KC_BOOTSTRAP_ADMIN_PASSWORD=admin -v /data/rakicloud/rakicloud-library/oxc-keycloak-custom-theme:/opt/keycloak/themes/oxc-keycloak-custom-theme quay.io/keycloak/keycloak:26.0.7 start-dev


```
