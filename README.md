Containrd
=========

An Ansible role to install and configure Containerd.

Requirements
------------

- Supported version of Ansible: 2.12 and highter.
- Supported platforms:
  - Debian
    - 10
    - 11
    - 12
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

- `containerd_version` The specific version of `Containerd` to install. By default, role install the latest version.
- `containerd_repository_mirror_url` Mirror of Docker repository that contains `Containerd` package (default: `https://download.docker.com/linux`).
- `containerd_repository_gpgkey_url` URL to `Containerd` GPG public key file (see default values in `vars/*.yml`).
- `containerd_repository_release_channel` Docker repository release channel.

  Available values:
  - `stable` (default)
  - `test`

Dependencies
------------

None.

Example Playbook
----------------

- Install `Containerd`:

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
