# ansible-three-tier-deployment
Ansible configuration for three tier server deployment

# Deploying a Three-Tier Server Setup with Ansible on Oracle VirtualBox

This guide outlines the steps to deploy a three-tier server setup on Oracle VirtualBox using Ansible. The setup includes:

1. **Application Server:** Flask application running on Python
2. **Web Server:** Apache HTTP server with HTTPS support
3. **Database Server:** MySQL server

Additionally, Ansible will be used for configuration management, and SSH keys will be generated for secure communication between the control machine and the VMs.

## Prerequisites

- Oracle VirtualBox installed and running
- Ansible installed on the control machine VM
- Basic knowledge of Flask, Apache, MySQL, and Ansible

## Step-by-Step Procedure

### 1. Set Up VMs in Oracle VirtualBox

1. **Create Virtual Machines:**
   - **Application Server VM**
   - **Web Server VM**
   - **Database Server VM**
   - **Ansible Control Machine VM**

2. **Configure Network:**
   - Ensure all VMs are on the same network or can communicate with each other.

3. **Install Operating Systems:**
   - Install an appropriate OS (e.g., Ubuntu) on each VM.

### 2. Generate SSH Keys

1. **On the Ansible Control Machine VM:**
   - Generate a new SSH key pair to facilitate secure communication with the other VMs.

### 3. Set Up the Application Server

1. **Install Python and Flask:**
   - Install Python and Flask on the Application Server VM.

2. **Deploy Flask Application:**
   - Deploy your Flask application to the Application Server VM.

### 4. Set Up the Web Server

1. **Install Apache HTTP Server:**
   - Install Apache HTTP server on the Web Server VM.

2. **Configure HTTPS:**
   - Set up SSL/TLS certificates and configure Apache for HTTPS.

3. **Set Up Reverse Proxy:**
   - Configure Apache to proxy requests to the Flask application on the Application Server VM.

### 5. Set Up the Database Server

1. **Install MySQL Server:**
   - Install MySQL on the Database Server VM.

2. **Configure MySQL:**
   - Secure MySQL installation and create necessary databases and users.

### 6. Configure Ansible

1. **Create Ansible Inventory:**
   - Define the inventory file with the IP addresses and hostnames of your VMs.

2. **Write Playbooks:**
   - Create Ansible playbooks to automate the setup and configuration of the Application Server, Web Server, and Database Server.

3. **Configure SSH Access:**
   - Add the SSH public key generated earlier to the `authorized_keys` on each VM to allow Ansible to connect.

### 7. Deploy with Ansible

1. **Run Ansible Playbooks:**
   - Execute the Ansible playbooks from the control machine to configure and deploy the application, web server, and database server.

### 8. Verify Deployment

1. **Check Services:**
   - Verify that the Flask application is accessible through the web server.
   - Confirm that the web server is properly handling HTTPS requests.
   - Ensure that the database server is correctly set up and accessible.

2. **Test End-to-End:**
   - Test the complete workflow from the web server through to the application server and database server.

## Troubleshooting

- Check VM network settings and ensure they are properly configured.
- Verify SSH access between the control machine and other VMs.
- Review Ansible playbook output for any errors during deployment.

## Conclusion

This README provides a high-level overview of deploying a three-tier server architecture using Ansible on Oracle VirtualBox. Ensure to replace placeholder values with actual configurations and adapt the steps as needed for your specific environment.


