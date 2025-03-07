# Move Docker Root Directory

This playbook is designed to move the Docker root directory to a new location on a Debian 12 VM. It stops the Docker service, moves the Docker data, updates the Docker configuration, and restarts the Docker service. Before starting the playbook, configure the values of the [config file](../configs/debian12-move-docker-root.yml).

## Features

- **Stop Docker Service**: Stops the Docker service to ensure data consistency.
- **Move Docker Data**: Moves the Docker data to a new directory.
- **Update Docker Configuration**: Updates the Docker daemon configuration to use the new data root directory.
- **Start Docker Service**: Restarts the Docker service with the new configuration.

## Usage

To run the playbook, use the following command from inside the playbooks folder:

```sh
ansible-playbook debian12-move-docker-root.yml