# Ansible Project: Apache and NTP Configuration

This Ansible project automates the configuration of Apache web server and NTP (Network Time Protocol) service on CentOS 9 servers. It uses roles to organize and manage the configuration tasks, and includes inventories, loops, and conditions to ensure flexibility and efficiency.

## Roles

### Apache Role

The Apache role is responsible for configuring the Apache web server on CentOS 9 servers. It performs tasks such as installing Apache, managing configuration files, and starting the Apache service.

### NTP Role

The NTP role configures the NTP service on CentOS 9 servers to synchronize their system clocks with a designated time server. It installs the NTP package, configures the NTP daemon, and starts the NTP service.

## Inventories

The project includes inventory files to define groups of servers on which the roles will be applied. 

## Playbook

The `apache-playbook.yml` file is the main playbook that orchestrates the execution of the roles on the target servers. It includes tasks to apply both the Apache and NTP roles to the servers defined in the inventory. Conditions and loops are used within tasks to control the execution flow and apply configuration based on specific conditions.

### Conditions

Conditions are used to perform tasks based on certain conditions. For example, in the Apache role, a conditional statement might check if the Apache service is already running before attempting to start it.

### Loops

Loops are used to iterate over a list of items and perform a task for each item in the list. For example, in the NTP role, a loop might be used to configure multiple NTP servers on each CentOS 9 server defined in the inventory.

## Usage

1. Clone this repository to your local machine:

    ```bash
    git clone <repository_url>
    ```

2. Navigate to the project directory:

    ```bash
    cd ansible-project
    ```

3. Update the inventory files (`inventory.ini`) with the IP addresses or hostnames of your CentOS 9 servers.

4. Customize the playbook (`apache-playbook.yml`) if needed, such as specifying variables or adjusting task parameters.

5. Run the playbook to apply the roles to the servers:

    ```bash
    ansible-playbook -i inventory.ini apache-playbook.yml
    ```

6. Sit back and relax as Ansible automates the configuration of Apache and NTP on your servers!

## Notes

- Make sure Ansible is installed on your local machine before running the playbook.
- Ensure SSH access to the target servers is configured properly for Ansible to connect and execute tasks.
- Review the output of the playbook for any errors or warnings, and troubleshoot as needed.
- Experiment with conditionals and loops in your playbooks to customize the configuration based on specific requirements.
