$ sudo apt-get install bucardo
$ mkdir -p /var/run/bucardo
$ chown bucardo:bucardo /var/run/bucardo

$ sudo su postgres
$ psql
$ createuser bucardo -s -P bucardo
$ create database bucardo
$ bucardo install
