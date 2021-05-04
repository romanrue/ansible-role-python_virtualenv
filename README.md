# Ansible Role: Ansible

[![CI](https://github.com/romanrue/ansible-role-python_virtualenv/workflows/CI/badge.svg?event=push)](https://github.com/romanrue/ansible-role-python_virtualenv/actions?query=workflow%3ACI)

An Ansible Role that installs Python and bootstraps virtualenv on Linux servers.

## Requirements

If using on a RedHat/CentOS-based host, make sure you've added the EPEL repository (it can easily be installed by including the `geerlingguy.repo-epel` role on Ansible Galaxy).

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

...

## Dependencies

None.

## Example Playbook

Install from the system package manager:

    - hosts: servers
      roles:
        - role: romanrue.python_virtualenv

Install from pip:

    - hosts: servers
      vars:
        ansible_install_method: pip
        ansible_install_version_pip: "2.7.0"
      roles:
        - role: geerlingguy.pip
        - role: romanrue.python_virtualenv

## License

MIT / BSD
