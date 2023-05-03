.. _index:

===========================
CrateDB Cloud How-To Guides
===========================

This is a collection of how-to guides for CrateDB Cloud. For the purposes of
these guides, we assume you interact with CrateDB Cloud by using the CrateDB
Cloud Console. This is the hosted user interface designed to make interacting
with CrateDB Cloud easier and more accessible, without the need for a command
line interface (CLI). If you do wish to use the CLI instead, see the
documentation for :ref:`Croud <cloud-cli:index>`, the CLI for CrateDB Cloud.

.. NOTE::

    Not all operations supported by the CrateDB Cloud Console are also
    available via Croud. Most importantly, clusters can only be deployed via
    the CrateDB Cloud Console.

.. NOTE::

    This resource assumes you know the basics. If not, check out the
    :ref:`tutorials <cloud-tutorials:index>` section for how to get started.
    Additionally, the :ref:`reference <cloud-reference:index>` section contains
    a :ref:`glossary <cloud-reference:glossary>` as well as an
    :ref:`overview <cloud-reference:overview>` of the CrateDB Cloud Console to
    give you further information.

.. SEEALSO::

    This is an open source documentation project. We host the source code and
    issue tracker on `GitHub`_.

.. rubric:: Table of contents

.. toctree::
    :maxdepth: 2
    :titlesonly:

    create-org
    add-users
    reconfigure-cluster
    suspend-cluster
    delete-cluster
    snapshot
    connect-to-cluster/index
    visualize-data-with-grafana
    logical-replication
    private-endpoints


.. _GitHub: https://github.com/crate/cloud-howtos/
