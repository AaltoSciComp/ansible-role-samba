Role Name
=========

This role sets default configurations for samba and allows to override those via variables. Shares are also defined 
as a configurable block. 

Requirements
------------

Written to work as a standalone role. Tested with ansible 1.9.4. 

Role Variables
--------------
```
samba_enabled (default false) - for automation purposes simple switch to disable/enable the role
samba_global (default none) - global configuration for samba
samba_shares (default none) - definition of shares

Examples:

samba_global:
 - "client ldap sasl wrapping": "seal"
 - "client ntlmv2 auth": "true"

samba_shares:
  home:
  - "path": "/export/home"
  - "directory mask": "2770"
```

Dependencies
------------

Written to work as a standalone role. Tested with ansible 1.9.4.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-role-samba }

License
-------

Apache License version 2.0

Author Information
------------------

https://github.com/mhakala
