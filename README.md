# Ansible Sandbox

## Overview

This repository provides an Ansible sandbox environment for testing and experimenting with Ansible playbooks. It includes predefined host configurations for both Linux and Windows machines and sample playbooks to execute basic tasks.

## Features

- Uses an inventory structure that includes Linux and Windows hosts.
- Provides a basic connection setup using SSH for Linux and SSH with PowerShell for Windows.
- Includes example playbooks that:
- Prompt for SSH credentials.
  - Ping the target machine to verify connectivity.
  - Display the system hostname.

## Prerequisites

- Install Ansible
- Ensure SSH access is available for target machines.
- For Windows, ensure OpenSSH or another SSH service is properly configured.

## Usage

### Clone the Repository

```sh
git clone https://github.com/dcmirandah/ansible-sandbox.git
cd ansible-sandbox-template
```

### Running Playbooks

#### Linux Playbook

`ansible-playbook -i inventory-sample/sandbox/hosts linux.yml`

#### Windows Playbook

`ansible-playbook -i inventory-sample/sandbox/hosts windows.yml`

During execution, you will be prompted to enter the SSH username and password.

## Inventory Structure

The inventory is structured as follows:

```text
inventory-sample/
  sandbox/
    hosts              # Defines the inventory hosts (linux, windows)
    host_vars/
      linux.yml        # Defines SSH settings for Linux
      windows.yml      # Defines SSH settings for Windows
```

## Customization

- Modify `host_vars/linux.yml` and `host_vars/windows.yml` to set up permanent SSH credentials.
- Extend the playbooks (`linux.yml` and `windows.yml)` to include additional tasks.
- Update the inventory file (`hosts`) to include more target machines.

## Contribution

Feel free to contribute by submitting a pull request! 🚀
