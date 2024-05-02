Containrd
=========

An Ansible role to install and configure [Containerd](https://github.com/containerd/containerd).

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

- `containerd_root_path` The root directory for containerd metadata (default: `/var/lib/containerd`).
- `containerd_state_path` The state directory for containerd (default: `/run/containerd`).
- `containerd_config_path` The config directory for containerd (default: `/etc/containerd`).
- `containerd_oom_score` The out of memory score applied to the containerd daemon process (default: `0`).
- `containerd_debug_level` The debug log level. Supported levels are: `trace`, `debug`, `info`, `warn`, `error`, `fatal`, `panic` (default: `info`).
- `containerd_grpc_max_recv_message_size` and `containerd_grpc_max_send_message_size` (default: `16777216`).
- `containerd_metrics_address` Metrics endpoint does not listen by default (default: `''`).
- `containerd_metrics_grpc_histogram` Turn on or off gRPC histogram metrics (default: `false`).
- `containerd_max_concurrent_downloads` Restricts the number of concurrent downloads for each image (default: `3`).
- `containerd_max_container_log_line_size` The maximum log line size in bytes for a container (default: `16384`).
- `containerd_sandbox_image` The image used by sandbox container (default: `registry.k8s.io/pause:3.6`).
- `containerd_default_runtime_name` The default runtime name to use (default: `runc`).
- `containerd_snapshotter` The default snapshotter used by containerd (default: `overlayfs`).
- `containerd_runtimes` Runtimes configuration settings.

  Available values:
  - `name` The name of runtime (default: `runc`).
  - `type` The runtime type to use in containerd (default: `io.containerd.runc.v2`).
  - `engine`
  - `root`
  - `options` The options specific to runtime.

- `containerd_registries_mirrors` See official [documentation](https://github.com/containerd/containerd/blob/main/docs/hosts.md) (default: `[]`).

  Available values:
  - `namespace`
  - `server` The default server for this registry host namespace (default: `''`).
  - `mirrors`

    - `host`
    - `capabilities` The setting that specifies what operations a host can perform (default: `["pull", "resolve"]`).
    - `skip_verify` skips verifications of the registry's certificate chain and host name when set to `true` (default: `false`).
    - `override_path` is used to indicate the host's API root endpoint is defined in the URL path rather than by the API specification (default: `false`).

Dependencies
------------

None.

Example Playbook
----------------

Install `Containerd`:

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
