docker-sandmanctl-mysql
=======================

This project was built to be a database browser for mysql
using [Sandman](https://sandman.readthedocs.org/en/latest/).

Usage:
------

```bash
$ docker run -e DATABASE_URL="mysql://user:pass@hostname/dbname" -p 5000:5000 -t sherzberg/sandman-mysql
```

Coming Soon:
------------

* Docker links
