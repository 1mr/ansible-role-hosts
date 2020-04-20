Hosts
=====
[![Build Status](https://travis-ci.com/1mr/ansible-role-hosts.svg?branch=master)](https://travis-ci.com/1mr/ansible-role-hosts)

This role helps to configure the /etc/hosts file.

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    hosts:
      - ip: 172.16.1.1
        host: test.example.lcl
        comment: test host
      - ip: 172.16.1.4
        host: git.example.lcl
      
The 'comment' variable is not obligatory.  
You can use the value 'empty' in comment variable to add a blank line.

Some instances with zabbix-proxy or other monitoring tools needs hosts_custom option:

    hosts_custom: yes

Some instances without fqdn hostname needs hosts_fqdn option:

    hosts_fqdn: app1.example.com

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: 1mr.hosts, tags: hosts }

License
-------

MIT

Author Information
------------------

This role was created by Stas Stavnichuk.
