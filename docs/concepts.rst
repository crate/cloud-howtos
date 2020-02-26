.. _concepts:

================
Console concepts
================

The purpose of this short guide is to guide you through the way the CrateDB
Cloud Console hangs together. The structure of CrateDB Cloud as presented in
the Console revolves around three main concepts: *organizations*, *projects*,
and *services*. Each of these will be briefly explained here (in that order).
This guide does not provide technical detail about the structure of CrateDB
itself or walkthroughs on how to interact with the Console. For that, please
see the `CrateDB Guide`_ or the `Getting Started with CrateDB Cloud`_ guide,
respectively.

.. rubric:: Table of contents

.. contents::
   :local:


.. _concepts-orgs:

Organizations
=============

Organizations represent the larger structure - for example a company - within
which CrateDB Cloud projects and associated services are deployed. At the
organization level there is always at least one organization administrator, who
can in turn add organization members. Such organization admins and members have
access to the projects run by the organization. (For more on user roles in
CrateDB Cloud and how to set them, see our `guide`_.)

Each organization has a name, a unique ID, and optionally an associated email
address. For information on how to create an organization, please refer to our
`guide to creating a new organization`_. Note that currently each CrateDB Cloud
user account corresponds to only one organization.


.. _concepts-projects:

Projects
========

Projects are contained within organizations. A project exists to contain any
number of associated services deployed in a particular region for a specific
organizational need. For example, an organization may use distinct projects to
separate between development and production environments.

A given organization can have any number of projects. Just as organizations
have administrators and members, so projects have their own administrators and
members. The two groups can but need not overlap. (Again, for more on user
roles in CrateDB Cloud and how to set them, see our guide_.)

Each project has a name, an associated region, and a unique ID. For information
on how to create a project, please refer to our guide to creating a new
project.


.. _concepts-services:

Services
========

Within each project a project administrator can deploy any number of services.
One such service is the deployment of clusters, which can be done through the
CrateDB Cloud Console. A cluster is a set of two or more CrateDB instances
(referred to as nodes) which together form a single, distributed database.
Effectively, each cluster within CrateDB Cloud is a hosted (part of) a
database. Depending on the user's subscription plan and scaling, each cluster
can have a certain storage capacity and can process a certain amount of ingests
and queries per second. Only actual cluster usage - a service within CrateDB
Cloud - is actually billed.

A cluster has a name, a unique ID, as well as a certain storage and processing
capacity and a number of nodes. Note that clusters are also versioned. For
information on how to deploy a cluster, please see our `tutorial for deploying
a CrateDB cluster via Azure Marketplace`_.

Other offered services include, for example, the Azure Event Hubs consumer
service. This service can `ingest event data from Event Hubs into CrateDB`_.


.. _CrateDB Guide: https://crate.io/docs/crate/guide/en/latest/
.. _Getting Started with CrateDB Cloud: https://crate.io/docs/cloud/getting-started/en/latest/
.. _guide to creating a new organization: https://crate.io/docs/cloud/console/en/latest/create-org.html
.. _guide: https://crate.io/docs/cloud/console/en/latest/user-roles.html
.. _ingest event data from Event Hubs into CrateDB: https://crate.io/a/connecting-azure-iot-hub-and-cratedb-cloud-for-the-ingestion-of-sensor-data/
.. _tutorial for deploying a CrateDB cluster via Azure Marketplace: placeholder
