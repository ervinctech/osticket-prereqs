<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket - Prerequisites and Installation

## Overview

This project demonstrates the installation and configuration of osTicket, an open-source help desk ticketing system. The lab covers server preparation, dependency installation, database setup, and successful deployment of the application.

## Technologies Used

- Microsoft Azure
- Internet Information Services (IIS)
- PHP
- MySQL
- HeidiSQL
- osTicket
- Remote Desktop Protocol (RDP)

## Operating Systems Used

- Windows 10 Pro (21H2)

## Skills Demonstrated

- Software Installation
- IIS Configuration
- Database Configuration
- Web Application Deployment
- Troubleshooting
- Help Desk Technologies

## Prerequisites

- Azure Virtual Machine
- IIS Web Server
- PHP Manager
- MySQL Server
- HeidiSQL
- osTicket Installation Files

## Installation Steps

## Step 1: Create Azure Virtual Machine

Created a Windows 10 virtual machine in Microsoft Azure and configured the required networking settings for remote access. After the deployment completed, I connected to the virtual machine using Remote Desktop Protocol (RDP) and verified that the operating system was functioning correctly. This virtual machine served as the environment for hosting and configuring the web server throughout the project.

### Screenshots

**Azure Virtual Machine Created**
![Azure VM Created](https://github.com/ervinctech/osticket-prereqs/blob/ff9a32055989930e3c740ea9d4e9cd51187520c5/Created%20VM%20Photo.png)

**Remote Desktop Connection**
![RDP Connection](images/rdp-connection.png)

**Windows 10 Virtual Machine Desktop**
![Windows 10 VM](images/windows10-vm-desktop.png)

### Step 2: Install IIS

After connecting to a Windows 10 virtual machine through Remote Desktop, I enabled Internet Information Services (IIS) using the Windows Features menu. Once installed, I verified the installation by browsing to localhost and confirmed the IIS web server was operational. I also accessed IIS Manager to review the server configuration

![image](INSERT_SCREENSHOT_HERE)

### Step 3: Install PHP Components

Installed PHP Manager, Rewrite Module, and required dependencies.

![image](INSERT_SCREENSHOT_HERE)

### Step 4: Install MySQL

Installed MySQL Server and verified database services.

![image](INSERT_SCREENSHOT_HERE)

### Step 5: Configure Database

Created the osTicket database using HeidiSQL.

![image](INSERT_SCREENSHOT_HERE)

### Step 6: Install osTicket

Configured application files and completed the installation wizard.

![image](INSERT_SCREENSHOT_HERE)

### Step 7: Verify Deployment

Verified access to both the Admin Panel and User Portal.

![image](INSERT_SCREENSHOT_HERE)

## What I Learned

- How web applications are deployed in a Windows environment.
- Basic IIS administration and configuration.
- Database creation and management using MySQL.
- How ticketing systems support IT operations.
