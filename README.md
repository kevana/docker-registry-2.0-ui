# Docker Registry

This folder contains the configuration information for our Docker Registry server, running on registry.example.com.

Images stored on this repo are prefixed with the domain name `registry.example.com`. E.g. hello-world:
```
docker pull registry.example.com/hello-world:latest
```

To push a new image to this registry, you must first tag the image with the registry prefix:
```
docker tag foo-image:latest registry.example.com/foo-image:latest
docker push registry.example.com/foo-image:latest
```

## Installation
```
git clone ...
# Add real certs
docker-compose up
# Navigate to http://registry.example.com/
```
