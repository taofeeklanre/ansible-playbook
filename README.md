## Project Overview
This project demonstrates how to automate the configuration of web servers using Ansible to deploy a static website on AWS. By leveraging Ansible's powerful automation capabilities, we streamline the deployment process, ensuring consistency, efficiency, and reliability across multiple servers.

### Introduction:

### Why Automation?

Automation is a cornerstone of modern IT infrastructure management. Imagine having to configure 100 servers manually—this process would be time-consuming, error-prone, and inefficient. Automation addresses these challenges by:

1. Enhancing Efficiency: Automate repetitive tasks to save time and resources.
2. Ensuring Consistency: Maintain uniform configurations across all servers, reducing discrepancies.
3. Improving Reliability: Minimize human errors, leading to more stable and predictable deployments.
4. Scaling Operations: Easily manage and scale infrastructure as your needs grow.

### Why Ansible?
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

1. Ensure you have access to AWS services required for this project.
2. SSH Key Pairs.
3. Generate SSH key pairs for secure access to your AWS instances.
4.  Installed Ansible on Your Server.
5.  Install Ansible on the designated Ansible server in your AWS infrastructure.

## Project Structure
The project is divided into the following main sections:

1. Introduction
2. Prerequisites
3. Step-By-Step Guide
4. Cleanup
5. Contributing
6. License
7. Contact

Each section provides detailed instructions to help you automate the configuration of web servers and deploy a static website on AWS using Ansible.

## Installation and Setup
### Step-By-Step Guide

Follow the steps below to set up and deploy your static website on AWS using Ansible.

1. #### Build a Two-Tier AWS Network VPC

Objective: Set up a Virtual Private Cloud (VPC) with public and private subnets.

Actions:

Create a VPC with CIDR block (e.g., 10.0.0.0/16).

Create public and private subnets within the VPC.

Configure route tables for each subnet.

2. #### Create NAT Gateways

Objective: Provide internet access to instances in private subnets.

Actions:

Allocate Elastic IP addresses.

Create NAT Gateways in public subnets.

Update route tables to route internet traffic through NAT Gateways.

3. #### Create Security Groups

Objective: Define firewall rules for your instances.

Actions:

Create security groups for the Bastion Host, Ansible Server, and Web Servers.

Configure inbound and outbound rules as per project requirements.

4. #### Create Keypairs

Objective: Secure SSH access to your instances.

Actions:

Generate SSH key pairs using ssh-keygen.

Store private keys securely and add public keys to AWS.

5. #### Add the Public SSH Key to GitHub

Objective: Enable secure access to your GitHub repositories from AWS instances.

Actions:

Navigate to GitHub settings.

Add your SSH public key for authentication.

6. #### Launch the Bastion Host Server

Objective: Provide a secure entry point to your AWS network.

Actions:

Launch an EC2 instance in the public subnet.

Configure security groups to allow SSH access.

7. #### Launch the Ansible Server in Private Subnet

Objective: Host Ansible for managing web server configurations.

Actions:

Launch an EC2 instance in the private subnet.

Assign appropriate security groups and IAM roles.

8. #### Launch the EC2 Instances (Web Servers) in the Private Subnets

Objective: Deploy web servers that will host the static website.

Actions:

Launch multiple EC2 instances in private subnets.

Configure security groups to allow necessary traffic.

9. #### Add the Private Key Pair to the Ansible Server

Objective: Enable Ansible to SSH into web servers.

Actions:

Transfer the private key to the Ansible server.

Secure the key with appropriate permissions.

10. #### Create a GitHub Repository to Store the Ansible Playbook

Objective: Version control your Ansible automation scripts.

Actions:

Create a new repository on GitHub.

Clone the repository to your local machine and Ansible server.

11. #### Clone the GitHub Repository on Ansible Server

Objective: Set up the Ansible server with the latest playbooks.

Actions:

Use git clone to clone the repository on the Ansible server.

12. #### Clone the GitHub Repository on Your Computer

Objective: Facilitate local development and updates to playbooks.

Actions:

Use git clone to clone the repository on your local machine.

13. #### Install Ansible on the Ansible Server

Objective: Prepare the Ansible server for automation tasks.

Actions:

Update the package manager and install Ansible.

Verify the installation with ansible --version.

14. #### Create the Ansible Inventory File

