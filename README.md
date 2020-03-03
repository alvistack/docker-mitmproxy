# Docker Image Packaging for mitmproxy

[![Travis](https://img.shields.io/travis/alvistack/docker-mitmproxy.svg)](https://travis-ci.org/alvistack/docker-mitmproxy)
[![GitHub release](https://img.shields.io/github/release/alvistack/docker-mitmproxy.svg)](https://github.com/alvistack/docker-mitmproxy/releases)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-mitmproxy.svg)](https://github.com/alvistack/docker-mitmproxy/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/mitmproxy.svg)](https://hub.docker.com/r/alvistack/mitmproxy/)

mitmproxy is an interactive man-in-the-middle proxy for HTTP and HTTPS with a console interface.

Learn more about mitmproxy: <https://docs.mitmproxy.org/>

## Supported Tags and Respective `Dockerfile` Links

  - [`5.0`, `latest`](https://github.com/alvistack/docker-mitmproxy/blob/master/molecule/5.0/Dockerfile.j2)
  - [`4.0`](https://github.com/alvistack/docker-mitmproxy/blob/master/molecule/4.0/Dockerfile.j2)

## Overview

This Docker container makes it easy to get an instance of mitmproxy up and running.

Based on [Official Ubuntu Docker Image](https://hub.docker.com/_/ubuntu/) with some minor hack:

  - Minimized `Dockerfile` for meta data definition
  - Provision by Ansible and Molecule Docker driver in single layer
  - Handle `ENTRYPOINT` with [tini](https://github.com/krallin/tini)

### Quick Start

Start mitmproxy:

    # Pull latest image
    docker pull alvistack/mitmproxy
    
    # Run as detach
    docker run \
        -itd \
        --name mitmproxy \
        --publish 8080:8080 \
        alvistack/mitmproxy

**Success**. mitmproxy is now available on port `8080`.

## Versioning

The `latest` tag matches the most recent version of this repository. Thus using `alvistack/mitmproxy:latest` or `alvistack/mitmproxy` will ensure you are running the most up to date version of this image.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
