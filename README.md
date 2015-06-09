# Ubuntu + Oracle jdk 7 + eXo Platform Community Docker container

* Ubuntu 14.04
* Oracle JDK 7 update 71
* eXo Platform 4.2.0-RC1 Community edition

*  **Needs a linked container called mysql**

* Mysql connections details configured through environment variables, for example:
  * MYSQL_DATABASE: exo
  * MYSQL_USER: exo
  * MYSQL_PASSWORD: changeme

## How to

* run the container


    docker run -d -p 8080:8080 --env MYSQL_DATABASE=exo --env MYSQL_USER=exo --env MYSQL_PASSWORD=changeme --name=exo exoplatform/ubuntu-jdk7-exo:plf-4.1.0

**It is highly recommended to run this container as part of a docker-compose setup using mysql/mysql-server:latest image as the MySQL DB container and making sure both services use the same MYSQL_ environment variables values.**


* watch container logs


    docker logs --follow exo
