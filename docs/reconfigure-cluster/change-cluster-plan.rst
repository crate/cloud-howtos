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

.. _cluster-change-plan-steps:

Steps to changing the plan
==========================

To change your cluster plan in the Console, navigate to the Clusters page in
the left-hand menu. Here you can see a list of all your clusters. Click *View*
on the cluster you wish to change.

.. image:: ../_assets/img/clusters-overview.png
   :alt: Cloud Console Clusters overview

This will bring you to the Overview page of your chosen cluster. 

.. image:: ../_assets/img/cluster-overview.png
   :alt: Cloud Console Clusters overview

Once here, navigate to the Scale page. Here you can change the plan of your
cluster. Simply click the *Edit cluster configuration*:

.. image:: ../_assets/img/cluster-scale-page.png
   :alt: Cloud Console Clusters overview

Now you can change the plan of your cluster. Keep in mind that scaling down to
CR0 is not allowed.

.. image:: ../_assets/img/cluster-edit-cluster-config.png
   :alt: Cloud Console Clusters overview

After you've made your changes, click *Save* to apply your changes.

.. _cluster-plan-important:

Important things to know
========================

When changing the cluster plan, there are things to keep in mind:

- Cluster plan can be changed by Organization admin.

- Switching plans is bi-directional, both up and down.

- Changing the plan down to CR0 is NOT supported.
