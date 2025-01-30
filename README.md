# ansible-proxmox
Ansible scripts for managing proxmox hosts.

## Setup
You will need to install the following ansible roles:

* [Proxmox nag removal Role](https://github.com/ironicbadger/ansible-role-proxmox-nag-removal) 
* [Librenms Agent Role](https://github.com/tobias-richter/ansible-librenms-agent)

Installation can be performed with the following commands:

``ansible-galaxy role install IronicBadger.proxmox_nag_removal``

``ansible-galaxy role install tobias_richter.librenms_agent``

## Configuration

Your will need to place your own key in templates/ipsec.secrets. The key can be generated by running: ``openssl rand -base64 128``. The key should be the same for each host using the vxlan.

The vars section of the proxmox-initial.yaml will need to be changed for your snmp settings, as you have configured for Librenms.

## Blog Post

The corresponding blog post for this repository can be found here: [PHP-systems.com Blog](https://blog.php-systems.com/proxmox-host-management-with-ansible/)
