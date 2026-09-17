# Ansible Role: test

![GitHub](https://img.shields.io/github/license/jomrr/ansible-role-test)
![GitHub last commit](https://img.shields.io/github/last-commit/jomrr/ansible-role-test)
![GitHub issues](https://img.shields.io/github/issues-raw/jomrr/ansible-role-test)
[![dev](https://img.shields.io/github/actions/workflow/status/jomrr/ansible-role-test/dev.yml?branch=dev&label=dev)](https://github.com/jomrr/ansible-role-test/actions/workflows/dev.yml?query=branch%3Adev)
[![main](https://img.shields.io/github/actions/workflow/status/jomrr/ansible-role-test/main.yml?branch=main&label=main)](https://github.com/jomrr/ansible-role-test/actions/workflows/main.yml?query=branch%3Amain)

Test role for demonstrating generated Ansible CI workflows.

## Purpose

Exercise and demonstrate the ansible-factory generator, lint hooks, Molecule
container lifecycle, and CI workflows. This is a test fixture with no
application functionality. With its default settings, applying the role makes no
changes to the managed host and is idempotent.

## Dependencies

```yaml
collections:
  - name: ansible.posix
  - name: community.general
    version: '>=12.0.0'
  - name: git+https://github.com/jomrr/ansible-collection-dev.git
    type: git
    version: main
```

## Role Variables

### `test_role_enabled`

Type: `bool`. Required: `false`.

Enable the demonstration tasks that load platform variables and pass an empty
package list to the package module.

Default:

```yaml
test_role_enabled: false
```

## Check Mode

With the default test_role_enabled: false, the demonstration tasks are skipped
in both normal and check mode.

## Operational Notes

- The default Molecule scenario uses the disabled role default. Its verify stage
  only demonstrates playbook execution; there is no application or service to
  verify.
- The optional enabled path retains a package-task example with empty platform
  package lists. The dev scenario enables this path on all configured platforms;
  the default CI scenario keeps it disabled.

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

### CI demonstration

Apply the test fixture with its default no-op behavior.

```yaml
---
- name: TEST | Demonstrate role execution
  hosts: all
  gather_facts: true
  roles:
    - role: jomrr.test
```

## Author

[Jonas Mauer](https://github.com/jomrr)

## License

This project is licensed under the MIT License.
See [LICENSE](LICENSE) for the full license text.

Copyright (c) 2021 Jonas Mauer.
