# Ansible-Playbooks

> A collection of Ansible Playbooks created and used during my learning journey with Ansible.

## Overview

This repository contains a variety of Ansible playbooks that automate different system administration tasks. Each playbook is organized by category for easy navigation.

## Usage

To run any of these playbooks, use the following command:

```bash
ansible-playbook path/to/playbook.yml -i your_inventory_file
```

## Playbooks

### Apt

- **[APT Setup Unattended Upgrades](apt/setup-unattended-upgrades.yml)**: This playbook installs `unattended-upgrades` package and configures it automatic updates.
- **[APT Packages Upgrade](apt/upgrade.yml)**: This playbook upgrades all installed APT packages to their latest versions.

### Cloudflared

- **[Upgrade Cloudflared](cloudflared/upgrade.yml)**: This playbook upgrades installed Cloudflared package to the latest version.

### Docker

- **[Docker Cleanup](docker/cleanup.yml)**: This playbook runs `docker system prune -f` to remove unused Docker data including stopped containers, networks, images, and build cache.
- **[Install Docker & Docker Compose](docker/install.yml)**: This playbook installs Docker & Docker Compose.

### Fail2ban

- **[Setup Fail2ban](fail2ban/install-and-configure.yml)**: This playbook installs Fail2ban and configures it for SSH connections.

### NTP

- **[NTP - Setup Time Synchronization](ntp/install-and-configure.yml)**: This playbook installs NTP and configures it for time synchronization.

### Prometheus

#### Node Exporter

- **[Install Node Exporter](prometheus/node_exporter/install.yml)**: This playbook installs Node Exporter and configures it to run as a systemd service.

### Ubuntu

- **[Add jungle User & Disable Root Login](ubuntu/jungle.yml)**: This playbook creates a new user named `jungle` and disables root login for enhanced security.
- **[Upgrade & Install Essential Packages](ubuntu/basic_system_provision.yml)**: This playbook sets up the server by installing with essential packages.
