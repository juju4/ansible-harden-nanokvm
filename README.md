# Hardening NanoKVM ansible role

[![Actions Status - Main](https://github.com/juju4/ansible-adduser/workflows/AnsibleCI/badge.svg)](https://github.com/juju4/ansible-adduser/actions?query=branch%3Amain)
[![Actions Status - Devel](https://github.com/juju4/ansible-adduser/workflows/AnsibleCI/badge.svg?branch=devel)](https://github.com/juju4/ansible-adduser/actions?query=branch%3Adevel)

A simple ansible role to do system hardening on [NanoKVM](https://github.com/sipeed/NanoKVM/). Mostly

* Firewall enforcing restricted network traffic
* Configure custom DNS server
* Configure more restricted ssh config

## Requirements & Dependencies

### Ansible

It was tested on the following versions:

* 13 (core 2.20)

### Operating systems

Tested on NanoKVM 2.3.

## Example Playbook

Just include this role in your list.
For example

```yaml
- host: myhost
  roles:
    - juju4.harden_nanokvm
```

you probably want to review variables

## Variables

TBD

## Continuous integration

```shell
pip install molecule docker
molecule test
MOLECULE_DISTRO=ubuntu:24.04 molecule test --destroy=never
```

## Troubleshooting & Known issues

TBD

## Resources

* nameserver https://github.com/sipeed/NanoKVM/issues/210 https://github.com/sipeed/NanoKVM/issues/399 https://github.com/sipeed/NanoKVM/issues/311#issuecomment-2658954062
* firewall https://github.com/sipeed/NanoKVM/issues/301#issuecomment-3172900815

## License

BSD 2-clause
