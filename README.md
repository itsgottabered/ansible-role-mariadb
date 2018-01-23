mariadb
======

For setting up MariaDB on an Ubuntu 14.04 or 16.04 server.


Requirements
------------
* Ubuntu

Role Variables
--------------
* mysql_max_allowed_packet
* mysql_transaction_isolation
* mysql_binlog_format
* mysql_max_connections
* mysql_expire_logs_days
* mysql_general_log_file
* mysql_general_log
* mysql_slow_query_log
* mysql_slow_query_log_file
* mysql_long_query_time
* mysql_innodb_log_file_size
* mysql_datadir

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
