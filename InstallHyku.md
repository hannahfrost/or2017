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

### Start docker

```
docker-compose up
```

### Create a hostname

Modify `/etc/hosts` and add `127.0.0.1 sample.localhost`
