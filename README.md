# Docker Image Packaging for mitmproxy

[![Travis](https://img.shields.io/travis/com/alvistack/docker-mitmproxy.svg)](https://travis-ci.com/alvistack/docker-mitmproxy)
[![GitHub release](https://img.shields.io/github/release/alvistack/docker-mitmproxy.svg)](https://github.com/alvistack/docker-mitmproxy/releases)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-mitmproxy.svg)](https://github.com/alvistack/docker-mitmproxy/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/mitmproxy.svg)](https://hub.docker.com/r/alvistack/mitmproxy/)

mitmproxy is an interactive man-in-the-middle proxy for HTTP and HTTPS with a console interface.

Learn more about mitmproxy: <https://docs.mitmproxy.org/>

## Supported Tags and Respective Packer Template Links

  - [`5.2`, `latest`](https://github.com/alvistack/docker-mitmproxy/blob/master/packer/5.2/packer.json)
  - [`5.1`](https://github.com/alvistack/docker-mitmproxy/blob/master/packer/5.1/packer.json)

## Overview

This Docker container makes it easy to get an instance of mitmproxy up and running.

Based on [Official Ubuntu Docker Image](https://hub.docker.com/_/ubuntu/) with some minor hack:

  - Packaging by Packer Docker builder and Ansible provisioner in single layer
  - Handle `ENTRYPOINT` with [catatonit](https://github.com/openSUSE/catatonit)

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

### `alvistack/mitmproxy:latest`

The `latest` tag matches the most recent [GitHub Release](https://github.com/alvistack/docker-mitmproxy/releases) of this repository. Thus using `alvistack/mitmproxy:latest` or `alvistack/mitmproxy` will ensure you are running the most up to date stable version of this image.

### `alvistack/mitmproxy:<version>`

The version tags are rolling release rebuild by [Travis](https://travis-ci.com/alvistack/docker-mitmproxy) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
