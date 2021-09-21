# Docker Image Packaging for mitmproxy

<img src="/alvistack.svg" width="75" alt="AlviStack">

[![GitLab pipeline status](https://img.shields.io/gitlab/pipeline/alvistack/docker-mitmproxy/master)](https://gitlab.com/alvistack/docker-mitmproxy/-/pipelines)
[![GitHub release](https://img.shields.io/github/release/alvistack/docker-mitmproxy.svg)](https://github.com/alvistack/docker-mitmproxy/releases)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-mitmproxy.svg)](https://github.com/alvistack/docker-mitmproxy/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/mitmproxy-7.0.svg)](https://hub.docker.com/r/alvistack/mitmproxy-7.0)

mitmproxy is an interactive man-in-the-middle proxy for HTTP and HTTPS with a console interface.

Learn more about mitmproxy: <https://docs.mitmproxy.org/>

## Supported Tags and Respective Packer Template Links

  - [`alvistack/mitmproxy-7.0`](https://hub.docker.com/r/alvistack/mitmproxy-7.0)
      - [`packer/docker-7.0/packer.json`](https://github.com/alvistack/docker-mitmproxy/blob/master/packer/docker-7.0/packer.json)
  - [`alvistack/mitmproxy-6.0`](https://hub.docker.com/r/alvistack/mitmproxy-6.0)
      - [`packer/docker-6.0/packer.json`](https://github.com/alvistack/docker-mitmproxy/blob/master/packer/docker-6.0/packer.json)

## Overview

This Docker container makes it easy to get an instance of mitmproxy up and running.

Based on [Official Ubuntu Docker Image](https://hub.docker.com/_/ubuntu/) with some minor hack:

  - Packaging by Packer Docker builder and Ansible provisioner in single layer
  - Handle `ENTRYPOINT` with [catatonit](https://github.com/openSUSE/catatonit)

### Quick Start

Start mitmproxy:

    # Pull latest image
    docker pull alvistack/mitmproxy-7.0
    
    # Run as detach
    docker run \
        -itd \
        --name mitmproxy \
        --publish 8080:8080 \
        alvistack/mitmproxy-7.0

**Success**. mitmproxy is now available on port `8080`.

## Versioning

### `YYYYMMDD.Y.Z`

Release tags could be find from [GitHub Release](https://github.com/alvistack/docker-mitmproxy/releases) of this repository. Thus using these tags will ensure you are running the most up to date stable version of this image.

### `YYYYMMDD.0.0`

Version tags ended with `.0.0` are rolling release rebuild by [GitLab pipeline](https://gitlab.com/alvistack/docker-mitmproxy/-/pipelines) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
