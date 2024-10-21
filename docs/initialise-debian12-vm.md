# Initiliase Debian 12 VM

This playbook is designed to automate the initiation of one or more new Debian12 VMs in the Proxmox cluster. These Debian12 VMs are assumed to be clones of the Debian12Template that can be found on Proxmox, which has the admin user configured and some required apt-packages preinstalled. All template clones will be initially configured with 2 cpu cores and 2 GBs of memory. You can change these values after the initialization script has finished.

Before starting the playbook, create a `hosts.yml` file and set the required values in it according to the [hosts inventory example](../inventory/hosts.yml.example).

## Features

- **Docker Installation**: Installs Docker and Docker Compose.
- **User Management**: Creates user accounts, configures SSH access, and grants sudo privileges to selected users.
- **Network Configuration**: Sets a static IP address and updates the hostname.
- **Security**: Disables password authentication for SSH and forces users to change the default password on first login.
- **Shutdown**: Shuts down the machine after configuration.

## Usage

To run the playbook, use the following command from inside the playbooks folder:

```sh
ansible-playbook initiliase-debian12-vm.yml
```

At the end of the configuration the machine will shutdown. Please set the required resources and manually start the machine in Proxmox.
