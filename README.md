# NiFi-base ![](https://images.microbadger.com/badges/version/xemuliam/nifi-base:0.7.1.svg) ![](https://images.microbadger.com/badges/image/xemuliam/nifi-base:0.7.1.svg)
Basic and clean [Docker](https://www.docker.com/what-docker) image for [Apache NiFi](http://nifi.apache.org), based on [Alpine](http://alpinelinux.org) and [OpenJDK](http://openjdk.java.net)

                        ##         .
                  ## ## ##        ==
               ## ## ## ## ##    ===
           /"""""""""""""""""\___/ ===
      ~~~ {~~ ~~~~ ~~~ ~~~~ ~~~ ~ /  ===- ~~~
           \______ o   NiFi    __/
             \    \   0.7.1 __/
              \____\_______/

# Overview

Dockerized single-host NiFi.

Deployment options out of the box:
- Standalone NiFi node

Can work under Kitematic


# Exposed ports

- 8080 - NiFi web application port
- 8081 - NiFi ListenHTTP processor port
- 8443 - NiFi web application secure port


# Official Documentation and Guides

- [Overview](https://nifi.apache.org/docs.html)
- [User Guide](https://nifi.apache.org/docs/nifi-docs/html/user-guide.html)
- [Expression Language](https://nifi.apache.org/docs/nifi-docs/html/expression-language-guide.html)
- [Development Quickstart](https://nifi.apache.org/quickstart.html)
- [Developer's Guide](https://nifi.apache.org/developer-guide.html)
- [System Administrator](https://nifi.apache.org/docs/nifi-docs/html/administration-guide.html)


# Usage

This image can either be used as a base image for building on top of NiFi or just to experiment with. I personally have not attempted to use this in a production use case.


# Pre-Requisites
Ensure the following pre-requisites are met (due to some blocker bugs in earlier versions). As of today, the latest Docker Toolbox and Homebrew are fine.

- Docker 1.10+
- Docker Machine 0.6.0+
- Kitematic 0.12

(all downloadable as a single [Docker Toolbox](https://www.docker.com/products/docker-toolbox) package as well)


# How to use from Kitematic

1. Start Kitematic
2. Enter `xemuliam` in serach box
3. Choose `nifi-base` image
4. Click `Create` button

Kitematic will assign all ports and you'll be able to run HDF web-interface directly from Kitematic.


# How to use from Docker CLI

1. Start Docker Quickstart Terminal
2. Run command  `docker run -d -p 8080:8080 -p 8081:8081 -p 8443:8443 xemuliam/nifi-base:0.7.1`
3. Check Docker machine IP  `docker-machine ls`
4. Use IP from previous step in address bar of your favorite browser ` http://192.168.99.100:8080/nifi`

# Enjoy! :)
