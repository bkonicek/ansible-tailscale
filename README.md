![CI](https://github.com/bkonicek/ansible-tailscale/workflows/CI/badge.svg)

Role Name
=========

Ansible role to install Tailscale agent on a Linux server.

Supported Operating Systems:
- Ubuntu
- CentOS (7 & 8)

Requirements
------------

- Ansible 2.9.x
- [Tailscale](https://tailscale.com/) account and reusable authentication key created.

Role Variables
--------------

The only variable required is `tailscale_key`, the authentication key for Tailscale. It should be provided as an ansible-vault secret to keep it secure.

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars_files:
         - tailscale.yml
      roles:
         - { role: bkonicek.ansible_tailscale }

`tailscale.yml` should be in the following format (just remember to encrypt it first):

```
tailscale_key: 'tskey-abc123...'
```

License
-------

MIT

Author Information
------------------

This role was created in 2020 by Ben Konicek.