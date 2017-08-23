# Ansible Role: SSH Keypair

Copies SSH Keypair to the homedir of the given user.

## Requirements

No special requirements.

## Dependencies

None.

## Example Playbook

    - hosts: servers
      vars_files:
        - vars/ssh_keypair.yml
      roles:
        - { role: net2grid.ssh_keypair }

Inside `vars/ssh_keypair.yml` (note the pipe and spacing for the private key!):

    user: root
    homedir: /root
    key_private: |
      -----BEGIN RSA PRIVATE KEY-----
      YiAyGtywXvqcy392xWskk1E8tz6ZNMO0PiNYCx+fLUOwy2lc3G5sBgVEQCBasdxd
      Fxx9H+VwmNpZXopQtBguuhijfbeX8IHn8voBo9EtTOl4tyEsnLHfyVWAqL3vFXHi
      -----END RSA PRIVATE KEY-----
    key_public: "ssh-rsa AAAAB3NzaC1yc2EAAIlh4aKFgC1CcosaReT+921DT9UHLuTOj2Qb69 root@vm"

## License

MIT / BSD

## Author Information

This role was created in 2017 by NET2GRID BV.
