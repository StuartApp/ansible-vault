# ansible-vault role
Installs and configures Hashicorp Vault for Linux distros which support `systemd`. It also sets AWS, LDAP/Jumpcloud and User&Password authentication methods. It uses Consul as the Storage backend.

## Requirements
![Ansible](https://img.shields.io/badge/ansible-2.8.2-green)

## Dependencies
No dependencies.


## Role variables
| Parameter    | Default |
|--------------|----------|
| `vault_version` | `1.1.2` |
| `vault_os` | `linux` |
| `vault_arch` | `amd64` |
| `vault_url` | `https://releases.hashicorp.com/vault/{{vault_version }}/vault_{{ vault_version }}_{{ vault_os }}_{{ vault_arch }}.zip` |
| `vault_configdir` | `/etc/vault` |
| `vault_configdir_ssl` | `{{ vault_configdir }}/ssl` |
| `vault_user` | `vault` |
| `vault_manage_user` | `true` |
| `vault_group` | `bin` |
| `vault_manage_group` | `true` |
| `vault_service_state` | `started` |
| `vault_service_enabled` | `yes` |
| `vault_service_execstartpre` | `[]` |
| `vault_listener_tcp_address` | `0.0.0.0:8200` |
| `vault_listener_tcp_tls_enable` | `true` |
| `vault_storage_consul_address` | `127.0.0.1:8500` |
| `vault_storage_consul_path` | `vault` |
| `vault_storage_consul_cluster_addr` | `""` |
| `vault_storage_consul_redirect_addr` | `""` |
| `vault_storage_consul_scheme` | `http` |
| `vault_storage_consul_tls_ca_file` | `""` |
| `vault_storage_consul_tls_cert_file` | `""` |
| `vault_storage_consul_tls_key_file` | `""` |
| `vault_storage_consul_token` | `""` |
| `vault_autounseal_aws` | `false` |
| `vault_autounseal_aws_key` | `""` |
| `vault_autounseal_aws_region` | `""` |
| `vault_web_ui` | `true` |
| `vault_api_addr` | `https://127.0.0.1:8200` |
| `vault_public_api_addr` | `{{ vault_api_addr }}` |
| `vault_config_extra` | `""` |
| `vault_auth_ldap_enable` | `false` |
| `vault_auth_ldap_config` | `{}` |
| `vault_auth_ldap_method_config` | `listing_visibility: unauth` |
| `vault_auth_userpass_enable` | `false` |
| `vault_auth_userpass_method_config` | `{}` |
| `vault_auth_aws_enable` | `false` |
