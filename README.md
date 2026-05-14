# MCSA Windows Server Infrastructure Project

## Overview

This project demonstrates the implementation and administration of a complete Windows Server infrastructure environment based on Microsoft Certified Solutions Associate (MCSA) concepts.

The environment was designed and configured in a virtualized lab to simulate a real enterprise network infrastructure including:

* Active Directory Domain Services (AD DS)
* Organizational Units (OU)
* Group Policy Management (GPO)
* DHCP Configuration
* File Sharing & Permissions
* Storage Management
* VPN & RRAS Configuration
* Child Domain Deployment
* User & Group Administration
* Logon Restrictions & Security Policies

---

# Project Objectives

* Build and configure a Primary Domain Controller (PDC)
* Deploy Active Directory infrastructure
* Create and manage users, groups, and organizational units
* Configure DHCP services and network policies
* Apply Group Policies for enterprise security
* Implement file sharing permissions and quotas
* Configure VPN and RRAS services
* Deploy Child Domain Controller
* Implement storage solutions including Spanned, Striped, and Fault-Tolerant volumes

---

# Lab Environment

| Component               | Details                     |
| ----------------------- | --------------------------- |
| Operating System        | Windows Server              |
| Domain Name             | ITISYSADMIN.com             |
| Network Range           | 10.0.0.0/24                 |
| Virtualization Platform | VMware Workstation          |
| Services Used           | AD DS, DHCP, GPO, RRAS, VPN |

---

# Project Tasks

## 1. Primary Domain Controller Installation

* Installed Windows Server
* Promoted server to Primary Domain Controller (PDC)
* Configured forest:

```powershell
ITISYSADMIN.com
```

---

## 2. Active Directory Users & Organizational Units

### Departments Created

* IT Department
* HR Department
* Sales Department

### Users

Each department contains:

* 5 Employees
* 1 Department Manager

Example:

```text
IT1 → IT5
HR1 → HR5
Sales1 → Sales5
```

### Organizational Units (OU)

Created separate OUs for:

* IT
* HR
* Sales

### Delegation

Department managers were granted permissions to:

* Reset passwords
* Create users
* Manage users inside their department OU

---

## 3. DHCP Configuration

Configured DHCP Server with the following settings:

| Setting             | Value       |
| ------------------- | ----------- |
| Network Scope       | 10.0.0.0/24 |
| Excluded IP         | 10.0.0.1    |
| Reservation Example | 10.0.0.100  |
| MAC Filtering       | Enabled     |
| DHCP Backup         | Configured  |

### Features Implemented

* DHCP Scope Creation
* MAC Address Filtering
* IP Reservation
* DHCP Configuration Backup

---

## 4. User Logon Restrictions

Configured:

* Logon Hours
* Workstation Restrictions

### Policy

| Setting                  | Value               |
| ------------------------ | ------------------- |
| Working Days             | Saturday → Thursday |
| Working Hours            | 9:00 AM → 4:00 PM   |
| Login Device Restriction | Enabled             |

---

## 5. Shared Folder Permissions

Created shared folder on:

```text
E:\SharedData
```

### Permissions

| Department | Permission   |
| ---------- | ------------ |
| HR         | Read         |
| Sales      | Change       |
| IT         | Full Control |

---

## 6. Disk Quota Management

Applied storage quota limits:

| User   | Quota  |
| ------ | ------ |
| IT2    | 200 MB |
| Sales2 | 200 MB |

---

## 7. Group Policy Objects (GPO)

Implemented multiple Group Policies:

### Policies Applied

* Hide local drives from users
* Change desktop wallpaper
* Run startup script to open Calculator
* Backup Group Policies

### Example Startup Script

```bat
start calc.exe
```

---

## 8. Child Domain Controller

Configured Child Domain:

```text
NEWGRC.ITISYSADMIN.com
```

### Validation

* User replication tested successfully
* Created test user from PDC and verified on Child DC

---

## 9. VPN Configuration

Configured VPN Server for remote access.

### Features

* Secure remote connectivity
* Authentication configuration
* Remote client access

---

## 10. RRAS Configuration

Configured Routing and Remote Access Services (RRAS).

### Services Enabled

* Routing
* NAT
* VPN Access

---

## 11. Storage Management

Configured dynamic disks and created:

| Volume Type           | Purpose         |
| --------------------- | --------------- |
| Spanned Volume        | Read Storage    |
| Striped Volume        | Performance     |
| Fault-Tolerant Volume | Data Protection |

---

# Skills Demonstrated

## Windows Server Administration

* Active Directory Management
* Domain Controller Deployment
* Group Policy Administration
* DHCP Administration
* VPN & RRAS Configuration
* Storage & Disk Management
* NTFS & Share Permissions
* User & Group Management

## Networking

* TCP/IP Configuration
* DHCP Scope Management
* Network Security Policies
* Remote Access Solutions

## Virtualization

* VMware Workstation
* Virtual Lab Deployment
* Multi-Server Infrastructure

---

# Project Structure

```text
MCSA-Windows-Server-Project/
│
├── README.md
├── screenshots/
│   ├── active-directory/
│   ├── dhcp/
│   ├── gpo/
│   ├── vpn/
│   ├── rras/
│   └── storage/
│
├── scripts/
│   └── startup-script.bat
│
└── documentation/
    └── project-report.pdf
```

---

# Suggested Screenshots

Add screenshots for:

* Active Directory Users and Computers
* DHCP Scope
* GPO Settings
* Shared Folder Permissions
* RRAS Dashboard
* VPN Configuration
* Disk Management
* Child Domain Controller

---

# Technologies Used

* Windows Server
* Active Directory Domain Services
* Group Policy Management
* DHCP Server
* RRAS
* VPN
* VMware Workstation

---

# Author

## Abdelaziz Mohamed

### IT Specialist | System Administrator | Network Engineer

GitHub Profile:

urlGitHub - Abdelaziz Mohamed[https://github.com/abdelazizhedeia](https://github.com/abdelazizhedeia)

---

# License

This project is for educational and training purposes.
