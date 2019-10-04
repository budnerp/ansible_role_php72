# Ansible role for PHP 7.2
Ansible role for PHP 7.2 installation for CentOS 7

## What's inside?
- PHP 7.2.15 (cli)
- Zend OPcache v7.2.15
- Xdebug v2.6.1
- Composer (global)
- Custom settings as per `defaults/main.yml`

##Interesting PHP dirs and files 
    ```
    /etc/php.ini
    /etc/php.d/*
    /etc/php-fpm.conf
    /etc/php-fpm.d/*.conf
    /var/log/php-fpm/www-error.log // as per /etc/php-fpm.d/www.conf
    /var/log/php-fpm/www-slow.log // if enabled
    session.save_path: /var/lib/php/session
    soap.wsdl_cache_dir: /var/lib/php/wsdlcache
    /etc/opt/remi/php72/php.d/
    ```
   
## Tested on
- PHP 7.2.15 (cli)
- Zend OPcache v7.2.15
- Xdebug v2.6.1

## Installation
1. Navigate to Ansible's roles folder
2. Add the repo to git modules
    ```
    git submodule add https://github.com/budnerp/ansible_role_php72.git ansible_role_php72
    ```
3. Add the role to Ansible's playbook file
    ```    
    roles:
    [...]
        - ansible_role_php72
    [...]
    ```

## Other links
- Remi's Wizard help [https://rpms.remirepo.net/wizard/]()
- Remi's FAQ [https://blog.remirepo.net/pages/English-FAQ]()
- Magento 2.3.x technology stack requirements [https://devdocs.magento.com/guides/v2.3/install-gde/system-requirements-tech.html]()
- Magento 2.3 - Required PHP settings [https://devdocs.magento.com/guides/v2.3/install-gde/prereq/php-settings.html]()
- Magento 2.3 - Software recommendations [https://devdocs.magento.com/guides/v2.3/performance-best-practices/software.html]()

## TO DO
-[ ] phpunit 
-[ ] configure sendmail + ;mail.log =
-[ ] define error_log
-[ ] check php-fpm pm.status_path

## License
Copyright (c) We Are Interactive under the MIT license.