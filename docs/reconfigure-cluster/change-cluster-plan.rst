.. _change-cluster-plan:

===================
Change cluster plan
===================

This guide will provide a quick overview of changing your cluster plan
using the CrateDB Cloud Console. Changing plans is the best option when
you're looking for a performance increase. This guide assumes that you have a
cluster up and running and can access the Console.
If not, please refer to the :ref:`tutorial on how to deploy a cluster for the
first time <cloud-tutorials:cluster-deployment>`.

There are things to keep in mind when changing the cluster plan: see
:ref:`Important things to know <cluster-plan-important>`.

.. NOTE::

    Please be aware that as actual cluster usage is billed, changing your
    cluster plan can affect your charges.

.. rubric:: Table of contents

.. contents::
   :local:


.. _cluster-plan-preferences:

Find the Cluster Preferences page
=================================

To change your cluster plan in the Console, navigate to the Cluster
Preferences page. When you first access the Console, you will arrive at the
Organization page.

.. image:: ../_assets/img/organization-overview.png
   :alt: Cloud Console organization overview

To change the cluster plan, you need to know what project the cluster belongs
to. Go to the Projects page in the left-hand menu to find an overview of all
projects associated with your organization. Select the one that has the cluster
you want to edit deployed in it. Please ensure the correct region is
selected in the dropdown menu at the top left to see the desired projects.

In the menu on the left hand side, below the divider line, you should see an icon or
icons representing all clusters associated with the currently selected project.
Here, find the correct cluster and click on the icon. It will expand and show
links to four pages: *Overview*, *Backups*, *Metrics*, and *Preferences*.

.. image:: ../_assets/img/cluster-dropdown.png
   :alt: Cloud Console projects cluster selection

Click on *Preferences*. This will take you to the cluster access page, where
you can see and edit your credentials. You can also enable deletion protection 
for your cluster and create a whitelist of IP addresses or CIDR blocks that are
allowed to connect to the cluster. 

.. image:: ../_assets/img/cluster-access.png
   :alt: Cloud Console cluster access settings

To change the cluster plan, click on *Cluster scale* in the top bar. This
will take you to a page where you can see an overview of your cluster plan as
well as the current cluster configuration.

.. image:: ../_assets/img/cluster-preferences.png
   :alt: Cloud Console cluster preferences


.. _cluster-plan-instructions:

Change plan instructions
========================

Once you arrive at the Cluster scale page, you can edit the selected cluster in
three steps. First, click the *Edit cluster configuration* button in the top
right.

Secondly, choose the desired new plan under the *Cluster plan*
section.

Finally, confirm with *Save*.

.. image:: ../_assets/img/cluster-scale-dropdown.png
   :alt: Cloud Console cluster settings scaling menu

.. _cluster-plan-important:

Important things to know
========================

When changing the cluster plan, there are things to keep in mind:

- Cluster plan can be changed by Organization and Project admins.

- Switching plans is bi-directional, both up and down.

- Scaling down to CR0 is NOT supported.
