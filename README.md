Containerd
==========

An Ansible role to install [Containerd](https://github.com/containerd/containerd) from the Docker repository and configure it.

Requirements
------------

- Supported version of Ansible: 2.12 and higher. Systems with Python versions below than 3.7 are not compatible with ansible-core 2.17 (see [ansible/ansible#83357](https://github.com/ansible/ansible/issues/83357#issuecomment-2150254754)).
- Supported platforms:
  - Debian
    - 10
    - 11
    - 12
  - Fedora
    - 39
    - 40
  - RHEL
    - 7
    - 8
    - 9
  - Ubuntu
    - 18.04
    - 20.04
    - 22.04

Role Variables
--------------

All variables that can be overridden are stored in the [defaults/main.yml](https://github.com/antmelekhin/ansible-role-containerd/blob/main/defaults/main.yml) file.
Please refer to the [meta/argument_specs.yml](https://github.com/antmelekhin/ansible-role-containerd/blob/main/meta/argument_specs.yml) file for a description of the available variables.
Similarly, descriptions and defaults for preset variables can be found in the [vars/main.yml](https://github.com/antmelekhin/ansible-role-containerd/blob/main/vars/main.yml) file.

Dependencies
------------

None.

Example Playbook
----------------

Install Containerd:

```yaml
---
- name: 'Install Containerd'
  hosts: all

  roles:
    - role: antmelekhin.containerd
```

License
-------

MIT

Author Information
------------------

Melekhin Anton.
