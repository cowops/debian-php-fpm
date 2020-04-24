Debian-Php-fpm
==============

PHP FastCGI Process Manager

Requirements
------------

This role requires a debian compliant system such as ubuntu.

Role Variables
--------------

- debian:
  -  version: wheezy
- use_dotdeb: false
- use_sury: false
- php:
  -  version: 7.4
  -  timezone: "Europe/Paris"
  - post_max_size: "8M"
  - upload_max_filesize: "2M"
  - fastcgi_pass: "/run/php/php7.4-fpm.sock"


Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: cowops.debian-php-fpm, debian.version: buster, php.version: 7.4, php.timezone: "Europe/Paris" }

Tasks
-----

  - Install [php-fpm](https://php.net/manual/fr/install.fpm.php)
  - Setup with default php.ini

License
-------

BSD
