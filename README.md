[![CI](https://github.com/DanielWeeber/ansible-role-postfix_exporter/actions/workflows/release.yml/badge.svg?branch=master)](https://github.com/DanielWeeber/ansible-role-postfix_exporter/actions/workflows/release.yml) ![CI Pipeline](https://github.com/DanielWeeber/ansible-role-postfix_exporter/actions/workflows/ci.yml/badge.svg)


# Ansible Role: postfix exporter

This role installs Prometheus' [postfix exporter](https://github.com/kumina/postfix_exporter) on postfix hosts.

## Why?

As kumina only has the sourcecode available I've set up a GitHub Action CI to automatically build the postfix_exporter binary every monday. Binary will be stored in files/ and is used by the ansible role.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    postfix_exporter_options: ''

Any additional options to pass to `postfix_exporter` when it starts.

    postfix_exporter_state: started
    postfix_exporter_enabled: true

Controls for the `postfix_exporter` service.

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - role: ansible-role-postfix_exporter

## License

MIT / BSD

## Author Information

This role was created in 2021 by [Daniel Weeber](https://github.com/DanielWeeber). Heavily inspired and forked from [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).
