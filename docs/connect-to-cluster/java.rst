.. _connect-java:

====
Java
====

JDBC is a standard Java API that provides a common interfaces for accessing
databases in Java.

Example method used in implementation:

.. code-block:: java

	import java.sql.*;
	import java.util.Properties;

	public class Main {
	    public static void main(String[] args) {
	        try {
	            Properties properties = new Properties();
	            properties.put("user", "admin");
	            properties.put("password", "<PASSWORD>");
	            properties.put("ssl", true);
	            Connection conn = DriverManager.getConnection(
	                    "crate://<name-of-your-cluster>.cratedb.net:5432/",
	                    properties
	            );

	            Statement statement = conn.createStatement();
	            ResultSet resultSet = statement.executeQuery("SELECT name FROM sys.cluster");
	            resultSet.next();
	            String name = resultSet.getString("name");

	            System.out.println(name);
	        } catch (SQLException e) {
	            e.printStackTrace();
	        }
	    }
	}

See full documentation :ref:`here <crate-jdbc:index>`.