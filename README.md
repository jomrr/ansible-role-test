# Ansible role: TEST

![GitHub](https://img.shields.io/github/license/jomrr/ansible-role-test) ![GitHub last commit](https://img.shields.io/github/last-commit/jomrr/ansible-role-test) ![GitHub issues](https://img.shields.io/github/issues-raw/jomrr/ansible-role-test)

**Ansible role for setting up test.**

## Description

This Ansible role installs and configures test on supported platforms.

## Prerequisites

This role has no special prerequisites.

## Dependencies (requirements.yml)

```yaml
collections:
  - name: "ansible.posix"
  - name: "jomrr.dev"
    src: "git+ssh://github.com/jomrr/ansible-collection-dev.git"
    version: "main"

roles: []
```

## Supported Platforms

| OS Family | Distribution | Version | Container Image |
|-----------|--------------|---------|-----------------|
| RedHat | AlmaLinux | latest | [jomrr/molecule-almalinux:latest](https://hub.docker.com/r/jomrr/molecule-almalinux) |
| Alpine | Alpine | latest | [jomrr/molecule-alpine:latest](https://hub.docker.com/r/jomrr/molecule-alpine) |
| Debian | Debian | latest | [jomrr/molecule-debian:latest](https://hub.docker.com/r/jomrr/molecule-debian) |
| RedHat | Fedora | latest | [jomrr/molecule-fedora:latest](https://hub.docker.com/r/jomrr/molecule-fedora) |
| Suse | OpenSuse Leap | latest | [jomrr/molecule-opensuse-leap:latest](https://hub.docker.com/r/jomrr/molecule-opensuse-leap) |
| Suse | OpenSuse Tumbleweed | latest | [jomrr/molecule-opensuse-tumbleweed:latest](https://hub.docker.com/r/jomrr/molecule-opensuse-tumbleweed) |
| Debian | Ubuntu | latest | [jomrr/molecule-ubuntu:latest](https://hub.docker.com/r/jomrr/molecule-ubuntu) |

## Role Variables

No role default variables specified, see [defaults/main.yml](defaults/main.yml).

## Example Playbook

Example playbooks that show how to use this role.

### Simple example playbook

A simple default example playbook for using jomrr.test.
```yaml
---
# name: "jomrr.test"
# file: "playbook_test.yml"

- name: "PLAYBOOK | test"
  hosts: "test"
  gather_facts: true
  roles:
    - role: "jomrr.test"
```

## Author(s) and License

- :octocat: Author: [jomrr](https://github.com/jomrr)
- :triangular_flag_on_post: Copyright: 2024, Jonas Mauer
- :page_with_curl: License: [MIT](LICENSE)

## References

- (Optional) Add any references here, such as links to documentation, related projects, etc.

---
