# ansible-redis

[Redis](http://redis.io/) - An open source, BSD licensed, advanced key-value cache and store. It is often referred to as a data structure server since keys can contain strings, hashes, lists, sets, sorted sets, bitmaps and hyperloglogs.

[![Build Status](https://travis-ci.org/telusdigital/ansible-redis.svg?branch=master)](https://travis-ci.org/telusdigital/ansible-redis)
[![Platforms](http://img.shields.io/badge/platforms-ubuntu-lightgrey.svg?style=flat)](#)

Tunables
--------
* ```redis_client``` (boolean)
* ```redis_server``` (boolean)
* ```redis_slave``` (boolean)
* ```redis_server_accepts_external_connections``` (boolean)
* ```redis_sentinel_accepts_external_connections``` (boolean)
* ```redis_sentinel_enabled``` (boolean)
* ```redis_user``` (string) - User to run redis as
* ```redis_group``` (string) - Group to run redis as
* ```redis_server_working_directory``` (string) - Working directory for redis-server
* ```redis_sentinel_working_directory``` (string) - Working directory for redis-sentinel
* ```redis_runtime_root``` (string) - Directory for runtime data
* ```redis_server_pidfile_path``` (string) - Path for redis-server pidfile
* ```redis_server_socket_path``` (string) - Path for redis-server socket
* ```redis_sentinel_pidfile_path``` (string) - Path for redis-sentinel pidfile
* ```redis_sentinel_socket_path``` (string) - Path for redis-sentinel socket
* ```redis_log_root``` (string) - Directory for logs
* ```redis_server_log_path``` (string) - Path for redis-server log
* ```redis_sentinel_log_path``` (string) - Path for redis-sentinel log
* ```redis_master_host``` (string) - address for master redis-server
* ```redis_master_port``` (integer) - port for master redis-server
* ```redis_master_name``` (string) - name for master redis-server
* ```redis_sentinel_quorum``` (interger) - number of sentinels required for quorum

Dependencies
------------
* [telusdigital.apt-repository](https://github.com/telusdigital/ansible-apt-repository/)

Example Playbook
----------------
    - hosts: servers
      roles:
         - role: telusdigital.redis
           redis_server: yes

License
-------
[MIT](https://tldrlegal.com/license/mit-license)

Contributors
------------
* [Chris Olstrom](https://colstrom.github.io/) | [e-mail](mailto:chris@olstrom.com) | [Twitter](https://twitter.com/ChrisOlstrom)
