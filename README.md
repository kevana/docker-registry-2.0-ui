# Docker Registry v2 with a UI

## What is it?

This is a docker-compose setup that runs a v2 registry on port 443 and nginx on port 80 serving a very minimal UI that lists repositories and their tags. You can start it with `docker-compose up -d`, use it like a normal registry, and access the UI at port 80 with your browser (e.g. http://localhost/).

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
