# mysql-munin-generic

## Context

This role is to be used to activate all munin's mysql plugins available and disable the mysql_innodb one.

```console
├── LICENSE
├── README.md
├── defaults
│   └── main.yml
├── handlers
│   └── main.yml
├── meta
│   └── main.yml
└── tasks
    └── main.yml
```

## Variable

```yaml
munin_path_plugins: /usr/share/munin/plugins
munin_path_actives_plugins: /etc/munin/plugins
```

## Action

```yaml
---
- hosts: munin-mysql
  gather_facts: True
  
  roles:
    - { role: mysql-munin-generic, become: True }
```
