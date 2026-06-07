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
![RDP Connection](https://github.com/ervinctech/osticket-prereqs/blob/1c6647811c265060ba2e65ff62c00cb98e3c746d/Remote%20Desktop%20Connection.png)

**Windows 10 Virtual Machine Desktop**
![Windows 10 VM](https://github.com/ervinctech/osticket-prereqs/blob/0821e99d9a243a28fa62477c6d9ed8653eed510d/Windows%2010%20VM%20Home%20Screen.png)

## Step 2: Install IIS

After connecting to the Windows 10 virtual machine through Remote Desktop, I enabled Internet Information Services (IIS) using "turn Windows features on or off" menu. Once the installation was complete, I verified that the web server was functioning correctly by browsing to localhost and confirming that the default IIS webpage loaded successfully. I also opened IIS Manager to review the server configuration and ensure the IIS services were running properly.

### Screenshots

**Windows Features - IIS Selected**
![IIS Installation](https://github.com/ervinctech/osticket-prereqs/blob/748aec2ad6edfa78d3ea46baa50b6055d22425e6/IIS%20Enabled.png)

**Default IIS Webpage (localhost)**
![IIS Default Page](https://github.com/ervinctech/osticket-prereqs/blob/20b8669b69933c61832c5ec77fea74355f834b21/Localhost%20Webpage.png)

**IIS Manager**
![IIS Manager](https://github.com/ervinctech/osticket-prereqs/blob/e83432d1b2a7b7d17818481b84b69905d17a4126/How%20to%20find%20IIS.png) ![image](https://github.com/ervinctech/osticket-prereqs/blob/ece31137f39f7a82c0d1bceb001d9f6f14ceb13f/IIS%20Home%20Screen.png)

## Step 3: Install PHP Components

After configuring IIS, I installed PHP to enable the web server to host PHP-based applications. I downloaded the Windows version of PHP, extracted the files to a dedicated directory, and configured the required PHP settings. To allow IIS to communicate with PHP, I enabled the CGI feature within IIS and configured a FastCGI module mapping to the PHP executable. Finally, I verified the installation by creating a PHP test page and confirming that the PHP information page loaded successfully in a web browser.


### Screenshots

**PHP Manager Installation**
![PHP Manager Installation](https://github.com/ervinctech/osticket-prereqs/blob/b4512fc354c4138807a1a74381607ff957a747f3/Download%20and%20Extract.png)

**CGI Feature Enabled**
![CGI Feature Enabled](https://github.com/ervinctech/osticket-prereqs/blob/df1748a6e122823025d566de59622fa2da596c84/CGI%20Confirmation.png)

**PHP FastCGI Module Mapping**
![PHP Module Mapping](https://github.com/ervinctech/osticket-prereqs/blob/013a782c1fb85a9b51eef470daa350abf8e52cd3/Finding%20Module%20Mapping.png) ![image](https://github.com/ervinctech/osticket-prereqs/blob/ac6f49b2b88bfb5f57613a69798f598e7f7e3c0b/Module%20Mapping%20Info.png)

**PHP Test Page Successfully Loaded**
![PHP Info Page](https://github.com/ervinctech/osticket-prereqs/blob/6291341cd4fd8fe07aafb24c9776776c06f01886/PHP%20Test%20Screen.png)

## Step 4: Install MySQL

To provide a database backend for web applications, I installed MySQL using the MySQL Installer for Windows. I selected the Developer Default setup type, which installed MySQL Server, MySQL Workbench, and the required command-line tools. During the configuration process, I configured the MySQL server using the default development settings, assigned a root password, and configured MySQL to run as a Windows service. After the installation was complete, I verified that the database service was running successfully by connecting to MySQL through the command line using the root account.

### Screenshots

**MySQL Installer Setup Type Selection**
![MySQL Setup Type](https://github.com/ervinctech/osticket-prereqs/blob/b31891e2f52c5cd533e741ecb79d31e94a9c1dc5/MySQL%20Website%20Installer.png)

**MySQL Server Configuration**
![MySQL Server Configuration](https://github.com/ervinctech/osticket-prereqs/blob/b31891e2f52c5cd533e741ecb79d31e94a9c1dc5/Config%20Type%20And%20Port%20Choice.png)

**Root Account Configuration**
![MySQL Root Password Setup](https://github.com/ervinctech/osticket-prereqs/blob/b31891e2f52c5cd533e741ecb79d31e94a9c1dc5/Setting%20up%20SQL%20account.png)

**MySQL Installation Completed**
![MySQL Installation Complete](https://github.com/ervinctech/osticket-prereqs/blob/b31891e2f52c5cd533e741ecb79d31e94a9c1dc5/Installation%20Complete.png)

**Successful MySQL Login Verification**
![MySQL Command Line Login](https://github.com/ervinctech/osticket-prereqs/blob/50122fb5f6b37e68137bbfeccd236e58eb123907/MYSQL%20Command%20Prompt%20Confirmation.png)

## Step 5: Configure Database (Create the osTicket Database Using HeidiSQL)

After installing MySQL, I used HeidiSQL to connect to the local MySQL server and create the database required for osTicket. Using the root account, I established a connection to the MySQL instance, created a new database named **osTicket**, and verified that it was successfully added to the list of available databases. This database serves as the backend storage location for osTicket, housing ticket information, user accounts, system settings, and other application data.

### Screenshots

**HeidiSQL Connection to MySQL Server**
![HeidiSQL Connection](INSERT_HEIDISQL_CONNECTION_SCREENSHOT_URL_HERE)

**Creating the osTicket Database**
![Creating osTicket Database](INSERT_DATABASE_CREATION_SCREENSHOT_URL_HERE)

**osTicket Database Successfully Created**
![osTicket Database Created](INSERT_DATABASE_VERIFICATION_SCREENSHOT_URL_HERE)

### Skills Demonstrated

- Database administration
- MySQL configuration and management
- Database creation and verification
- Client-server database connectivity
- Application backend preparation

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
