# ericsymsin.cfnbootstrap

This role was built to deploy the aws-cfn-bootstrap to your servers.

## Build Status

[![Build Status](https://travis-ci.com/ericsysmin/ansible-role-cfnbootstrap.svg?branch=master)](https://travis-ci.com/ericsysmin/ansible-role-cfnbootstrap)

## Requirements

-   python-pip (install via another role or task)

## Role Variables

| Variable                   | Required | Default  | Comments                                 |
| -------------------------- | -------- | -------- | ---------------------------------------- |
| `cfnbootstrap_pkg_version` | No       | `1.4-30` | Sets the version of cfnbootstrap to grab |

## Example Playbook

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  roles:
    - role: ericsysmin.aws.cfnbootstrap
```

## License

MIT

## Author Information

[ericsysmin](https://ericsysmin.com)
