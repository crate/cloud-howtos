.. _connect-ruby:

====
Ruby
====

This section shows an example implementation of Ruby client library for CrateDB
Cloud:

.. code-block:: ruby

	require 'crate_ruby'

	client = CrateRuby::Client.new(servers=["<name-of-your-cluster>.cratedb.net:4200"], username: "admin", password: "<PASSWORD>", ssl: true)
	result = client.execute("SELECT name FROM sys.cluster")
	p result.to_a

For additional information see `our GitHub documentation`_.

.. _our GitHub documentation: https://github.com/crate/crate_ruby/blob/main/README.rst