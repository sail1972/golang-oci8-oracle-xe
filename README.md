golang-oci8-oracle-xe
=====================

This repository contains a Dockerfile to create a docker container with Golang latest version, go-oci8 Oracle Express Edition 11g Release 2 and Ubuntu Strech.

This project is inspired by cross compiling golang program using go-oci8 and Oracle XE for linux/amd64 platform.

## How to: Install and Use

### Install:

```
docker pull sail1972/golang-oci8-oracle-xe
```
### Start Oracle XE:

```
docker run -d --shm-size=2g -p 1521:1521 sail1972/golang-oci8-oracle-xe
```

### Connect:
Connect database with following setting:
```
hostname: localhost
port: 1521
sid: xe
username: system
password: oracle
```

Password for **SYS** user
```
oracle
```

Connect to Oracle Application Express web management console with following settings:
```
url: http://localhost:8080/apex
workspace: internal
user: admin
password: oracle
```

### Thanks

[mattn](https://github.com/mattn) The author of project [go-oci8](https://github.com/mattn/go-oci8)

[Alexei Ledenev](https://github.com/alexei-led) The author of project [docker-oracle-xe-11g](https://hub.docker.com/r/alexeiled/docker-oracle-xe-11g/)

[ricsmania](https://github.com/ricsmania) Who reminded me using Docker to cross compiling from Mac to linux/amd64. The issue is [here](https://github.com/mattn/go-oci8/issues/84).
