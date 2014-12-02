ennea-git-builder
=================

Build and push a docker image on git push

This was built for [EnneaHost](https://github.com/bryanlarsen/enneahost), although you should be able to use it outside of EnneaHost.

# Installation

## Prerequisites

- [Docker](http://docker.com)
- [gitreceive](https://github.com/progrium/gitreceive)
- [jq](http://stedolan.github.io/jq/)  (Optional)
- [Consul](http://consul.io) (Optional)

## Installation

- Copy [receiver](https://raw.github.com/bryanlarsen/ennea-git-builder/master/receiver) to `/home/git/receiver`.   Make sure it is executable

## Configuration

The following can be set in `/etc/default/enneahost`:

- `DOCKER_NAMESPACE`: default `registry.service.consul:5000`.  Either the location of a private Docker repository, the username/organization on the Docker Hub, or both.
- `CONSUL_IMAGES_URL`: default `http://consul.service.consul:8500/v1/kv/enneahost/images`.  the URL where metadata is to be POSTed to.  If blank, no POSTing is done.
