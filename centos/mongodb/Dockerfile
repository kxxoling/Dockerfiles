FROM centos:latest
MAINTAINER Kane Blueriver <kxxoling@gmail.com>

RUN yum -y update
RUN yum -y install epel-release
RUN yum -y install mongodb-server

RUN yum clean all

RUN mkdir -p /data/db

EXPOSE 27017
EXPOSE 27018
ENTRYPOINT ["/usr/bin/mongod"]
