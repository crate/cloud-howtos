.. _connect-php:

===
PHP
===

This section provides a quick overview of available PHP extensions for CrateDB
Cloud.

PDO
---

The PHP Data Objects (PDO) is a standard PHP extension that defines a common
interface for accessing databases in PHP.

Example implementation will look like this:

.. code-block:: php

	<?php

	require 'vendor/autoload.php';

	use Crate\PDO\PDO as PDO;

	$pdo = new PDO(
	    'crate:<name-of-your-cluster>.cratedb.net:4200',
	    'admin',
	    '<PASSWORD>'
	);

	$stm = $pdo->query('SELECT name FROM sys.cluster');
	$name = $stm->fetch();
	print $name[0];

	?>

See full documentation :ref:`here <crate-pdo:index>`.

DBAL
----

DBAL is a PHP database abstraction layer that comes with database schema
introspection, schema management, and PDO support.

Example implementation will look like this:

.. code-block:: console

	<?php

	require 'vendor/autoload.php';

	$params = array(
	    'driverClass' => 'Crate\DBAL\Driver\PDOCrate\Driver',
	    'user' => 'admin',
	    'password' = '<PASSWORD>',
	    'host' => '<name-of-your-cluster>.cratedb.net',
	    'port' => 4200
	);

	$connection = \Doctrine\DBAL\DriverManager::getConnection($params);
	$sql = 'SELECT name FROM sys.cluster';
	$name = $connection->query($sql)->fetch();

	print $name['name'];

	?>

See full documentation :ref:`here <crate-dbal:index>`.
