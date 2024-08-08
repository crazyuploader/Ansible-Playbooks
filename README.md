# Ansible-Playbooks

> A collection of Ansible Playbooks created and used during my learning journey with Ansible.

## Overview

This repository contains a variety of Ansible playbooks that automate different system administration tasks. Each playbook is organized by category for easy navigation.

## Playbooks

### Apt

- **[APT Packages Upgrade](apt/upgrade.yml)**: This playbook upgrades all installed APT packages to their latest versions.

### Cloudflared

- **[Upgrade Cloudflared](cloudflared/upgrade.yml)**: This playbook upgrades installed Cloudflared package to the latest version.

### Docker

- **[Docker Cleanup](docker/docker_cleanup.yml)**: This playbook runs `docker system prune -f` to remove unused Docker data including stopped containers, networks, images, and build cache.
- **[Install Docker & Docker Compose](docker/docker_setup.yml)**: This playbook installs Docker & Docker Compose.

### Ubuntu

- **[Add jungle User & Disable Root Login](ubuntu/jungle.yml)**: This playbook creates a new user named `jungle` and disables root login for enhanced security.
- **[Upgrade & Install Essential Packages](ubuntu/basic_system_provision.yml)**: This playbook sets up the server by installing with essential packages.

## Usage

To run any of these playbooks, use the following command:

```bash
ansible-playbook path/to/playbook.yml -i your_inventory_file
```
