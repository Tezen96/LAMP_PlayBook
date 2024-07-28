# LAMP Playbook

## Overview

This project provides an Ansible playbook for setting up a LAMP stack (Linux, Apache, MySQL, PHP) along with a firewall configuration. It is designed to automate the installation and configuration of a web server, database, and firewall, making it easier to deploy and manage a web application environment.

## Features

- **Install and Configure Firewall**: Sets up and configures Firewalld to manage firewall rules.
- **Database Setup**: Installs and configures MariaDB, creates a database and user.
- **Web Server Setup**: Installs Apache2, PHP, and other web server dependencies, and deploys code from a repository.

## Requirements

- **Ansible**: 2.9 or later
- **Ubuntu**: Tested on Ubuntu 20.04
- **Access to GitHub repository** for code deployment

## Directory Structure

