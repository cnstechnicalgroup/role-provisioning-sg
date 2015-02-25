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
| mgmt_subnet_name      |   ---   | Name of the management subnet for the target VPC.                             |
| instance              |   ---   | Object containing instance details (see example).                             |

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
- name: cns.provision-site-sg example
  hosts: localhost
  roles:
    - { role: cns.provisioning-sg, instance: "{{ instance_ec2 }}" }
```
