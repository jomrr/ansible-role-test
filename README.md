# ansible-role-testing

![GitHub](https://img.shields.io/github/license/jam82/ansible-role-testing) ![GitHub last commit](https://img.shields.io/github/last-commit/jam82/ansible-role-testing) ![GitHub issues](https://img.shields.io/github/issues-raw/jam82/ansible-role-testing) ![Actions](https://github.com/jam82/ansible-role-testing/actions/workflows/molecule.yml/badge.svg)

**Ansible role for setting up test.**

## Supported Platforms

- Alpine
- Archlinux
- CentOS
- Debian
- Fedora
- OpenSuse Leap, Tumbleweed
- OracleLinux
- Ubuntu

## Requirements

Ansible 2.9 or higher.

## Variables

Variables and defaults for this role.

### defaults/main.yml

```yaml
test_role_enabled: false
```

## Dependencies

None.

## Example Playbook

```yaml
---
# role: ansible-role-testing
# play: test
# file: test.yml

- hosts: all
  become: true
  gather_facts: true
  vars:
    test_role_enabled: true
  roles:
    - role: ansible-role-testing
```

## License and Author

- Author:: [jam82](https://github.com/jam82/)
- Copyright:: 2021, [jam82](https://github.com/jam82/)

Licensed under [MIT License](https://opensource.org/licenses/MIT).
See [LICENSE](https://github.com/jam82/ansible-role-testing/blob/master/LICENSE) file in repository.

## References

- [ArchWiki](https://wiki.archlinux.org/)
