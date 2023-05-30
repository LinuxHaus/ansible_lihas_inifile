Role Name
=========

set inifile values and eventually run commands if values got changed

Does so by copying a template. Everything in there before will be overwritten.

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
### %.config.inifile.INISHORT.path:
Path and Name of the ini-File to create
### %.config.inifile.INISHORT.command: []
List of commands to execute on change
### %.config.inifile.INISHORT.sections: []
List of dictionaries of sections
### %.config.inifile.INISHORT.sections[]name:
Name of the ini-Section
### %.config.inifile.INISHORT.sections[]entries: []
List of entries
### %.config.inifile.INISHORT.sections[]entries[]option
### %.config.inifile.INISHORT.sections[]entries[]value
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

