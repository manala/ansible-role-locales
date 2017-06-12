# Ansible Role: Locales [![Build Status](https://travis-ci.org/manala/ansible-role-locales.svg?branch=master)](https://travis-ci.org/manala/ansible-role-locales)

This role will deal with the configuration of system __locales__.

It's part of the Manala <a href="http://www.manala.io" target="_blank">Ansible stack</a> but can be used as a stand alone component.

## Requirements

None.

## Dependencies

None.

## Installation

### Ansible 2+

Using ansible galaxy cli:

```bash
ansible-galaxy install manala.locales
```

Using ansible galaxy requirements file:

```yaml
- src: manala.locales
```

## Role Handlers

None

## Role Variables

| Name                           | Default  | Type   | Description                                    |
| ------------------------------ | -------- | ------ | ---------------------------------------------- |
| `manala_locales_codes`         | [ ]      | Array  | Locales to configure                           |
| `manala_locales_codes_default` | nil      | String | Default locale, stored in /etc/default/locale  |

### Configuration example

```yaml
manala_locales_codes_default: C.UTF-8

manala_locales_codes:
  - fr_FR.UTF-8
  - name: en_EN.UTF-8
    state: absent
```

## Example playbook

```yaml
- hosts: servers
  roles:
    - { role: manala.locales }
```

# Licence

MIT

# Author information

Manala [**(http://www.manala.io/)**](http://www.manala.io)
