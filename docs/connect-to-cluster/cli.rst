.. _connect-cli:

===
CLI
===

This section provides a quick overview of CLI clients available for CrateDB
Cloud clusters.

.. _crash:

Crash
-----

The CrateDB Shell (aka Crash) is an interactive command-line interface (CLI)
tool for working with CrateDB.

Example command to connect to your cluster will look like this:

.. code-block:: console

  crash --hosts 'https://<name-of-your-cluster>.cratedb.net:4200' -U 'admin' -W

See full documentation :ref:`here <crate-crash:index>`.

.. _psql:

psql
----

psql is a terminal-based front-end to PostgreSQL. It enables you to type in
queries interactively, issue them to PostgreSQL, and see the query results.

Example command to connect to your cluster will look like this:

.. code-block:: console

  psql -h '<name-of-your-cluster>.cratedb.net' -U 'admin' -W

For more information see `Full psql documentation`_.

.. _Full psql documentation: https://www.postgresql.org/docs/current/app-psql.html
