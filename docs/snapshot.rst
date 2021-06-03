.. _snapshot:

=============================
Restore backups and snapshots
=============================

This short guide explains in general terms the CrateDB Cloud backup policy for
automatically generating snapshots of the cluster data and how one can use such
snapshots to restore data. A more detailed technical discussion of how CrateDB
handles snapshots can be found in the CrateDB documentation about
:ref:`snapshots <crate-reference:snapshot-restore>`.

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
Restoring a snapshot resets that table or partition to the state it was in when
that snapshot was created.

You can restore a snapshot in two ways. One option is to `contact CrateDB Cloud
support`_. We are happy to assist. Alternatively, you can use the CrateDB Admin
UI to do it yourself. Please refer to the :ref:`reference documentation about
snapshots <crate-reference:snapshot-restore>` for assistance.


.. _contact CrateDB Cloud support: https://help.crate.io/en/
