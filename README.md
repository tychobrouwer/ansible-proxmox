Configure Proxmox VE
=========

The role configures Proxmox VE on my server.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Example Playbook
----------------

```yaml
    - hosts: servers
      vars:
      proxmox_pbs_client:
        password: ""
        fingerprint: ""
      proxmox_pbs_client_directories:
          - file-share.pxar:/media/file-share
          - lxc-config.pxar:/etc/pve/lxc

      proxmox_smtp:
        email: ""
        password: ""
        host: smtp.gmail.com
        port: 587

      roles:
         - { role: tychobrouwer.proxmox, proxmox_pbs_repository: backup@pbs@192.168.1.108:main, proxmox_enable_ha_services: true, proxmox_enable_pbs_client: true }
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
