Debian-Php-fpm
==============

PHP FastCGI Process Manager

Requirements
------------

This role requires a debian compliant system such as ubuntu.

Role Variables
--------------

debian:
    version: wheezy
php:
    timezone: "Europe/Paris"
Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: loranger.debian-php-fpm, debian.version: wheezy, php.timezone: "Europe/Paris" }

Tasks
-----

  - Install [php-fpm](https://php.net/manual/fr/install.fpm.php)
  - Setup with default php.ini

License
-------

BSD