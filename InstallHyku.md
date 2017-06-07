# Installing Hyku

### Get the docker image bundle
This file is called `hyku-all.tar.gz` and can be pulled from the LibraryBox.

### Uncompress

`gunzip hyku-all.tar.gz`

### Load image bundle into docker

`docker load -i hyku-all.tar`

### Download our docker compose.yml
```
git clone https://github.com/RepoCamp/or2017.git
cd or2017
```

### Start docker

```
docker up
```

### Create a hostname

Modify `/etc/hosts` and add `127.0.0.1 sample.localhost`
