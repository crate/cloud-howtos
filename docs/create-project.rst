.. _create-project:

====================
Create a new project
====================

A guide on how to create a new project in the CrateDB Cloud Console.

.. rubric:: Table of contents

.. contents::
   :local:


.. _create-project-account:

The Account Overview page
=========================

When you first access the CrateDB Cloud Console, you will arrive at the Account
Overview page. This page displays your organization with the name you selected.
Within the organization, it shows any projects that currently exist. On the top
right you see the currently selected region. The existing region for each
project is displayed under the project name.

.. image:: _assets/img/account-overview.png

In order to create a new project within the organization, click on *New
project* within that organization section on this Account Overview page. This
will make a tab appear where you can name the new project.

.. image:: _assets/img/create-project.png

Name the project, then click *Create*. After a few seconds, the new project
will be created and will be added on the Account Overview page.


.. _create-project-overview:

The Project Overview page
=========================

Once a project has been created and is listed on the Account Overview page, you
can click on that project to go to the Project Overview page. Here you can see
an overview of all the services (e.g. clusters) attached to the project, as
well as their service name and billing. If no services have been deployed for
this project yet, this list will be empty.

.. image:: _assets/img/project-overview.png

From the left-hand menu, you can now navigate to the project users under
*Users* and the project settings under *Settings*. You can also click on a
service name on the Project Overview page to bring up their overview - for
CrateDB clusters, this will bring up the Cluster Overview page. (For more on
clusters, see our `guide on how to deploy a cluster via the Azure
Marketplace`_.)


.. _create-project-users:

The Project Users page
======================

The Project Users page is accessed by clicking on *Users* in the Project
Overview page. Here you will find a list of all users associated with the
project, including their name, email address, and project role. (For more on
project roles, see our `guide on user roles in CrateDB Cloud`_.)

.. image:: _assets/img/project-users.png

For information on adding users, please see our `guide to adding users to
organizations and projects`_.


.. _create-project-settings:

The Project Settings page
=========================

The Project Settings page is accessed by clicking on *Settings* in the Project
Overview page. This page provides an overview of the project name, project
region, and the project ID.

.. image:: _assets/img/project-settings.png

A project can be deleted in the Project Settings page by clicking the *Delete*
button at the top right.


.. _guide on how to deploy a cluster via the Azure Marketplace: https://help.crate.io/en/articles/3603380-how-to-deploy-a-cluster-via-the-azure-marketplace
.. _guide on user roles in CrateDB Cloud: https://crate.io/docs/cloud-console/docs/user-roles.rst
.. _guide to adding users to organizations and projects: https://crate.io/docs/cloud-console/docs/add-users.rst