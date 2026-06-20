# osTicket - Prerequisites and Installation

## Overview

This project demonstrates the installation and configuration of osTicket, an open-source help desk ticketing system, within a Microsoft Azure cloud environment. The project includes deploying a Windows 10 virtual machine, configuring IIS, installing PHP and MySQL, creating a database with HeidiSQL, deploying osTicket, and performing post-installation security tasks.

The purpose of this project was to gain hands-on experience with cloud infrastructure, web servers, databases, and help desk technologies commonly used in IT Support, Help Desk, and System Administration roles.

---

## Technologies Used

- Microsoft Azure
- Azure Virtual Machines
- Windows 10 Pro
- Internet Information Services (IIS)
- URL Rewrite Module
- PHP 8.2
- MySQL 8.0
- HeidiSQL
- osTicket
- Remote Desktop Protocol (RDP)

---

## Operating Systems Used

- Windows 10 Pro (21H2)

---

## Skills Demonstrated

- Cloud Infrastructure Deployment
- Azure Virtual Machine Administration
- Windows Administration
- Remote Desktop Administration
- IIS Configuration and Management
- PHP Configuration
- MySQL Database Administration
- Database Creation and Management
- Web Application Deployment
- Troubleshooting
- Security Hardening
- Help Desk Platform Administration

---

## Project Requirements

Before installing osTicket, the following components were installed and configured:

- Microsoft Azure Account
- Windows 10 Virtual Machine
- Internet Information Services (IIS)
- URL Rewrite Module
- PHP Manager for IIS
- PHP 8.2
- MySQL 8.0
- HeidiSQL
- osTicket Installation Files

---

# Installation Steps

## Step 1: Create Azure Virtual Machine

Created a Windows 10 virtual machine in Microsoft Azure and configured networking settings to allow Remote Desktop access. After deployment, connected to the virtual machine using RDP and verified the operating system was functioning properly.

This virtual machine served as the environment for hosting IIS, PHP, MySQL, and osTicket throughout the project.

### Screenshots

![Azure Virtual Machine Created](images/azure-vm-created.png)

![Remote Desktop Connection](images/rdp-connection.png)

![Windows 10 Virtual Machine Desktop](images/windows10-desktop.png)

### Skills Demonstrated

- Azure Administration
- Virtual Machine Deployment
- Remote Desktop Administration
- Cloud Infrastructure Management

---

## Step 2: Install IIS

Enabled Internet Information Services (IIS) through Windows Features. After installation, verified functionality by navigating to `http://localhost` and confirming that the default IIS webpage loaded successfully.

Opened IIS Manager and verified that all required web services were running properly.

### Screenshots

![IIS Installation](images/iis-installation.png)

![IIS Default Page](images/iis-default-page.png)

![IIS Manager](images/iis-manager.png)

### Skills Demonstrated

- IIS Installation
- Web Server Administration
- Service Verification

---

## Step 3: Install PHP Components

Installed PHP 8.2 and configured IIS to process PHP applications. Enabled the CGI feature, installed PHP Manager for IIS, and configured FastCGI mappings.

Created a PHP test page and verified the installation by successfully loading the PHP information page in a web browser.

### Screenshots

![PHP Manager Installation](images/php-manager.png)

![CGI Enabled](images/cgi-enabled.png)

![PHP FastCGI Mapping](images/php-module-mapping.png)

![PHP Information Page](images/php-info-page.png)

### Skills Demonstrated

- PHP Installation
- FastCGI Configuration
- IIS Integration
- Application Runtime Configuration

---

## Step 4: Install MySQL

Installed MySQL 8.0 and configured the database server. Assigned a root password, configured MySQL to run as a Windows service, and verified successful installation by connecting to the database.

### Screenshots

![MySQL Setup Type](images/mysql-setup-type.png)

![MySQL Server Configuration](images/mysql-configuration.png)

![Root Password Configuration](images/mysql-root-password.png)

![MySQL Installation Complete](images/mysql-installed.png)

![MySQL Login Verification](images/mysql-login.png)

### Skills Demonstrated

- Database Installation
- Database Server Configuration
- MySQL Administration

---

