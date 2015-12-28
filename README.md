php_extensions
========

Install PHP extensions

Requirements
------------

Debian Wheezy/Jessie with the package python-pycurl and python-software-properties installed.
In addition, it is assumed that the PHP is already installed.

Role Variables
--------------

This roles is used with an array of php extensions as parameter.

For PHP7:

    php_extensions:
        - php7.0-curl
        - php7.0-intl
        - php7.0-gd
        - php7.0-mysql

For PHP5:

    php_extensions:
        - php5-curl
        - php5-intl
        - php5-gd
        - php5-mysql

Dependencies
------------

None.

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - { role: f500.php_extensions, php_extensions["php7.0-curl","php7.0-intl","php7.0-gd","php7.0-mysql"] }

License
-------

LGPL

Author Information
------------------

Jasper N. Brouwer, jasper@nerdsweide.nl

Ramon de la Fuente, ramon@delafuente.nl
