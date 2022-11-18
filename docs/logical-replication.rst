.. _logical-replication:

==========================
Set up logical replication
==========================

This guide demonstrates how to configure logical replication on your CrateDB
Cloud cluster. Logical replication is a mechanism by which data can be copied
across multiple clusters. CrateDB uses a publish and subscribe model where
subscribers pull data from the publications of the publisher they subscribed
to.

This guide only provides an example of configuration in the context of Cloud
clusters. For a full documentation and all use-cases of logical replication
:ref:`see the full documentation. <administration-logical-replication>`

To get started, you will need to deploy some clusters first. Head over to
`Cloud Console`_ to do that.

.. rubric:: Table of contents

.. contents::
   :local:

Configure logical replication
-----------------------------

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
  CONNECTION 'crate://your-cluster-url.cratedb.net?mode=pg_tunnel&user=your_user&password=your_password' 
  PUBLICATION mypublication;

.. NOTE::

   By default, CrateDB uses the transport protocol (on port 4300) for logical
   replication. If the port is not available (such as with CrateDB Cloud), the
   ``mode=pg_tunnel`` can be used to tunnel over the Postgres protocol (port
   5432).

That's it in terms of configuration. Data from Cluster 1 will now be
automatically replicated on Cluster 2. This feature can also be configured on
multiple clusters, for example you could create another subscription on 
Cluster 3 to ensure high availability.

Disable logical replication
---------------------------

To disable the feature you need to remove the publication from the cluster
that serves as the datasource, and remove the subscription from the cluster
that serves as the target.

Remove a publication from Cluster 1
'''''''''''''''''''''''''''''''''''

Example publication:

.. code-block:: sql

  DROP PUBLICATION mypublication

Remove a subscription from Cluster 2
''''''''''''''''''''''''''''''''''''

Example subscription:

.. code-block:: sql

  DROP SUBSCRIPTION mysubscription 

Conclusion
----------

This is a configuration that works out-of-the-box on CrateDB Cloud Cluster.
For all the configuration options :ref:`see the full logical
replication documentation. <administration-logical-replication>`

.. _Cloud Console: https://console.cratedb.cloud/?utm_campaign=2022-Q3-WS-Developer-Motion&utm_source=docs
