# Class 1: Access on NGINX+ - Authentication for Web Access
=====================================================

This Agility Lab covers the following topics:



Expected time to complete: **1 hour**

Lab Setup
---------

We will leverage the following setup to enable OpenID Connect-based single-sign-on for applications proxied by NGINX Plus, using Keycloak as the identity provider (IdP).

.. list-table::
   :header-rows: 1

   * - **Hostname**
     - **IP-ADDR**
     - **Credentials**
   * - nginx
     - 10.1.1.4
     - ubuntu/ubuntu
   * - infra
     - 10.1.1.5
     - admin/admin
       root/default
   * - container/keycloak
     - 10.1.1.5:8080
     - admin/admin
