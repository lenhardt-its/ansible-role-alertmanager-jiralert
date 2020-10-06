# Ansible Role: alertmanager jiralert

## Description

Deploy [APP](https://github.com/) system using ansible.

## Requirements

- Ansible >= 2.6 (It might work on previous versions, but we cannot guarantee it)

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `dummy` | 0.0.0 | Binary version |
| `dummy` | /etc/app | Config Path |
| `dummy` | /var/lib/app | Data Path |

## Example

### Playbook

```yaml
---
- hosts: all
  roles:
  - ansible-role-alertmanager-jiralert
```

## Contributing

See [contributor guideline](CONTRIBUTING.md).

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
