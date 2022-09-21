.. _connect-python:

======
Python
======

This guideasdasd

crate-python
------------

crate-python library implements the Python Database API 2.0 specification, 
which defines a common interface for accessing databases in Python

Example implementation will look like this:

.. code-block:: python

	from crate import client

	conn = client.connect("https://<name-of-your-cluster>.cratedb.net:4200", username="admin", password="<PASSWORD>", verify_ssl_cert=True)

	with conn:
	    cursor = conn.cursor()
	    cursor.execute("SELECT name FROM sys.cluster")
	    result = cursor.fetchone()
	    print(result)

See full documentation :ref:`here <crate-python:index>`.

psycopg2
--------

Psycopg is a popular PostgreSQL database adapter for Python. Its main features
are the complete implementation of the Python DB API 2.0 specification and the
thread safety (several threads can share the same connection).

Example implementation will look like this:

.. code-block:: python

	import psycopg2

	conn = psycopg2.connect(host="<name-of-your-cluster>.cratedb.net", port=5432, user="admin", password="<PASSWORD>", sslmode="require")

	with conn:
	    with conn.cursor() as cursor:
	        cursor.execute("SELECT name FROM sys.cluster")
	        result = cursor.fetchone()
	        print(result)

For more information see `psycopg documentation`_.

aiopg
-----

aiopg is a python library for accessing a PostgreSQL database from the asyncio
PEP-3156/tulip) framework. It wraps asynchronous features of the Psycopg
database driver.

Example implementation will look like this:

.. code-block:: python

	import asyncio
	import aiopg

	async def run():
	    async with aiopg.create_pool(host="<name-of-your-cluster>.cratedb.net", port=5432, user="admin", password="<PASSWORD>", sslmode="require") as pool:
	        async with pool.acquire() as conn:
	            async with conn.cursor() as cursor:
	                await cursor.execute("SELECT name FROM sys.cluster")
	                result = await cursor.fetchone()
	    print(result)

	loop = asyncio.get_event_loop()
	loop.run_until_complete(run())

For more information see `aiopg documentation`_.

asyncpg
-------

asyncpg is a database interface library designed specifically for PostgreSQL
and Python/asyncio. asyncpg is an efficient, clean implementation of PostgreSQL
server binary protocol for use with Python’s asyncio framework.

Example implementation will look like this:

.. code-block:: python

	import asyncio
	import asyncpg

	async def run():
	    conn = await asyncpg.connect(host="<name-of-your-cluster>.cratedb.net", port=5432, user="admin", password="<PASSWORD>", ssl=True)
	    try:
	        result = await conn.fetch("SELECT name FROM sys.cluster")
	    finally:
	        await conn.close()
	    print(result)

	loop = asyncio.get_event_loop()
	loop.run_until_complete(run())

For more information see `asyncpg documentation`_.

.. _psycopg documentation: https://www.psycopg.org/docs/
.. _aiopg documentation: https://aiopg.readthedocs.io/
.. _asyncpg documentation: https://magicstack.github.io/asyncpg/current/
