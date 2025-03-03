# ansible-role-vnc-server #

[![GitHub Build Status](https://github.com/cisagov/ansible-role-vnc-server/workflows/build/badge.svg)](https://github.com/cisagov/ansible-role-vnc-server/actions)
[![Total alerts](https://img.shields.io/lgtm/alerts/g/cisagov/ansible-role-vnc-server.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/cisagov/ansible-role-vnc-server/alerts/)
[![Language grade: Python](https://img.shields.io/lgtm/grade/python/g/cisagov/ansible-role-vnc-server.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/cisagov/ansible-role-vnc-server/context:python)

An Ansible role for installing a VNC server.

## Requirements ##

None.

## Role Variables ##

| Variable | Description | Default | Required |
|----------|-------------|---------|----------|
| password | The password for the VNC user. | Defaults to a random value. | No |
| private\_ssh\_key | The private ssh key for the VNC user. | By default no such key is assigned to the VNC user. | No |
| public\_ssh\_key | The public ssh key for the VNC user. | By default no such key is assigned to the VNC user. | No |
| username | The name of the VNC user, which will be created. | `vnc` | No |
| user\_groups | A list of additional groups to which the VNC user should belong. | [Omitted](https://docs.ansible.com/ansible/latest/user_guide/playbooks_filters.html#making-variables-optional) | No |
| user\_uid | The UID to use for the VNC user. | [Omitted](https://docs.ansible.com/ansible/latest/user_guide/playbooks_filters.html#making-variables-optional) | No |

## Dependencies ##

None.

## Example Playbook ##

Here's how to use it in a playbook:

```yaml
- hosts: all
  become: yes
  become_method: sudo
  roles:
    - vnc_server
```

## Contributing ##

We welcome contributions!  Please see [`CONTRIBUTING.md`](CONTRIBUTING.md) for
details.

## License ##

This project is in the worldwide [public domain](LICENSE).

This project is in the public domain within the United States, and
copyright and related rights in the work worldwide are waived through
the [CC0 1.0 Universal public domain
dedication](https://creativecommons.org/publicdomain/zero/1.0/).

All contributions to this project will be released under the CC0
dedication. By submitting a pull request, you are agreeing to comply
with this waiver of copyright interest.

## Author Information ##

David Redmin - <david.redmin@trio.dhs.gov>
