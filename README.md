Containerd
==========

An Ansible role to install [Containerd](https://github.com/containerd/containerd) from the Docker repository and configure it.

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

- `containerd_version` The version of the Containerd package. By default, Containerd is installed with the latest available version.
- `containerd_repository_mirror_url` The URL of Docker repository mirror (default: `https://download.docker.com/linux`).
- `containerd_repository_release_channel` Docker repository release channel. Available values are: `stable` (default), `test`.
- `containerd_root_path` The root directory for containerd metadata (default: `/var/lib/containerd`).
- `containerd_state_path` The state directory for containerd (default: `/run/containerd`).
- `containerd_config_path` The config directory for containerd (default: `/etc/containerd`).
- `containerd_oom_score` The out of memory score applied to the containerd daemon process (default: `0`).
- `containerd_debug_level` The debug log level. Supported levels are: `trace`, `debug`, `info`, `warn`, `error`, `fatal`, `panic` (default: `info`).
- `containerd_grpc_max_recv_message_size` and `containerd_grpc_max_send_message_size` Maximum gRPC receive and send message size in bytes (default: `16777216`).
- `containerd_metrics_address` Metrics tcp address (default: `''`).
- `containerd_metrics_grpc_histogram` Turn on or off gRPC histogram metrics (default: `false`).
- `containerd_max_concurrent_downloads` Restricts the number of concurrent downloads for each image (default: `3`).
- `containerd_max_container_log_line_size` The maximum log line size in bytes for a container (default: `16384`).
- `containerd_sandbox_image` The image used by sandbox container (default: `registry.k8s.io/pause:3.6`).
- `containerd_default_runtime_name` The default runtime name to use (default: `runc`).
- `containerd_snapshotter` The default snapshotter used by containerd (default: `overlayfs`).
- `containerd_runtimes` A list that contains runtimes configuration settings.
  - `name` The name of runtime (default: `runc`).
  - `type` The runtime type to use in containerd (default: `io.containerd.runc.v2`).
  - `engine`
  - `root`
  - `options` The options specific to the runtime.
- `containerd_registries_mirrors` A list that contains registry hosts configuration. See the official [documentation](https://github.com/containerd/containerd/blob/main/docs/hosts.md) (default: `[]`).
  - `namespace` A registry host namespace.
  - `server` The default server for this registry host namespace (default: `''`).
  - `mirrors` This section defines the names of registries.
    - `host` The hostname of the registry. It must be a valid domain name or an IP address.
    - `capabilities` The setting that specifies what operations a host can perform (default: `["pull", "resolve"]`).
    - `skip_verify` Boolean that defines if TLS verification should be skipped for the registry (default: `false`).
    - `override_path` is used to indicate the host's API root endpoint is defined in the URL path rather than by the API specification (default: `false`).
- `containerd_registries_auth` A list that contains a credential for a specific registry. See the official [documentation](https://github.com/containerd/containerd/blob/main/docs/cri/registry.md#configure-registry-credentials) (default: `[]`).
  - `registry` The hostname of the registry. It must be a valid domain name or an IP address.
  - `username` Username of the private registry basic auth.
  - `password` User password of the private registry basic auth.
  - `auth` Authentication token of the private registry basic auth.

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
