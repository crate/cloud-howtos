.. _scale-storage:

=================
Scale the storage
=================

This guide will provide a quick overview of how to scale (vertical scaling)
your cluster storage using the CrateDB Cloud Console. This guide assumes that
you have a cluster up and running and can access the Console. If not, please
refer to the :ref:`tutorial on how to deploy a cluster
for the first time <cloud-tutorials:cluster-deployment>`.

There are things to keep in mind when scaling storage: see :ref:`Important
things to know <scale-storage-important>`.

.. NOTE::

    Please be aware that as actual cluster usage is billed, scaling your
    cluster storage can affect your charges.

.. WARNING::

    Increasing the storage is irreversible. You should only increase storage
    when you're sure you will need it.

.. rubric:: Table of contents

.. contents::
   :local:


.. _scale-storage-preferences:

Find the Cluster Preferences page
=================================

To scale your cluster storage in the Console, navigate to the Cluster
Preferences page. When you first access the Console, you will arrive at the
Organization page.

.. image:: ../_assets/img/organization-overview.png
   :alt: Cloud Console organization overview

To scale the cluster storage, you need to know what project the cluster belongs
to. Go to the Projects page in the left-hand menu to find an overview of all
projects associated with your organization. Select the one that has the cluster
you want to scale deployed in it. Please ensure the correct region is
selected in the dropdown menu at the top left to see the desired projects.

In the menu on the left hand, you should see below the divider line an icon or
icons representing all clusters associated with the currently selected project.
Here, find the correct cluster and click on the icon. It will expand and show
links for four pages: *Overview*, *Backups*, *Metrics*, and *Preferences*.

.. image:: ../_assets/img/cluster-dropdown.png
   :alt: Cloud Console projects cluster selection

Click on *Preferences*. This will take you to the Cluster Access page, where
you can see and edit your credentials. You can also enable deletion protection 
of your cluster and create a whitelist of IP addresses or CIDR blocks that are
allowed to connect to the cluster. 

.. image:: ../_assets/img/cluster-access.png
   :alt: Cloud Console cluster access settings

To edit the cluster storage, click on *Cluster scale* in the top bar. This will
take you to a page where you can see an overview of your cluster plan as well
as current cluster configuration.

.. image:: ../_assets/img/cluster-preferences.png
   :alt: Cloud Console cluster preferences


.. _scale-storage-instructions:

Scale the storage instructions
==============================

Once you arrive at the Cluster scale page, you can scale the cluster you
selected in three steps. First, click the *Edit cluster configuration* button
in the top right.

Secondly, choose the desired scaling value in the *Storage*
section. This will increase the per-node storage of your cluster.

Finally, confirm with *Save*.

.. image:: ../_assets/img/cluster-scale-dropdown.png
   :alt: Cloud Console cluster settings scaling menu

.. _scale-storage-important:

Important things to know
========================

When scaling the cluster storage, there are some important aspects to keep in
mind:

- Storage scaling cannot be reversed. Please make sure you need
  the storage increase before performing it.

- If you're expecting only a temporary traffic increase, scaling the amount of
  nodes in a cluster might be a better choice as it can be reversed again.

