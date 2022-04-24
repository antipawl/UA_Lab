Class 1: Access on NGINX+ - Authentication for Web Access
=====================================================
This lab will show how to enable single sign-on (SSO) for applications being proxied by NGINX Plus. The solution uses OpenID Connect as the authentication mechanism, with Keycloak as the identity provider (IdP), and NGINX Plus as the relying party.

Expected time to complete: **1 hour**

High Level View of components in OpenID Connect Environment

.. image:: images/ualab01.svg
  :width: 800
  
This implementation assumes the following environment:

The identity provider (IdP) supports OpenID Connect 1.0
The authorization code flow is in use
NGINX Plus is configured as a relying party
The IdP knows NGINX Plus as a confidential client or a public client using PKCE
With this environment, both the client and NGINX Plus communicate directly with the IdP at different stages during the initial authentication event.

.. image:: images/ualab02.svg
  :width: 800
  




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
