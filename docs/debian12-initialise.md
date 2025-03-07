# Initiliase Debian 12 VM

This playbook is designed to automate the initiation of one or more new Debian12 VMs in the Proxmox cluster. These Debian12 VMs are assumed to be clones of the Debian12 Templates that can be found on Proxmox, which has the admin user configured and some required apt-packages preinstalled. All template clones will be initially configured with 2 cpu cores and 2 GBs of memory. You can change these values after the initialization script has finished.

Before starting the playbook, ensure that the IP address that the VM is temporarily set at (by the router's DHCP) is listed in the `hosts.yml` file. Then you can configure the values of the [config file](../configs/debian12-initialise.yml).

## Features

- **Docker Installation**: Installs Docker and Docker Compose.
- **Network Configuration**: Sets a static IP address and updates the hostname.

## Usage

To run the playbook, use the following command from inside the playbooks folder:

```sh
ansible-playbook debian12-initiliase.yml
```
