docker-sandmanctl-mysql
=======================

This project was built to be a database browser for mysql
using [Sandman](https://sandman.readthedocs.org/en/latest/). 
Specifically this was created to have a clean interface into
running docker mysql database instances.

Usage:
------

```bash
$ docker run -e DATABASE_URL="mysql://user:pass@hostname/dbname" -p 5000:5000 -t sherzberg/sandmanctl-mysql
```

*OR* use docker links!

```bash
$ docker run -e MYSQL_DATABASE=dbname -e MYSQL_USER=user -e MYSQL_PASSWORD=pass -name db -d orchardup/mysql
$ docker run -p 5000:5000 -link db:db -t sherzberg/sandmanctl-mysql
```

*NOTE*: Using docker links, the link alias is assumed to be _db_.

*NOTE*: This docker container relies on environment variables from the 
_db_ container. The example _orchardup/mysql_ container uses environment
variables to setup the database, user, and password.

Now visit [http://localhost:5000/admin](http://localhost:5000/admin) in your
browser to view the database with a nice interface.
