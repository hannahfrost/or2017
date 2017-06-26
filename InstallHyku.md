---
layout: default
---

# Installing Hyku

### Copy files from the thumbdrive / LibraryBox
You only need the or2017 directory. The docker directory contains the docker binaries.

### Uncompress
change into the or2017 directory and uncompress the images

```
cd or2017
gunzip hyku-all.tar.gz
```

### Load image bundle into docker

`docker load -i hyku-all.tar`


### If you are using docker-machine (older computers)
Skip this step if you are not using docker-machine.
Open `docker-compose.yml` in an editor an uncomment line 186

```
# You must uncomment this line if and only if you are running docker-machine
# - $DOCKER_CERT_PATH:$DOCKER_CERT_PATH
```

If you're on windows create a `.env` file with the following content:
```
COMPOSE_CONVERT_WINDOWS_PATHS=1
```

### Start docker

```
docker-compose up
```

### Create a hostname

Modify `/etc/hosts` and add `127.0.0.1 sample.localhost`
