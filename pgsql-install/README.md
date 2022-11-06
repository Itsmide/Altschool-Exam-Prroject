BASH script for installation of PostgreSQL on Ubuntu

This script will perform the following steps:

Check config file for PostgreSQL dependencies list, this will include optional dependencies as well for a total of 18.

Install packages based off of config file settings and log all missing dependencies.

Create directory: /postgres and other required.

Create system user 'postgres'.

Pull PostgreSQL from Git depot and confirm it is correct: git://git.postgresql.org/git/postgresql.git

Install PostgreSQL.

Configure PostgreSQL, ensuring the data files are stored in /postgres/data.

Start the PostgreSQL service using the pg_ctl command.

Optimize PSQL as well as securing it. This includes benchmarking/load testing.

Run create_hello.sql script

Run "/usr/local/pgsql/bin/psql -c 'select * from hello;' -U globus hello_postgres;" against newly created DB and test for successful response.

Add production enhancements such as support for being part of a cluster.
