# vagrant-centos7

CentOS 7 Vagrant environment for development.

## Prerequisites:

- [Vagrant](https://www.vagrantup.com)
- [VirtualBox](https://www.virtualbox.org)

## Getting Started

1. Start the vm.

    ```
    vagrant up
    ```

2. Log into the vm:

    ```
    vagrant ssh
    ```

## Mount Points

- `/projects` Parent folder from the host relative from this repository.
- `/vagrant` Local folder from the host.

## Installed Dependencies

- Docker 1.12
- PostgreSQL 9.5
- Python 3.4
