.. _private-endpoints:

============================
Configure a private endpoint
============================

A private endpoint, or private link, is a mechanism that allows a secure, private
connection to your cluster. Effectively, it allows you to bypass the public
internet when accessing the environment where your cluster is deployed. CrateDB
Cloud supports both AWS and Azure private endpoints.

.. rubric:: Table of contents

.. contents::
   :local:

.. _private-endpoints-configuration:

Configuration
-------------

This guide won't go into details of configuring the service itself on the
mentioned platforms. For those, see `AWS`_ and `Azure`_. guides.

If you're interested in this feature, `contact us`_ and we'll gladly get you
started. The workflow will look something like this:

1. Contact us and ask about configuring a private endpoint. We'll ask for your
   AWS Account ID or Azure Subscription ID.
2. We will create the endpoint service and provide you with the Alias/ID.
3. You create the private endpoint request.
4. We confirm it.

That's it. After this, you will have a secure, private way of connecting to
your CrateDB Cloud cluster.

.. _AWS: https://docs.aws.amazon.com/vpc/latest/privatelink
.. _Azure: https://learn.microsoft.com/en-us/azure/private-link/
.. _contact us: https://crate.io/contact
