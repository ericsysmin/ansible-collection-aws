# Ansible Collection - ericsysmin.aws

Ansible collection that holds roles, that can be used to configure common AWS items.

## Roles

| Role         | Build Status                                                                                                                                                                                                                                                  | Documentation                                                                                          |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| cfnbootstrap | [![Role: ericsysmin.aws.cfnbootstrap](https://github.com/ericsysmin/ansible-collection-aws/workflows/ericsysmin.aws.cfnbootstrap/badge.svg)](https://github.com/ericsysmin/ansible-collection-aws/actions?query=workflow%3A%22ericsysmin.aws.cfnbootstrap%22) | [Documentation](https://github.com/ericsysmin/ansible-collection-aws/blob/master/docs/cfnbootstrap.md) |

## Usage

You can find specific to each role within the "Documentation" link for each role. However, most should be in this format.

```yaml
---
- hosts: localhost
  connection: local
  tasks:
    - name: Include role
      include_role:
        name: ericsysmin.aws.<role_name>
      vars:
        var1: value1
        var2: value2
```

## Testing

Testing is done through GitHub Actions, and can be tested locally as well. GitHub Actions can be located [here](https://github.com/ericsysmin/ansible-collection-aws/actions).
Each workflow pertains to a single role, and can be launched locally using the following command:

```bash
MOLECULE_COMMAND={{ matrix.molecule_distro.command }} \
MOLECULE_DISTRO={{ matrix.molecule_distro.distro }} \
molecule --debug test -s {{ matrix.collection_role }}
```

To decide on the `MOLECULE_COMMAND` value please refer to the `.github/workflow/{{ collection_role }}.yml` file as it will have the value for proper systemd services.
