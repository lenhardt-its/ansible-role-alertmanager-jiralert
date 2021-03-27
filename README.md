# Ansible Role: Alertmanager Jiralert

[![ubuntu-18](https://img.shields.io/badge/ubuntu-18.x-orange?style=flat&logo=ubuntu)](https://ubuntu.com/)
[![ubuntu-20](https://img.shields.io/badge/ubuntu-20.x-orange?style=flat&logo=ubuntu)](https://ubuntu.com/)
[![debian-9](https://img.shields.io/badge/debian-9.x-orange?style=flat&logo=debian)](https://www.debian.org/)
[![debian-10](https://img.shields.io/badge/debian-10.x-orange?style=flat&logo=debian)](https://www.debian.org/)
[![centos-7](https://img.shields.io/badge/centos-7.x-orange?style=flat&logo=centos)](https://www.centos.org/)
[![centos-8](https://img.shields.io/badge/centos-8.x-orange?style=flat&logo=centos)](https://www.centos.org/)

[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg?style=flat)](https://opensource.org/licenses/MIT)
[![GitHub issues](https://img.shields.io/github/issues/OnkelDom/ansible-role-alertmanager-jiralert?style=flat)](https://github.com/OnkelDom/ansible-role-alertmanager-jiralert/issues)
[![GitHub tag](https://img.shields.io/github/tag/OnkelDom/ansible-role-alertmanager-jiralert.svg?style=flat)](https://github.com/OnkelDom/ansible-role-alertmanager-jiralert/tags)
[![GitHub action](https://github.com/OnkelDom/ansible-role-alertmanager-jiralert/workflows/ansible-lint/badge.svg)](https://github.com/OnkelDom/ansible-role-alertmanager-jiralert)

## Description

Deploy Jiralert [Alertmanager - Jira](https://github.com/prometheus-community/jiralert) using ansible.

## Requirements

- Ansible >= 2.9 (It might work on previous versions, but we cannot guarantee it)
- Community Packages: `ansible-galaxy collection install community.general`

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `proxy_env` | {} | proxy environment variables |
| `jiralert_version` | 1.0 | app version |
| `jiralert_config_dir` | /etc/jiralert | default config folder |
| `jiralert_template_dir` | "{{ jiralert_config_dir }}/templates" | default tempalte folder |
| `jiralert_config_file` | config.yml | default config file |
| `jiralert_allow_firewall` | false | allow firewall access |
| `jiralert_binary_install_dir` | "/usr/local/bin" | default bin path |
| `jiralert_system_user` | "{{ jiralert_user | default('prometheus') }}" | default system user |
| `jiralert_system_group` | "{{ jiralert_group | default('prometheus') }}" | default system group |
| `jiralert_web_listen_port` | 9097 | default listen port |
| `jiralert_web_listen_address` | 0.0.0.0 | default listen address |
| `jiralert_default_template` | jiralert | default template |
| `jiralert_http_proxy` | [] | define proxy to send alerts over it |
| `jiralert_https_proxy` | [] | define proxy to send alerts over it |
| `jiralert_config_defaults` | {} | config defaults [defaults/main.yml](defaults/main.yml) |
| `jiralert_config_receivers` | {} | receivers [defaults/main.yml](defaults/main.yml) |
| `jiralert_config_template` | jiralert | config template [defaults/main.yml](defaults/main.yml) |

## Example

### Playbook

```yaml
---
- hosts: all
  roles:
  - onkeldom.alertmanager-jiralert
```

## Contributing

See [contributor guideline](CONTRIBUTING.md).

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
