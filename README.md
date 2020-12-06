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

```
NOTE: At this time there is no API for Tailscale, so it's not possible to automatically remove
hosts created by Molecule. Make sure you're doing this after successful CI runs so you don't consume
too many hosts in your account!
```

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
         - { role: ansible-tailscale }

License
-------

MIT

Author Information
------------------

This role was created in 2020 by Ben Konicek.