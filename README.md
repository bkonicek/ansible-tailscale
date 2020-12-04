Role Name
=========

Ansible role to install Tailscale agent on a Linux server.

Requirements
------------

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
         - { role: ansible-tailscale }

License
-------

MIT

Author Information
------------------

This role was created in 2020 by Ben Konicek.