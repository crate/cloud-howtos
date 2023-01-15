.. _private-endpoints:

============================
Configure a private endpoint
============================

A private endpoint, or private link, is a mechanism that allows a secure, private connection to your cluster. Effectively, it allows you to bypass the public internet when accessing the environment where your cluster is deployed. Note that private endpoints don’t work across providers, meaning that if you want to securely access your AWS cluster, you must do so from within the AWS environment.

To create a private endpoint, you need to deploy a cluster first. To do that,
go to the `Cloud Console`_. 

Enabling private endpoints takes some configuration from our side, so the 
first step is contacting us. To do that, navigate to the Access tab of your
cluster.

.. image:: /_assets/img/access-page.png
   :alt: Cloud Console Access overview

Once here, there is a Private Link section at the bottom. To request a private
link, click the *Request Private Link* button. Fill out the requested
information and click *OK*. We will get back to you as soon as we can.

.. _Cloud Console: https://console.cratedb.cloud/?utm_campaign=2022-Q3-WS-Developer-Motion&utm_source=docs
