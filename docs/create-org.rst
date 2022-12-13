.. _create-org:

=========================
Create a new organization
=========================

This is a guide on how to create a new organization in the CrateDB Cloud
Console. If you follow the `cluster deployment tutorial`_, you will create an
organization as part of the signup process. There are scenarios where you may
want to create a new organization, however. If you arrive at the Console for
the first time, or if you have deleted your last organization, you will have
to create an organization to use the CrateDB Cloud Console's functionality. If
you wish to create multiple organizations when you are already in one, the
process is slightly different. This guide will show you both methods.

.. rubric:: Table of contents

.. contents::
   :local:


.. _create-org-new:

Create a first organization
===========================

When you first access the CrateDB Cloud Console, you will arrive at the
Organization overview page. If there is not currently an active organization,
the page will display an empty box logo and the message *No organization yet*.

.. image:: _assets/img/create-org.png
   :alt: Cloud Console org overview without organization

In order to create an organization, fill out the organization name in the
space provided, and click *Create organization*.

When the organization has been created, you will be returned to the
Organization overview.


.. _create-org-multiple:

Create multiple organizations
=============================

If you are already in an organization and want to create another one, go to
the Account tab. Here you will see a list of all your organizations and your
`user role`_ in them.

.. image:: _assets/img/account.png
   :alt: Cloud Console account tab

To create a new organization, click on *Create new organization* at the top
right above the organization list. The organization creation process is then
the same as that described above for a first organization. To delete an
organization, click the trashcan icon next to the organization in the list.

To switch the active organization, click on the organization name in the list.
All organization and cluster management options displayed in the
CrateDB Cloud Console will then refer to that organization until you switch
organizations again.


.. _create-org-overview:

The Organization page
=====================

To access the Organization overview page, click *Organization* at the top left
of the left-hand menu in the Console. At the Dashboard tab, you will see an
overview of your organization and any deployed clusters.

.. image:: _assets/img/organization-overview.png
   :alt: Cloud Console organization overview

The current tab is by default Dashboard. There are also six further
tabs.

In the Settings tab you see the organization name, unique ID, and
notification settings.

In the Users tab you can add users to the organization at organization level.
For more on adding users, see our :ref:`guide to adding users to organizations
<add-users>`. To understand roles and role definitions, see our
:ref:`guide to user roles in CrateDB Cloud <cloud-reference:overview>`.

The Audit Log tab allows the organization admin access to the audit log. For
more details on these tabs, see the description in the
:ref:`cloud-reference:overview`.

The Billing tab shows your billing method (e.g., credit card), address, and
upcoming charges. You can also always view the current bill at the bottom left
of the CrateDB Cloud Console.

The Regions tab shows the available CrateDB Cloud regions with options to
deploy a cluster in that region. It also allows you to create a custom region.

Finally, the Subscriptions tab displays your current subscription and gives
options for creating a new subscription with our supported cloud providers.

.. _cluster deployment tutorial: https://crate.io/docs/cloud/tutorials/en/latest/cluster-deployment/stripe.html
.. _user role: https://crate.io/docs/cloud/reference/en/latest/user-roles.html