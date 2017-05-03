$ sudo apt-get install postgresql-plperl `# this will trigger a db restart`
$ sudo su postgres
$ psql
$ SET session_replication_role = `replica`;
$ CREATE EXTENSION plperl;

$ psql -f star_wars < star_wars.sql
