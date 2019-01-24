mariadb
======

For setting up MariaDB on Ubuntu.


Requirements
------------
* Ubuntu 14.04 or newer.

Role Variables
--------------
* maradb_version:  If you want something newer or older than what comes with apt, then specify it. Not all versions combos have been configured yet. See tasks/main.yml

Performance tweaks:
* mysql_max_allowed_packet
* mysql_max_connections
* mysql_expire_logs_days
* mysql_general_log_file
* mysql_general_log
* mysql_slow_query_log
* mysql_slow_query_log_file
* mysql_long_query_time

Drupal commerce performance:
* mysql_transaction_isolation
* mysql_binlog_format

Non-trivial, potentially destructive:
* mysql_innodb_log_file_size - Don't use this unless you you absolutely know what you're doing
* mysql_datadir - Don't use this unless you you absolutely know what you're doing

Other:
* mariadb_mirror: $hostname # Which mirror to pull mariadb apt binaries from. Only applies when setting `maradb_version`.
* client_only (boolean): Only install the client, not the server.

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: dbmaster
  become: true
  gather_facts: true
  roles:
    - role: acromedia.mariadb

- hosts: app-nodes
  roles:
    - role: acromedia.mariadb
      vars:
        client_only: true
```

License
-------

GPLv3

Author Information
------------------

Acro Media Inc.
https://www.acromedia.com/
