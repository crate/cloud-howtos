.. _delete-cluster:

================
Delete a cluster
================

In this tutorial, we will explain how to delete a cluster. If you have followed
the steps of our `tutorial`_ on how to set up a cluster from scratch, you
should have one running. (If not, refer to that tutorial for instructions.)
Although the `general documentation`_ for the CrateDB Cloud Console explains
how you can delete a cluster within the Console specifically, this tutorial
additionally provides a step-by-step guide for both methods of deleting a
cluster in order to make the process more transparent and easier to find.

You have two different ways to delete a cluster once it has been created. The
first is through the CrateDB Cloud Console itself; the second is via the
Microsoft Azure SaaS listing. We will describe each process below.

.. WARNING::

    All cluster data will be lost on deletion. This action cannot be undone.


.. _delete-cluster-console:

Deleting a cluster via the CrateDB Cloud Console
================================================

The easiest and preferred way to delete a cluster is via the CrateDB Cloud
Console. Make sure you are logged in to the Console with a user that has org
admin access. (For more on what that means, please see our documentation on
`user roles`_.)

In the Console, first we have to select the correct project within which the
cluster was deployed. To do this, go to the Projects page. Here you will see
an overview of all projects. (If you followed the previous tutorial, there
should be just one.)

.. image:: _assets/img/projects.png

Select the relevant project by clicking on it. Make sure the correct region is
displayed in the regions dropdown menu to see the correct project.

Next, we need to display the cluster in question. To do this, we need to access
the Cluster Settings page in the left-hand sidebar, below the divider line. The
name of the cluster you have created should appear in this sidebar; simply
click on it and the menu will 'roll out', showing the Settings option. This is
the one we want. Clicking this will lead to the Cluster Settings page for the
cluster.

.. image:: _assets/img/cluster-settings.png

On this page, you will see size and scaling information for the cluster in
question. You can delete the cluster here as well. Simply click the bin icon at
the top right. It will ask for confirmation; provide it and the cluster will be
deleted.


.. _delete-cluster-azure:

Deleting a cluster via the Microsoft Azure Portal
=================================================

As an alternative option, you can also delete a cluster - once deployment has
been confirmed in the CrateDB Cloud Console - directly via the Microsoft Azure
Portal. If you followed the `tutorial`_ on deploying a cluster from scratch
using the Azure Marketplace, you will already be familiar with it.

To delete a cluster via the Azure Portal, first we must head to the Azure
Portal |homepage|. Make sure you are logged in with the correct account
while on this page. If all is well, you should be able to see an overview of
different possible Azure services at the top of the page. If you have recently
used a SaaS resource, you should find in this overview the item "Software as a
Service (SaaS)". If this item is not present in the list, go to the search bar
at the top (which says *search resources, services, and docs*) and enter "SaaS"
there. The SaaS item should then appear in the list of results.

.. image:: _assets/img/azureservices.png

Click on this. If you have subscribed to the CrateDB Cloud offer and have
deployed a cluster previously, the cluster name should now appear in the list
of SaaS items.

.. image:: _assets/img/azuresaas.png

All that remains is to click directly on the relevant cluster name (you do not
need to tick the box). This will take you to a screen with cluster details.

.. image:: _assets/img/azuresaasdetails.png

To delete the cluster, press the *Delete* button at the top right and confirm.


.. _delete-cluster-billing:

Billing
=======

Crate.io only bills for actual cluster usage. During cluster operation, this is
on a per-hour basis. As soon as the cluster is deleted, nothing further will be
billed for that cluster.


.. _general documentation: https://crate.io/docs/cloud/howtos/en/latest/overview.html
.. _tutorial: https://crate.io/docs/cloud/tutorials/en/latest/getting-started/azure-to-cluster/index.html
.. _user roles: https://crate.io/docs/cloud/reference/en/latest/user-roles.html
.. |homepage| raw:: html

    <a href="https://portal.azure.com/#home" target="_blank">homepage</a>