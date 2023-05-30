Role Name
=========

set inifile values

Requirements
------------

Uses lihas_variables to merge the configuration from multiple sources

To run solo:

```
ansible-galaxy install -r requirements.yml
ansible-playbook -i localhost, inifile.yml
```

Role Variables
--------------

Dictionaries with random name and entries `ctl` and `value`
### %.config.inifile.INISHORT
INISHORT is just any identifiert, possibly giving a hint what we talk about
The name of the inifile, e.g. /etc/php/8.2/fpm/conf.d/99-memory.ini
### %.config.inifile.INISHORT.entries: []
List of entries
### %.config.inifile.INISHORT.entries[]section
### %.config.inifile.INISHORT.entries[]option
### %.config.inifile.INISHORT.entries[]value
The section, option and value

Dependencies
------------

* lihas_variables

Example Playbook
----------------

## Example Playbook
```
---
- hosts: '*'
  roles:
    - lihas_inifile
```

License
-------

GPL-3.0-or-later

Author Information
------------------

Adrian Reyer <lihas@lihas.de>

