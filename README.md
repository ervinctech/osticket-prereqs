# osTicket - Prerequisites and Installation

## Overview

This project demonstrates the installation and configuration of osTicket, an open-source help desk ticketing system. The lab covers server preparation, dependency installation, database configuration, application deployment, and post-installation security tasks.

---

## Technologies Used

- Microsoft Azure
- Internet Information Services (IIS)
- PHP 8.4
- MySQL 8.0
- HeidiSQL
- osTicket
- Remote Desktop Protocol (RDP)

---

## Operating Systems Used

- Windows 10 Pro (21H2)

---

## Skills Demonstrated

- Web Application Deployment
- IIS Administration
- PHP Configuration
- Database Configuration
- Software Installation
- Troubleshooting
- File Permission Management
- Security Hardening
- Help Desk Technologies

---

## Prerequisites

Before installing osTicket, the following components were required:

- Windows 10 Virtual Machine
- Internet Information Services (IIS)
- PHP Manager for IIS
- PHP 8.4
- MySQL 8.0
- HeidiSQL
- osTicket Installation Files

---

# Installation Steps

## Step 1: Create Azure Virtual Machine

Created a Windows 10 virtual machine in Microsoft Azure and configured networking settings to allow Remote Desktop access. After deployment, connected to the virtual machine using RDP and verified the operating system was functioning properly.

### Screenshots

![Azure VM Created](images/azure-vm-created.png)

![RDP Connection](images/rdp-connection.png)

![Windows 10 Desktop](images/windows10-desktop.png)

---

## Step 2: Install IIS

Enabled Internet Information Services (IIS) using the Windows Features menu. After installation, verified functionality by browsing to `localhost` and confirming the default IIS webpage loaded successfully. Opened IIS Manager to verify server services and configuration.

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

Installed PHP to enable IIS to host PHP-based web applications. Downloaded PHP, extracted the files, enabled CGI within IIS, and configured FastCGI module mappings. Verified the installation by creating a PHP test page and successfully loading the PHP information page in a browser.

### Screenshots

![PHP Manager Installation](images/php-manager.png)

![CGI Enabled](images/cgi-enabled.png)

![PHP Module Mapping](images/php-module-mapping.png)

![PHP Info Page](images/php-info-page.png)

### Skills Demonstrated

- PHP Installation
- FastCGI Configuration
- IIS Integration
- Application Runtime Configuration

---

## Step 4: Install MySQL

Installed MySQL 8.0 and configured the database server using default development settings. Assigned a root password and configured MySQL to run as a Windows service. Verified successful installation by connecting to MySQL through the command-line client.

### Screenshots

![MySQL Setup Type](images/mysql-setup-type.png)

![MySQL Configuration](images/mysql-configuration.png)

![Root Password Setup](images/mysql-root-password.png)

![MySQL Installation Complete](images/mysql-installed.png)

![MySQL Login Verification](images/mysql-login.png)

### Skills Demonstrated

- Database Installation
- Database Server Configuration
- MySQL Administration

---

## Step 5: Configure Database Using HeidiSQL

Downloaded HeidiSQL and connected to the local MySQL server using the root account. Created a new database named **osTicket** and verified that it appeared within the available databases list.

The database serves as the backend storage location for:

- Tickets
- Users
- Departments
- System Settings
- Email Configurations

### Screenshots

![HeidiSQL Download](images/heidisql-download.png)

![HeidiSQL Connection](images/heidisql-connection.png)

![Database Creation](images/osticket-db-create.png)

![Database Verification](images/osticket-db-created.png)

### Skills Demonstrated

- Database Administration
- Database Creation
- User Privilege Management
- Backend Application Preparation

---

## Step 6: Install osTicket

Downloaded and extracted the latest version of osTicket. Copied the contents of the **upload** folder into the IIS web root directory.

Configured the required file permissions for the `ost-config.php` configuration file and launched the browser-based installation wizard.

The installer automatically checked:

- PHP Requirements
- IIS Configuration
- File Permissions
- Database Connectivity

Configured:

- Help Desk Name
- Administrator Account
- Database Settings
- Database Credentials

After validation, the installer created the required database tables and generated the configuration file.

### Screenshots

![osTicket Download](images/osticket-download.png)

![osTicket Files](images/osticket-files.png)

![Installer Requirements Check](images/osticket-requirements.png)

![Database Setup](images/osticket-database-setup.png)

![Installation Complete](images/osticket-installed.png)

![Admin Login](images/osticket-admin-login.png)

### Skills Demonstrated

- Application Deployment
- PHP Application Configuration
- Database Integration
- Help Desk Platform Installation

---

## Step 7: Post-Installation Security Configuration

After installation completed successfully, performed the recommended security cleanup tasks.

### Security Tasks

- Removed write permissions from `include/ost-config.php`
- Deleted the `setup` directory
- Enabled the osTicket system
- Verified administrator access
- Verified user portal access

These steps prevent unauthorized configuration changes and accidental reinstallation.

### Screenshots

![Config File Permissions](images/config-permissions.png)

![Setup Folder Removed](images/setup-folder-removed.png)

![Admin Dashboard](images/admin-dashboard.png)

![User Portal](images/user-portal.png)

### Skills Demonstrated

- Security Hardening
- Access Verification
- System Administration

---

## Step 8: Verify Deployment

Verified successful deployment by accessing both:

- Admin Control Panel
- End User Support Portal

Confirmed:

- Web Server Functionality
- Database Connectivity
- User Authentication
- Administrative Access
- Application Availability

### Screenshots

![Admin Dashboard Verification](images/admin-verification.png)

![User Portal Verification](images/user-verification.png)

---

## Troubleshooting

If installation issues occur, osTicket provides built-in debugging options.

### Enable Error Display

Locate the following lines in:

- `bootstrap.php`
- `main.inc.php` (older versions)

Default:

```php
ini_set('display_errors',0);
ini_set('display_startup_errors',0);
```

Change to:

```php
ini_set('display_errors',1);
ini_set('display_startup_errors',1);
```

Errors can then be reviewed in:

- Browser Output
- PHP Error Logs
- IIS Logs
- osTicket Dashboard Logs
- Mail Server Logs

### Skills Demonstrated

- Troubleshooting
- Log Analysis
- Error Diagnosis
- Application Support

---

# What I Learned

- How web applications are deployed in a Windows environment.
- How IIS, PHP, and MySQL work together to support web applications.
- How to create and configure databases for application backends.
- How file permissions impact application installation and security.
- Basic security hardening practices for production deployments.
- How ticketing systems support IT help desk operations and service management.
