# Hardware requirements

Geoprism Registry is memory intensive. The recommended server is equivalent to an AWS r4.large (2 vCPUs and 16 GB of RAM), with 500 GB of general-purpose SSD storage.

The example `docker-compose.yml` allows the web application up to 4 GB of memory and OrientDB up to 2 GB, so leave room for PostgreSQL and the operating system as well.

The software requirements are:

* Docker version 20.0 or later
* Docker Compose
