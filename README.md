# Jenkins Ansible Automation for Nginx Installation

This project demonstrates the use of Jenkins along with Ansible for automating the installation of Nginx on target systems.

# Prerequisites

## 1.Jenkins Installation:
    Ensure Jenkins is installed, and the Ansible plugin is installed. If not, follow the official Jenkins installation guide and install the Ansible plugin.

## 2.Inventory Setup:
    Fill the inventories file for both prod and testing environments. In the inventory file, set ansible_host to the IP address and ansible_user to the username of the target machines.

## 3.Jenkinsfile Configuration:
    Update the Jenkinsfile with the appropriate values for the following variables:
     PLAYBOOK: Path to your Ansible playbook.
     ESTING_INVENTORY: Path to the testing environment inventory file.
     PRODUCTION_INVENTORY: Path to the production environment inventory file.

## 4.SSH Key Setup:
    Create SSH keys using ssh-keygen.
    Copy the SSH public key to the target machines.
    Ensure the private key's location is specified in the Ansible playbook.
    Set proper permissions on the private key so that Jenkins can access it.

# Getting Started

 ## Run the Jenkins Pipeline:
     Trigger the Jenkins pipeline to execute the Ansible playbook.
     The pipeline will use the configured inventories and playbook to install Nginx on the target machines.
