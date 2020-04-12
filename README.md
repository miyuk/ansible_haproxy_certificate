[![CircleCI](https://circleci.com/gh/miyuk/ansible_haproxy_certificate.svg?style=svg)](https://circleci.com/gh/miyuk/ansible_haproxy_certificate)

# HAProxy Certificate

This is an Ansible role to Install Certificate and Private Key for HAProxy server.


This module can use transport type `rest` only.

## Role Variables

| Variable | Description | Default |
| --- | --- | --- |
| `haproxy_src_crt_path` | source certificate path | "{{ certificate_directory }}/{{ certificate_crt_filename }}" |
| `haproxy_src_key_path` | source private key path | "{{ certificate_directory }}/{{ certificate_crt_filename }}" |
| `haproxy_dest_crt_and_key_force_create` | yes if overwrite certificate and private key | "{{ certificate_directory }}/{{ certificate_crt_filename }}" |
| `haproxy_dest_crt_and_key_path` | destination path | /etc/haproxy/ssl/server.crt |
| `haproxy_dest_crt_and_key_mode` | destination file permission mode | 0600 |
| `haproxy_dest_files_owner` | destination file owner | root |
| `haproxy_dest_files_group` | destination file group | root |
| `haproxy_restart` | yes if restart after deploy | yes |
| `haproxy_docker_dir` | docker-compose dir if use daemon type is docker | /opt/haproxy |
| `haproxy_daemon_type` | haproxy daemon type | docker |
| `haproxy_docker_name` | haproxy docker-compose name if daemon type is docker | haproxy |

## Install

this module name is `haproxy_certificate`. So, you try to install below command under Ansible Playbook folder.

```bash
cd roles
git clone git@github.com:miyuk/ansible_haproxy_certificate.git haproxy_certificate
```
