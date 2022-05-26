# MariaDB in Linux in Docker

[![Docker Automated build](https://img.shields.io/docker/automated/linuxcontainers/mariadb.svg?style=for-the-badge&logo=docker)](https://hub.docker.com/r/linuxcontainers/mariadb/)
[![Docker Pulls](https://img.shields.io/docker/pulls/linuxcontainers/mariadb.svg?style=for-the-badge&logo=docker)](https://hub.docker.com/r/linuxcontainers/mariadb/)
[![Docker Stars](https://img.shields.io/docker/stars/linuxcontainers/mariadb.svg?style=for-the-badge&logo=docker)](https://hub.docker.com/r/linuxcontainers/mariadb/)
[![Docker Image Size (tag)](https://img.shields.io/docker/image-size/linuxcontainers/mariadb?logo=docker&style=for-the-badge)](https://hub.docker.com/r/linuxcontainers/mariadb/)

[![Debian Version](https://img.shields.io/badge/Debian%20version-v11.3.0-green.svg?style=for-the-badge)](https://debian.org/)
[![MariaDB Version](https://img.shields.io/badge/MariaDB%20version-v10.7.4-green.svg?style=for-the-badge)](https://mariadb.org/)

This Docker image [(linuxcontainers/mariadb)](https://hub.docker.com/r/linuxcontainers/mariadb/) is based on the minimal [Debian Linux](https://mariadb.org/).

##### Debian 10 - Buster (Released May 9, 2020)
##### Debian 11 - Bullseye (Released August 14, 2021)

This docker image is the base Debian 10 Slim Linux for MariaDB 10.5.x and Debian 11 Slim for MariaDB 10.6.x. For more info on versions & support see [Releases](https://wiki.debian.org/DebianStable)

##### MariaDB Version 10.7.4

It is an evolution of MariaDB 10.3 with several entirely new features not found anywhere else and with backported and reimplemented features from MySQL.

----
##### MariaDB Version 10.7.4

MariaDB 10.7 is the current stable series of MariaDB. It is an evolution of MariaDB 10.3 with several entirely new features not found anywhere else and with backported and reimplemented features from MySQL.

----

## What is Debian Linux?
Debian is an operating system which is composed primarily of free and open-source software, most of which is under the GNU General Public License, and developed by a group of individuals known as the Debian project. Debian is one of the most popular Linux distributions for personal computers and network servers, and has been used as a base for several other Linux distributions.

## What is MariaDB?
MariaDB Server is one of the most popular open source relational databases. It’s made by the original developers of MySQL and guaranteed to stay open source. It is part of most cloud offerings and the default in most Linux distributions.

## Features

Minimal size only, minimal layers \
Memory usage is minimal on a simple install. \
MariaDB the MySQL replacement \

## Volume structure

* `/var/lib/mysql`: Database files
* `/var/lib/mysql/mysql-bin`: MariaDB logs

## Environment Variables:

### Main Mariadb parameters:
* `MYSQL_DATABASE`: specify the name of the database
* `MYSQL_USER`: specify the User for the database
* `MYSQL_PASSWORD`: specify the User password for the database
* `MYSQL_ROOT_PASSWORD`: specify the root password for Mariadb
* `MYSQL_CHARSET`: default charset (utf8) for Mariadb
* `MYSQL_COLLATION`: default collation (utf8_general_ci) for Mariadb

## Features

* Minimal size only, minimal layers
* Memory usage is minimal on a simple install

## Docker Tags and Versioning Scheme

Each image pushed to Docker Hub and the Github Container Registry is tagged as follows:
* The tag `latest` indicates, well, the latest image.
* Tags of the form MAJOR.MINOR.PATCH (such as 10.6) indicate the SemVer of 
  the __MariaDB__ image used as the base.
* Tags of the form MAJOR.MINOR (e.g., 10) correspond to the most recent patch level of
  the __MariaDB__ image used as the base. For example, if 10.6 is the latest
  release, then 10 maps to this as well.
* Tags of the form MAJOR (e.g., 10) correspond to the most recent patch level of
  the __MariaDB__ image used as the base, with major corresponding major version. 
  For example, if 10.6 is the latest release, then 10 maps to this as well.

[Semantic Versioning](https://semver.org/) uses version numbers of the form: MAJOR.MINOR.PATCH, where differences in MAJOR correspond
 to incompatible changes, differences in MINOR correspond to introduction of backwards compatible new functionality, and PATCH corres
ponds to backwards compatible bug fixes.


## Installation and Usage

The pre-built image is hosted on both Docker Hub and the Github Container Registry. You can use it in the following ways.

### Docker Pull Command

Pull the latest image from Docker Hub with the following (replace `latest` with 
a specific version number if you prefer):

```
docker pull linuxcontainers/mariadb:latest
```

Pull from the Github Container Registry with:

```
docker pull ghcr.io/linuxcontainers/mariadb:latest
```


### Use as a base image in a Dockerfile

Use as a base image in a Dockerfile (replace `latest` with 
a specific version number if you prefer):

```Dockerfile
FROM linuxcontainers/mariadb:latest

# The rest of your Dockerfile would go here.
```

Or you can use as a base image (via the Github Container Registry) with:

```Dockerfile
FROM ghcr.io/linuxcontainers/mariadb:latest

# The rest of your Dockerfile would go here.
```

A specific example usage can be found in the [Dockerfile of the generate-sitemap Github action](https://github.com/marketplace/action
s/generate-sitemap).


