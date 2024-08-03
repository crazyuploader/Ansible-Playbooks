# Ansible-Playbooks

> A collection of Ansible Playbooks created and used during my learning journey with Ansible.

## Overview

This repository contains a variety of Ansible playbooks that automate different system administration tasks. Each playbook is organized by category for easy navigation.

## Playbooks

### Apt

- **[APT Packages Upgrade](apt/upgrade.yml)**: This playbook upgrades all installed APT packages to their latest versions.

### Docker

- **[Docker Cleanup](docker/docker_cleanup.yml)**: This playbook runs `docker system prune -f` to remove unused Docker data including stopped containers, networks, images, and build cache.

### Setup

- **[Add jungle User & Disable Root Login](setup/jungle.yml)**: This playbook creates a new user named `jungle` and disables root login for enhanced security.
- **[Ubuntu Jammy With Docker](setup/ubuntu_jammy_with_docker.yml)**: This playbook sets up a new Ubuntu Jammy instance with Docker installed and configured.

## Usage

To run any of these playbooks, use the following command:

```bash
ansible-playbook path/to/playbook.yml -i your_inventory_file
```
