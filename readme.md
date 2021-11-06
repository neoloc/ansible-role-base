Base Role
=========

This roles purpose is to configure the base settings that are common to all hosts managed. Settings like the hostname, ``/etc/resolv.conf`` file, common packages, etc.

[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-neoloc.base-blue.svg)](https://galaxy.ansible.com/neoloc/ansible-role-base/)

Requirements
------------

All included in ansible-base package.

Role Variables
--------------

| Variable                | Required | Default | Choices                   | Comments                                 |
|-------------------------|----------|---------|---------------------------|------------------------------------------|
| base.fqdn               | yes      | N/A     | string value              | fully qualified domain name of host      |
| base.hostname           | yes      | N/A     | string value              | hostname (without domain part) of host   |
| base.dns.searchdomain   | no       | N/A     | string value              | searchdomain to be set in /etc/resolv.conf |
| base.dns.forwarders     | no       | 8.8.8.8 | list of IP addresses      | nameservers to be set in /etc/resolv.conf  |

```yaml
base:
  fqdn: somehost.domain.tld
  hostname: somehost
  dns:
    searchdomain: somedomain.tld
    forwarders:
      - 1.1.1.1
      - 9.9.9.9
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - neoloc.base

License
-------

See license.md

Author Information
------------------

[![Github](https://img.shields.io/badge/Github-neoloc-blue.svg)](https://github.com/neoloc)