## Step 5: Configure Database Using HeidiSQL

Downloaded and installed HeidiSQL to manage the MySQL database environment.

Connected to the local MySQL server using the root account and created a new database named **osTicket**. Verified the database was successfully created and accessible.

The database serves as the backend storage location for:

- Support Tickets
- User Accounts
- Departments
- Email Configurations
- System Settings

### Screenshots

![HeidiSQL Download](images/heidisql-download.png)

![HeidiSQL Connection](images/heidisql-connection.png)

![Creating Database](images/osticket-db-create.png)

![Database Successfully Created](images/osticket-db-created.png)

### Skills Demonstrated

- Database Administration
- Database Creation
- User Permissions Management
- Backend Application Preparation

---

## Step 6: Install osTicket

Downloaded the latest version of osTicket and extracted the installation package.

Copied the contents of the **upload** folder into the IIS web root directory and configured the required permissions for the `ost-config.php` configuration file.

Launched the browser-based installer and completed the setup process by configuring:

- Help Desk Name
- Administrator Account
- Database Name
- Database Username
- Database Password

The installer automatically verified system requirements, created the necessary database tables, populated the database, and generated the configuration file.

### Screenshots

![osTicket Download](images/osticket-download.png)

![osTicket Files Copied to IIS Directory](images/osticket-files.png)

![Installer Requirements Check](images/osticket-requirements.png)

![Database Configuration](images/osticket-database-setup.png)

![Installation Complete](images/osticket-installed.png)

![Admin Login](images/osticket-admin-login.png)

### Skills Demonstrated

- Web Application Deployment
- PHP Application Configuration
- Database Integration
- Help Desk Platform Installation

---

## Step 7: Post-Installation Security Configuration

After installation completed successfully, performed the recommended security hardening steps.

### Security Tasks Completed

- Removed write permissions from `include/ost-config.php`
- Deleted the `setup` directory
- Enabled the osTicket system
- Verified administrator access
- Verified user portal access

These actions help prevent unauthorized modifications and accidental reinstallation.

### Screenshots

![Configuration File Permissions Updated](images/config-permissions.png)

![Setup Folder Removed](images/setup-folder-removed.png)

![Admin Dashboard](images/admin-dashboard.png)

![User Portal](images/user-portal.png)

### Skills Demonstrated

- Security Hardening
- Access Verification
- System Administration

---

## Step 8: Verify Deployment

Verified successful deployment by accessing both the Administrator Control Panel and End User Support Portal.

Confirmed:

- Web Server Functionality
- Database Connectivity
- User Authentication
- Administrative Access
- Application Availability

### Screenshots

![Admin Dashboard Verification](images/admin-verification.png)

![User Portal Verification](images/user-verification.png)

### Skills Demonstrated

- Application Verification
- System Validation
- Help Desk Administration

---

## Cloud Environment

This project was deployed within Microsoft Azure using a Windows 10 Virtual Machine.

### Azure Components Used

- Azure Virtual Machine
- Virtual Network (VNet)
- Public IP Address
- Network Security Group (NSG)
- Remote Desktop Protocol (RDP)

This cloud-based deployment provided hands-on experience managing infrastructure, networking, remote administration, and application hosting within a modern cloud platform.

---

## Troubleshooting

During installation, osTicket can identify common issues such as:

- Missing PHP extensions
- Database connectivity failures
- File permission errors
- Configuration problems

Common troubleshooting methods included:

- Reviewing IIS logs
- Checking PHP error logs
- Verifying MySQL connectivity
- Confirming file permissions
- Reviewing osTicket dashboard logs

### Skills Demonstrated

- Troubleshooting Methodology
- Log Analysis
- Error Diagnosis
- Application Support

---

# What I Learned

- How to deploy and manage a Windows virtual machine in Microsoft Azure.
- How IIS, PHP, and MySQL work together to support web applications.
- How to create and manage databases using MySQL and HeidiSQL.
- How to deploy and configure a help desk ticketing platform.
- The importance of file permissions during application installation.
- Basic security hardening practices for web applications.
- How ticketing systems support IT operations and service management.
- Real-world troubleshooting techniques used by IT Support and Help Desk professionals.
