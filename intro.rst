Getting Started
---------------

Please follow the instructions provided by the instructor to start your
lab.

.. NOTE::
	 All work for this lab will be performed exclusively from the udf session. No installation or interaction with your local system is
	 required.

Lab Topology
~~~~~~~~~~~~

The following components have been included in your lab environment:

- 1 x Infa Server Running the below Docker Containers (Ubuntu 20.04)

  - firefox
  - keycloak
  - juiceshop

- 1 x Linux Server (Ubuntu 20.04) running Nginx (nginx/1.21.5 (nginx-plus-r26))

Lab Components
^^^^^^^^^^^^^^

The following table lists VLANS, IP Addresses and Credentials for all
components:

Lab Setup
---------
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
   * - container/juiceshop
     - 10.1.1.5:3000
     - 
   * - container/firefox
     - 10.1.1.5:5180
     - 
  
This lab will show how to enable single sign-on (SSO) for applications being proxied by NGINX Plus. The solution uses OpenID Connect as the authentication mechanism, with Keycloak as the identity provider (IdP), and NGINX Plus as the relying party.