Objective: Define the target hosts for Ansible.

Actions:

Create an inventory.ini file listing all web server IPs.

15. #### Use Ansible to Ping the Web Servers to Test Connection

Objective: Ensure Ansible can communicate with all web servers.

Actions:

Run ansible all -m ping -i inventory.ini.

16. #### Create the Ansible Config File

Objective: Configure Ansible settings for your environment.

Actions:

Create an ansible.cfg file with necessary configurations.

17. #### Create Ansible Playbook

Objective: Define tasks to configure web servers and deploy the website.

Actions:

Write playbooks in YAML to install necessary packages and deploy website files.

18. #### Create an Application Load Balancer

Objective: Distribute incoming traffic across web servers.

Actions:

Set up an Application Load Balancer in the AWS Management Console.

Configure target groups and listeners.

19. #### Register a New Domain Name in Route 53

Objective: Manage DNS settings for your website.

Actions:

Use Amazon Route 53 to register and configure your domain name.

20. #### Register for an SSL Certificate in AWS Certificate Manager

Objective: Secure your website with HTTPS.

Actions:

Request an SSL certificate for your domain using AWS Certificate Manager.

21. #### Create an HTTPS Listener for the Application Load Balancer

Objective: Enable secure HTTPS traffic through the load balancer.

Actions:

Configure the load balancer to use the SSL certificate and handle HTTPS requests.

22. #### Create a Record Set in Route 53

Objective: Point your domain to the Application Load Balancer.

Actions:

Create DNS records in Route 53 to route traffic to your load balancer.

After completing the setup and deployment steps, your static website will be accessible via the domain you registered. The automation ensures that your web servers are consistently configured and your website is reliably deployed.

To access your website:

Open your web browser.
Navigate to your registered domain name (e.g., www.zabinets.com) in my own case.
![Architectural Drawing](https://github.com/taofeeklanre/ansible-playbook/blob/main/Web-Page-1.jpg?raw=true)
![Architectural Drawing](https://github.com/taofeeklanre/ansible-playbook/blob/main/Web-Page-2.jpg?raw=true)
![Architectural Drawing](https://github.com/taofeeklanre/ansible-playbook/blob/main/Web-Page-3.jpg?raw=true)
![Architectural Drawing](https://github.com/taofeeklanre/ansible-playbook/blob/main/Web-Page-4.jpg?raw=true)
![Architectural Drawing](https://github.com/taofeeklanre/ansible-playbook/blob/main/Web-Page-5.jpg?raw=true)

Verify that the website loads correctly and functions as expected.

23. #### Create an AMI of the Ansible Server

Objective: Backup and reuse the Ansible server configuration.

Actions:

Create an Amazon Machine Image (AMI) of the Ansible server for future deployments.

24. #### Clean Up
Objective: Remove unnecessary resources to avoid costs.
Actions:
Terminate EC2 instances, delete security groups, and remove other AWS resources no longer needed.

Cleanup
To avoid incurring charges for the AWS resources used in this project, follow these cleanup steps:

Terminate EC2 Instances

Stop and terminate all EC2 instances created for the Bastion Host, Ansible Server, and Web Servers.
Delete NAT Gateways

Remove NAT Gateways to stop incurring costs.
Delete Security Groups

Remove all security groups associated with the project.
Delete VPC and Subnets

Delete the VPC along with its public and private subnets.
Remove Load Balancer and SSL Certificates

Delete the Application Load Balancer and associated SSL certificates from AWS Certificate Manager.
Delete Route 53 Domain and Records

If no longer needed, delete your domain registration and DNS records in Route 53.
Delete GitHub Repositories

Remove the GitHub repository if it’s no longer needed or keep it for future reference.
Delete AMI

Remove the AMI of the Ansible Server if it's no longer required.
Contributing
Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

How to Contribute
Fork the Repository

Click the "Fork" button at the top right of this repository's page on GitHub.
Create a New Branch

git checkout -b feature/YourFeature
Commit Your Changes

git commit -m 'Add some feature'
Push to the Branch

git push origin feature/YourFeature
Open a Pull Request

Navigate to the original repository and open a pull request from your forked repository.
License
This project is licensed under the MIT License.

Contact
For any questions or inquiries, please contact:

Your Name
Email: your.email@example.com
GitHub: your-github-username
Happy automating! 🚀
