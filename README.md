## Project Overview
This project demonstrates how to automate the configuration of web servers using Ansible to deploy a static website on AWS. By leveraging Ansible's powerful automation capabilities, we streamline the deployment process, ensuring consistency, efficiency, and reliability across multiple servers.

# Introduction:

## Why Automation?

Automation is a cornerstone of modern IT infrastructure management. Imagine having to configure 100 servers manually—this process would be time-consuming, error-prone, and inefficient. Automation addresses these challenges by:

1. Enhancing Efficiency: Automate repetitive tasks to save time and resources.
2. Ensuring Consistency: Maintain uniform configurations across all servers, reducing discrepancies.
3. Improving Reliability: Minimize human errors, leading to more stable and predictable deployments.
4. Scaling Operations: Easily manage and scale infrastructure as your needs grow.

## Why Ansible?
Ansible is a powerful open-source tool for configuration management, application deployment, and task automation. Its key benefits include:

1. Agentless Architecture: Operates over SSH, eliminating the need for agent installation on managed nodes.
2. Ease of Use: Uses simple YAML syntax for playbooks, making automation accessible even to those with limited coding experience.
3. Consistency: Ensures repeated runs achieve the same results, maintaining system consistency without unnecessary changes.
4. Extensibility: Integrates seamlessly with various platforms and services, including AWS, through its extensive module ecosystem.

### Ansible Project Reference Architecture
![Architectural Drawing](https://github.com/taofeeklanre/ansible-playbook/blob/main/Ansible%20Architectural%20drawing.drawio.png?raw=true)

The reference architecture for this project includes the following AWS resources:

1. VPC
2. Internet Gateway
3. NAT Gateway
4. Security Groups
5. Public and Private Subnets
6. EC2 Instances
7. Application Load Balancer
8. AWS Certificate Manager
9. Route 53

### Objectives
Building on our previous project, this Ansible project aims to:

1. Automate the configuration of web servers using Ansible.
2. Deploy a static website on AWS efficiently.
3. Achieve scalability, consistency, and reliability in deployment processes.
4. Utilize AWS services to support the infrastructure and deployment pipeline.
5. By the end of this project, you will have a fully automated process for deploying and managing a static website on AWS, leveraging the power and simplicity of Ansible.

### Prerequisites
Before you begin, ensure you have the following tools and accounts set up:

A. GitHub Account

#### Why GitHub?
1. Version Control: Host your code and track changes efficiently.
2. Collaboration: Easily collaborate with others by sharing repositories.
3. Issue Tracking: Manage tasks, bugs, and feature requests seamlessly.

### Setup:
Sign up for a free GitHub account.

B. Visual Studio Code

### Why Visual Studio Code?
1. Integrated Development Environment: Write and edit Ansible playbooks with ease.
2. Built-in Git Integration: Manage version control directly within the editor.
3. Extensibility: Enhance functionality with a vast library of extensions.

### Setup:
Download and install Visual Studio Code.

C. AWS Account

Ensure you have access to AWS services required for this project.
SSH Key Pairs

Generate SSH key pairs for secure access to your AWS instances.
Ansible Installed on Your Server

Install Ansible on the designated Ansible server in your AWS infrastructure.
Project Structure
The project is divided into the following main sections:

Introduction
Prerequisites
Step-By-Step Guide
Usage
Cleanup
Contributing
License
Contact
Each section provides detailed instructions to help you automate the configuration of web servers and deploy a static website on AWS using Ansible.
