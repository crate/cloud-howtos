.. _add-users:

=========
Add users
=========

This is a quick guide on how to add users to organizations and
how to manage their privileges. This information can also be found in the
CrateDB Cloud Console :ref:`Overview <cloud-reference:overview>` but is
presented here separately for ease of use.

.. rubric:: Table of contents

.. contents::
   :local:

In CrateDB Cloud you can add team members to your organizations.
In order to add a user, they must first have signed up for CrateDB Cloud. Once
they have an existing account, they can be added as a user. Users can be
members or admins of more than one organization at a time, but every
organization must have at least one organization admin (see also Restrictions
below).


.. _add-users-to-org:

Add users to an organization
============================

New users can be added to an organization by going to the Organization overview
page in the Console if you are logged in as organization admin. (For more
information on user roles and associated privileges, see our documentation on
:ref:`user roles <cloud-reference:user-roles>`.) At the top, you will see seven
tabs.

.. image:: _assets/img/organization-overview.png
   :alt: Cloud Console organization overview

Click the *Users* tab to see an overview of all users associated with the
organization. It will show their username, email, and user role.

To add a new user click the *Add user* button in the top right.

.. image:: _assets/img/organization-users.png
   :alt: Cloud Console organization overview users tab

First, enter the email address the user signed up with.

Second, select the :ref:`role <cloud-reference:user-roles>` you want to give
the user in your organization.

Finally, click *Save*.

.. image:: _assets/img/organization-users-dropdown.png
   :alt: Cloud Console org add user dropdown menu

A user who is a member of more than one organization can at any time switch
between organizations by using the dropdown menu at the top right of the
Organization overview screen. For a detailed overview of all the Organization
tabs, refer to our `Console overview`_.


.. _add-users-edit:

Edit and delete users from an organization
==========================================

You can also edit user roles and delete users in the *Users* tab. To edit a
user's role, simply click the pen icon corresponding to that user in the user
table. This will bring up a dropdown menu. To delete a user, use the bin icon.

.. _restrictions:

Restrictions
============

- An organization needs to have at least one organization admin. It is
  therefore not possible to remove the organization admin if there is only one.

.. _Console overview: https://crate.io/docs/cloud/reference/en/latest/overview.html