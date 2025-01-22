# ansible-role-system-update

This role conveniently patches hosts and updates all packages.

Following systems are supported:

- Arch Linux
- Debian / Ubuntu / Kali Linux
- Fedora
- Gentoo
- Red Hat / CentOS / Rocky
- Suse
- FreeBSD
- NetBSD
- OpenBSD

The role is published to [Ansible Galaxy](https://galaxy.ansible.com/ui/standalone/roles/drkhsh/journald_upload/)

## Parameters

See full list at [defaults.yml](./defaults/main.yml)

| Parameter                                 | Description                        | Default                                          |
|-------------------------------------------|------------------------------------|--------------------------------------------------|
| system_update_cleanup                     | Cleanup after upgrading            | `false`                                          |
| system_update_apt_upgrade_command         | Apt: Upgrade type (dist/full/safe) | `safe`                                           |
| system_update_apt_cache_valid_time        | Apt: Cache validity in seconds     | `3600`                                           |
| system_update_portage_binpkgs             | Portage: Use binary packages       | `false`                                          |
| system_update_portage_newuse              | Portage: New use flags             | `false`                                          |
| system_update_portage_changed_use         | Portage: Changed use flags         | `false`                                          |
| system_update_openbsd_become_method       | OpenBSD: Become method             | `community.general.doas`                         |

## Example playbook

```
- name: "Update and patch OS"
  hosts: all
  tags:
    - update
  roles:
    - drkhsh.system_update
```
