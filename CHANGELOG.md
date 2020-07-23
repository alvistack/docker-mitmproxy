# Docker Image Packaging for mitmproxy

## 5.2.0-XalvistackY - TBC

### Major Changes

## 5.1.1-4alvistack3 - 2020-06-10

### Major Changes

  - Revamp `create`, `side_effect`, `verify` and `destroy` logic
  - Install with static binary archive
  - Replace `tini` with `catatonit`
  - Rename `post_tasks.yml` as `side_effect.yml`
  - Upgrade base image to Ubuntu 20.04

## 5.0.1-4alvistack4 - 2020-03-05

### Major Changes

  - Revamp with Molecule and `docker commit`
  - Consolidate molecule tests into `default` (noop)
  - Hotfix for systemd

## 5.0.1-3alvistack1 - 2020-01-15

### Major Changes

  - Replace `dumb-init` with `tini`, as like as `docker --init`
  - Include release specific vars and tasks

## 5.0.1-2alvistack1 - 2019-12-28

### Major Changes

  - Add 5.0 support

## 4.0.4-2alvistack3 - 2019-11-05

### Major Changes

  - Upgrade minimal Ansible support to 2.9.0
  - Upgrade Travis CI test as Ubuntu Bionic based
  - Default with Python 3
  - Hotfix for en\_US.utf8 locale

## 4.0.4-0alvistack1 - 2019-09-11

  - Ubuntu 18.04 based
  - Handle ENTRYPOINT with dumb-init
  - Self initialize with Ansible, by dogfooding with Ansible Playbook
