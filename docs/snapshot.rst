.. _snapshot:

===============
Restore backups
===============

This short guide explains in general terms the CrateDB Cloud backup policy for
automatically generating snapshots of the cluster data and how one can use 
such snapshots to restore data. A more detailed technical discussion of how
CrateDB handles snapshots can be found in the CrateDB documentation about
:ref:`snapshots <crate-reference:snapshot-restore>`.

You may also want to read our reference on :ref:`the backup page on the 
CrateDB Cloud Console <cloud-reference:overview-cluster-backups>`.

.. rubric:: Table of contents

.. contents::
   :local:


.. _snapshot-backup:

CrateDB Cloud's backup policy
=============================

CrateDB Cloud takes *hourly snapshots* which are kept for *14 days*.

.. _snapshot-restore:

Restore a snapshot
==================

Once a snapshot of a table or partition has been created, it can be restored.
Restoring a snapshot resets that table or partition to the state it was in 
when that snapshot was created. The relevant current table or partition is
dropped and replaced by its corresponding table or partition from the 
snapshot.

To restore a snapshot, first, navigate to the Clusters page and click *View* 
on the relevant cluster. This will bring you to the Overview page of your
cluster.

.. image:: /_assets/img/clusters-overview.png
   :alt: Cloud Console Clusters overview

From here, navigate to the Backups tab. Here you can see all your existing
snapshots.

.. image:: /_assets/img/backups.png
   :alt: Cloud Console Clusters backups

To restore a specific snapshot, click the *Restore* button next to the
snapshot. A window with a SQL statement will appear. 
Clicking the *Run query in Admin UI* will take you to the Admin UI console and
input the statement for you. Once you run it, the snapshot will be restored.


.. _contact CrateDB Cloud support: support@crate.io
.. _documentation on restoring snapshots: https://crate.io/docs/crate/reference/en/4.6/sql/statements/restore-snapshot.html#sql-restore-snapshot
