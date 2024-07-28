
# Hotel Booking Website - LAMP Stack Ansible Playbook

## Overview

This project provides an Ansible playbook for deploying a LAMP stack (Linux, Apache, MySQL, PHP) for a Hotel Booking website. It automates the setup of three EC2 instances: one for the master node, one for the database server, and one for the web server. The playbook leverages Ansible roles for modular and organized configuration management.

## Features

- **Firewall Configuration**: Manages firewall rules using Firewalld.
- **Database Setup**: Installs and configures MariaDB, creates a database and user.
- **Web Server Setup**: Installs Apache2 and PHP, deploys the website code from a repository.

## Requirements

- **Ansible**: 2.9 or later
- **Ubuntu 20.04**: The playbook is designed for Ubuntu 20.04 LTS.
- **EC2 Instances**: Three EC2 instances (master, database, and web server).
- **GitHub Repository**: https://github.com/Tezen96/Hotel_Booking_website.
- 

## Installation

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/Tezen96/LAMP_PlayBook.git
    cd LAMP_PlayBook
    ```

2. **Install Ansible**:
    Follow the instructions at [Ansible Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) to install Ansible on your local machine.

3. **Configure Inventory**:
    Edit the `inventory` file to specify the EC2 instances. Define the master node, database server, and web server with their respective IP addresses or hostnames.

4. **Configure Variables**:
    Update any necessary variables in the `db/tasks/main.yml` and `web/tasks/main.yml` files according to your specific configuration needs.

## Usage

1. **Run the Playbook**:
    Execute the Ansible playbook to set up the LAMP stack across the EC2 instances:
    ```bash
    ansible-playbook -i inventory deploy_lamp.yml
    ```

2. **Verify Deployment**:
    After the playbook completes, you should:
    - Access the web server via its public IP address or domain.
    - Verify that the MariaDB server is running and properly configured.
    - Check that the firewall rules are correctly applied.

3. **Access Your Application**:
    Navigate to the IP address or domain of your web server to access the Hotel Booking website.

## Customization

- **Firewall Rules**: Modify the firewall rules in `firewall/tasks/main.yml` to adjust which ports are open.
- **Database Configuration**: Update database settings, including database name and user credentials, in `db/tasks/main.yml`.
- **Web Server Deployment**: Adjust the web server setup and deployment of website code in `web/tasks/main.yml`.

## Troubleshooting

- **Permission Issues**: Ensure that you have the necessary permissions to manage the EC2 instances and run Ansible commands.
- **Service Issues**: Check the status of services on each server using `systemctl` commands or consult the server logs for errors.

## Contributing

Contributions are welcome! Please submit issues or pull requests to improve this playbook.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Author

[Tezen96](https://github.com/Tezen96)


