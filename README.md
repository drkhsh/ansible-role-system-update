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
|                                           |                                    |                                                  |

## Example playbook

```
- name: "Update and patch OS"
  hosts: all
  tags:
    - update
  roles:
    - drkhsh.system_update
```
