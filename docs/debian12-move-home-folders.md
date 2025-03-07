# Move Home Folder on Debian 12 VM

This playbook is designed to move the home directories of users to a new parent directory on a Debian 12 VM. It ensures the new home directory parent exists, moves the home directories, and updates `/etc/passwd` with the new home directory paths. Before starting the playbook, configure the values of the [config file](../configs/debian12-move-home-folders.yml).


## Features

- **Ensure Directory Exists**: Ensures the new home directory parent exists.
- **Move Home Directories**: Moves the home directories of users to the new parent directory.
- **Update /etc/passwd**: Updates `/etc/passwd` with the new home directory paths for the users.

## Usage

To run the playbook, use the following command from inside the playbooks folder:

```sh
ansible-playbook debian12-move-home-folder.yml