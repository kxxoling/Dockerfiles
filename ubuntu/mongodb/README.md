# Ubuntu MongoDB Dockerfile

Config with comment:

```dockerfile
    FROM dockerfile/ubuntu

    # 安装 MongoDB
    RUN \
      apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10 && \
      echo 'deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen' > /etc/apt/sources.list.d/mongodb.list && \
      apt-get update && \
      apt-get install -y mongodb-org && \
      rm -rf /var/lib/apt/lists/*

    # 设置挂载点
    VOLUME ["/data/db"]

    # Define working directory.
    WORKDIR /data

    CMD ["mongod"]

    # 27017: process
    # 28017: http
    EXPOSE 27017
    EXPOSE 28017
```
