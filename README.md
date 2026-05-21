# Ansible Role: test

![GitHub](https://img.shields.io/github/license/jomrr/ansible-role-test) ![GitHub last commit](https://img.shields.io/github/last-commit/jomrr/ansible-role-test) ![GitHub issues](https://img.shields.io/github/issues-raw/jomrr/ansible-role-test)

Ansible role for setting up test.

## Dependencies

```yaml
collections:
  - name: ansible.posix
  - name: git+https://github.com/jomrr/ansible-collection-dev.git
    type: git
    version: main
```

## Role Variables

No role variable source was detected by the README generator.

## Supported Platforms

| OS Family | Distribution | Version | Container Image |
| --------- | ------------ | ------- | --------------- |
| RedHat | AlmaLinux | latest | [jomrr/molecule-almalinux:latest](https://hub.docker.com/r/jomrr/molecule-almalinux) |
| Alpine | Alpine | latest | [jomrr/molecule-alpine:latest](https://hub.docker.com/r/jomrr/molecule-alpine) |
| Debian | Debian | latest | [jomrr/molecule-debian:latest](https://hub.docker.com/r/jomrr/molecule-debian) |
| RedHat | Fedora | latest | [jomrr/molecule-fedora:latest](https://hub.docker.com/r/jomrr/molecule-fedora) |
| Suse | OpenSuse Leap | latest | [jomrr/molecule-opensuse-leap:latest](https://hub.docker.com/r/jomrr/molecule-opensuse-leap) |
| Suse | OpenSuse Tumbleweed | latest | [jomrr/molecule-opensuse-tumbleweed:latest](https://hub.docker.com/r/jomrr/molecule-opensuse-tumbleweed) |
| Debian | Ubuntu | latest | [jomrr/molecule-ubuntu:latest](https://hub.docker.com/r/jomrr/molecule-ubuntu) |

## Example Playbook

### Simple example playbook

Minimal example for applying this role.

```yaml
---
- name: "Configure test"
  hosts: "test"
  gather_facts: true
  roles:
    - role: "jomrr.test"
```

## References

- (Optional) Add any references here, such as links to documentation, related projects, etc.

## Author

[Jonas Mauer](https://github.com/jomrr)

## License

This project is licensed under the MIT License.
See [LICENSE](LICENSE) for the full license text.

Copyright (c) 2021 Jonas Mauer.
