Role: cns.provision-site-sg
========

This role configures AWS security groups for a site.

Requirements
------------

Nothing, it runs out of the box.

Role Variables
--------------

In the current version, you can specify the following variables:

| Name                  | Default |                                                                               |
|-----------------------|---------|-------------------------------------------------------------------------------|
| vpc                   |   ---   | Object containint entire VPC structure. Passed from management_vpc playbook.  |
| mode                  |   ---   | Target build environment (dev, test, stage, prod.                             |
| mgmt_subnet_name      |   ---   | Name of the management subnet for the target VPC.                             |
| prefix                |   ---   | Short name for site. e.g. the-world.com becomes theworldcom.                  |
| domain                |   ---   | Primary site domain name. e.g. the-world.com.                                 |
| subdomain             |   ---   | Special environment subdomains for dev, test, and stage.                      |
| ssl_certificate_id    |   ---   | AWS IAM SSL Certificate ID.                                                   |

Dependencies
------------

This package has no dependencies.

License
-------

GPLv2

Author Information
------------------

Created by Sam Morrison
https://www.twitter.com/samcns

Examples
--------

```yaml
---
- name: common role test
  hosts: all
  roles:
    - cns.provision-site-sg
```
