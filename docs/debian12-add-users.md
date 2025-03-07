# Add Users to Debian 12 VM

This playbook is designed to add users to a Debian 12 VM. It creates user accounts, configures SSH access, grants sudo privileges to selected users, and sets default passwords. Before starting the playbook, configure the values of the [config file](../configs/debian12-add-users.yml).

## Features

- **User Account Creation**: Creates user accounts with specified home directories and shells.
- **SSH Access Configuration**: Adds public keys to the `authorized_keys` file for SSH access.
- **Sudo Privileges**: Grants sudo privileges to specified users.
- **Default Passwords**: Sets default passwords for user accounts and forces users to change their passwords on first login.

## Usage

To run the playbook, use the following command from inside the playbooks folder:

```sh
ansible-playbook debian12-add-users.yml