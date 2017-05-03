$ sudo apt-get install postgresql-plperl `# this will trigger a db restart`
$ sudo su postgres
$ psql
$ SET session_replication_role = `replica`;
$ CREATE EXTENSION plperl;

$ pg_dump -s -U postgres -d star_wars | grep -v '^--' | grep -v '^$' | grep -v '^SET' | grep -v 'OWNER TO' > star_wars.sql
$ createuser bucardo -s -P
