$ sudo su postgres
$ psql

$ bucardo add db star_wars_source dbhost=$SOURCE dbuser=bucardo dbpass=bucardo dbname=star_wars
$ bucardo add db star_wars_target dbhost=$TARGET dbuser=bucardo dbpass=bucardo dbname=star_wars

$ bucardo add relgroup star_wars
$ bucardo add all tables db=star_wars_source relgroup=star_wars -n public
$ bucardo add all sequences db=star_wars_source relgroup=star_wars -n public

$ bucardo add sync star_wars dbs=star_wars_source,star_wars_target relgroup=star_wars onetimecopy=2
$ bucardo start
