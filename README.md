Debian-Nginx
============

free, open-source, high-performance HTTP server and reverse proxy, as well as an IMAP/POP3 proxy server

Requirements
------------

This role requires a debian compliant system such as ubuntu.

Role Variables
--------------

nginx:
    php_engine: fpm
    port: 80
    workers: 4

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: loranger.debian-nginx, nginx.php_engine: fpm, nginx.port: 80, nginx.workers: 4 }

Tasks
-----

  - Install [nginx](http://nginx.org/)
  - Setup minimal settings using nginx.conf and defaut enabled website
  - Enable PHP-FPM proxy and copy a simple phpinfo script

License
-------

BSD