.. _logical-replication:

==========================
Set up logical replication
==========================

This guide demonstrates how to configure logical replication on your CrateDB
Cloud cluster. Logical replication is a mechanism by which data can be copied
across multiple clusters. CrateDB uses a publish and subscribe model where subscribers pull data from the publications of the publisher they subscribed to.

This guide only provides an example of configuration in the context of Cloud
clusters. For a full documentation and all use-cases of logical replication
:ref:`see the full documentation. <administration-logical-replication>`

.. rubric:: Table of contents

.. contents::
   :local:

Configuration
-------------

Logical replication uses publication-subscription system. A publication is
created on a cluster from which the data should be copied, and a subscription
is created on a cluster where the data should be copied to.

Create a publication on Cluster 1
'''''''''''''''''''''''''''''''''

Example publication:

.. code-block:: sql

  CREATE PUBLICATION mypublication
  FOR ALL TABLES

Create a subscription on Cluster 2
''''''''''''''''''''''''''''''''''

Example subscription:

.. code-block:: sql

  CREATE SUBSCRIPTION mysubscription 
  CONNECTION'crate://gold-ackbar.aks1.eastus.azure.cratedb.net?mode=pg_tunnel&user=admin&password=98%2AQ3%26v1i%28-1OH-vFq9W2wYB' 
  PUBLICATION mypublication;

.. NOTE::

   The ``mode=pq_tunnel`` is tunnel mode is needed when the cluster is not
   reachable directly (outside of the network). Which, when working with
   CrateDB Cloud cluster, is basically always.
