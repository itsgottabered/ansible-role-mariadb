mariadb
======

For setting up MariaDB on an Ubuntu 14.04 or 16.04 server.


Requirements
------------
* Ubuntu

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

Non-trivial:
* mysql_innodb_log_file_size
* mysql_datadir

Other:
* mariadb_mirror: $hostname # Which mirror to pull mariadb apt binaries from

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: acromedia.mariadb }

License
-------

BSD

Author Information
------------------

Acro Media Inc.
https://www.acromedia.com/
