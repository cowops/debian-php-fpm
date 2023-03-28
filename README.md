Debian-Php-fpm
==============

PHP FastCGI Process Manager

Requirements
------------

This role requires a debian compliant system such as ubuntu.

Role Variables
--------------

- use_dotdeb: false
- use_sury: false
- php:
  -  version: 8.2
  -  timezone: "Europe/Paris"
  - post_max_size: "8M"
  - upload_max_filesize: "2M"
  - fastcgi_pass: "/run/php/php8.2-fpm.sock"


Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: cowops.debian-php-fpm, php.version: 8.2, php.timezone: "Europe/Paris" }

Tasks
-----

  - Install [php-fpm](https://php.net/manual/fr/install.fpm.php)
  - Setup with default php.ini

License
-------

BSD
