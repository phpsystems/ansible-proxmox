# ansible-proxmox
Ansible scripts for managing proxmox hosts.

## Setup
You will need to install the following ansible roles:

[Proxmox nag removal](https://github.com/ironicbadger/ansible-role-proxmox-nag-removal) 


## Configuration

Your will need to place your own key in templates/ipsec.secrets. The key can be generated by running: ``openssl rand -base64 128``. The key should be the same for each host using the vxlan.

The vars section of the proxmox-initial.yaml will need to be changed for your snmp settings, as you have configured for Librenms.

