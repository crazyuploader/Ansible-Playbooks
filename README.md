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

- **[APT Setup Unattended Upgrades](apt/setup-unattended-upgrades.yml)**:
  This playbook installs the `unattended-upgrades` package and configures your system to receive automatic updates for enhanced security and stability.

- **[APT Packages Upgrade](apt/upgrade.yml)**:
  This playbook upgrades all installed APT packages to their latest versions, keeping your system up-to-date.

### Cloudflared

- **[Upgrade Cloudflared](cloudflared/upgrade.yml)**:
  This playbook upgrades the installed Cloudflared package to the latest version, ensuring you have the latest features and security patches.

### Docker

- **[Docker Cleanup](docker/cleanup.yml)**:
  This playbook runs `docker system prune -f` to remove unused Docker data, including stopped containers, networks, images, and the build cache, thus freeing up disk space.

- **[Deploy Docker Prune Timer](docker/deploy-docker-prune-timer.yml)**:
  This playbook creates a Systemd Service/Timer for weekly pruning of unused Docker objects, ensuring that your Docker environment remains clean.

- **[Install Docker & Docker Compose](docker/install.yml)**:
  This playbook installs Docker and Docker Compose, providing a robust platform for containerized applications.

### Fail2ban

- **[Setup Fail2ban](fail2ban/install-and-configure.yml)**:
  This playbook installs Fail2ban and configures it to protect your server from brute-force attacks, particularly on SSH connections.

### GoAccess

- **[Generate Report](goaccess/generate_report.yml)**:
  This playbook generates GoAccess report for Caddy Server.

### Install

- **[Install Caddy Server](install/install-caddy-server.yml)**:
  This playbook install Caddy Server.

- **[Install GoAccess](install/install-goacess.yml)**:
  This playbook install GoAccess.

- **[Install Nginx](install/install-nginx.yml)**:
  This playbook install Nginx Web Server.

- **[Install q](install/install-q.yml)**:
  This playbook installs `q`, a powerful command-line DNS client, facilitating better DNS querying.

- **[Install Rclone](install/install-rclone.yml)**:
  This playbook installs Rclone, a command-line program to manage files on cloud storage.

- **[Install Restic](install/install-restic.yml)**:
  This playbook installs Restic, a program that allows you to backup your files.

### NTP

- **[NTP - Setup Time Synchronization](ntp/install-and-configure.yml)**:
  This playbook installs and configures NTP to keep your server's time synchronized accurately with global time standards.

### Prometheus

#### Node Exporter

- **[Install Node Exporter](prometheus/node_exporter/install.yml)**:
  This playbook installs the Node Exporter, which allows you to collect and report hardware and OS metrics exposed by \*nix kernels, integrated as a systemd service.

- **[Systemd Service Template](prometheus/node_exporter/node_exporter.service.j2)**:
  A Jinja2 template to define the Node Exporter as a systemd service for consistent management and startup.

### Speedtest

- **[Install Speedtest](speedtest/install.yml)**:
  This playbook installs the official CLI from Speedtest.net, allowing you to easily test and measure your internet connection performance.

### SSH Keys

- **[SSH Keys](ssh_keys/add_key.yml)**:
  This playbook adds desired SSH Keys either from GitHub or manually from [ssh_keys/vars/keys.yml](ssh_keys/vars/keys.yml).

### Ubuntu

- **[Add jungle User & Disable Root Login](ubuntu/jungle.yml)**:
  This playbook creates a new user named `jungle` and disables root login for enhanced security of your server.

- **[Upgrade & Install Essential Packages](ubuntu/basic_system_provision.yml)**:
  This playbook sets up your server by installing essential packages, ensuring that your Ubuntu system is ready for basic operations.

## Notes

Ensure you review each playbook and update any necessary variables according to your environment specifics before running them. This will help in avoiding unintended changes to your systems.
