# Mount Drive on Debian 12 VM

This playbook is designed to select and mount a drive on a Debian 12 VM. It ensures the partition exists, creates a filesystem, mounts the drive, and updates `/etc/fstab` for persistent mounting. Before starting the playbook, configure the values of the [config file](../configs/debian12-mount-drive.yml).


## Features

- **Partition Management**: Ensures the partition exists on the selected drive.
- **Filesystem Creation**: Creates an ext4 filesystem on the partition.
- **Mount Drive**: Mounts the drive to the specified mount point.
- **Persistent Mounting**: Updates `/etc/fstab` to ensure the drive is mounted persistently.

## Usage

To run the playbook, use the following command from inside the playbooks folder:

```sh
ansible-playbook debian12-mount-drive.yml