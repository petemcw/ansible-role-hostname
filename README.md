# Hostname Role for Ansible

[![Build Status](https://travis-ci.org/petemcw/ansible-role-hostname.svg?branch=master)](https://travis-ci.org/petemcw/ansible-role-hostname)

This role manages the hostname.

## Requirements

* Ansible 1.9+

## Role Variables

The variables that can be passed to this role and a brief description about
them are as follows:

```yaml
# Enable/Disable hostname tasks
hostname_enabled: true

# Default hostname
hostname_name: "{{ inventory_hostname }}"
```

## Examples

1. Configure the hostname with the defaults:

    ```yaml
    ---
    # This playbook configures hostname

    - name: Configure hostname on all nodes
      hosts: all
      roles:
        - hostname
    ```

2. Configure a non-default hostname:

    ```yaml
    ---
    # This playbook configures hostname

    - name: Configure hostname on all nodes
      hosts: all
      roles:
        - { role: hostname, hostname_name: "psc-doc-ansible01.augustash.com" }
    ```

## Dependencies

None.

## License

MIT
