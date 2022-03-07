.. _create-org:

=========================
Create a new organization
=========================

This is a guide on how to create a new organization in the CrateDB Cloud
Console. If you follow the :ref:`cluster deployment tutorial
<cloud-tutorials:cluster-deployment>`, you will create an
organization as part of the signup process via the Console wizard. Currently,
clusters can only be deployed by this method. Should you, however, access the
Console without following this method, or have deleted your organization, this
guide will inform you on how to create one from scratch.

.. rubric:: Table of contents

.. contents::
   :local:


.. _create-org-new:

Create a new organization
=========================

When you first access the CrateDB Cloud Console, you will arrive at the
Organization overview page. If there is not currently an active organization,
the page will display an empty box logo and the message *No organization yet*.

.. image:: _assets/img/create-org.png
   :alt: Cloud Console org overview without organization

In order to create an organization, fill out the organization name in the space
provided, and click *Create organization*.

When the organization has been created, you will be returned to the
Organization page, where it will now be listed.


.. _create-org-overview:

The Organization page
=====================

To access the Organization overview page, click *Organization* at the top left
of the left-hand menu in the Console. Here you will see an overview of your
organization, further subscription options, and any deployed clusters.

.. image:: _assets/img/organization-overview.png
   :alt: Cloud Console organization overview

The current tab is by default *Subscriptions*. There are also three further
tabs.

In the *Settings* tab you see the organization name, unique ID, and
notification settings.

In the *Users* tab you can add users to the organization at organization level.
For more on adding users, see our :ref:`guide to adding users to organizations
and projects <add-users>`. To understand roles and role definitions, see our
:ref:`guide to user roles in CrateDB Cloud <cloud-reference:overview>`.

The *Audit Log* tab allows the organization admin access to the audit log. For
more details on these tabs, see the description in the
:ref:`cloud-reference:overview`.

To create a new project within the organization, go to the *Projects* page
after creating your organization. A description of this process can be found
:ref:`here <create-project>`.
