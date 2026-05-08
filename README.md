# Active Directory Lab on Windows Server 2025

## 📑 Table of Contents
- [Overview](#-overview)
- [Installation Process](#%EF%B8%8F-installation-process)
- [Active Directory for IT Usage](#-active-directory-for-it-usage)
- [Resources](#-resources)

---
## 🌐 Overview 
This repository guides you through creating an Active Directory home lab using Windows Server 2025 inside VMware. You will learn how to deploy a Domain Controller, manage users, configure Group Policies, and simulate real IT support tasks.

## 🛠️ Installation Process
#### 1. Install VMware
Download and install **VMware Workstation Pro 17** (free for personal use).

**Steps:**
- Download VMware  
- Run installer  
- Complete setup  
- Restart if needed  

**Reference:** [Install VMware Workstation Pro 17 (YouTube)](https://www.youtube.com/watch?v=1w6CH6eTZhM)

#### 2. Download & Install Windows Server 2025
Start by downloading the ISO: <br/> 
https://info.microsoft.com/ww-landing-evaluate-windows-server-2025.html

**Steps:**
- Create a new virtual machine  
- Mount the Server 2025 ISO  
- Install Windows Server  
- Set up local admin account  
- Run Windows Updates  
- Confirm version using `Winver`

**Reference:** [Install Windows Server 2025 on VMware (YouTube)](https://www.youtube.com/watch?v=SsjV_qYc4GA)

## 🧩 Active Directory for IT Usage


| Topic | Description | Resources |
|---|---|---|
| ✔ **Set Up Active Directory**| Deploy a Domain Controller and configure a new forest | [📄 notes and screenshots](./active-directory-setup/) |
| ✔ **User and Group Management** | Create and manage user accounts and security groups | [📄 notes and screenshots](./user-group-management/notes.md) |
| ✔ **Organizational Units (OUs)** | Organize users and computers into logical containers | [📄 notes and screenshots](./organizational-units/notes.md) |
| ✔ **Group Policy Management** | Enforce settings and rules across the domain | [📄 notes and screenshots](./group-policy-management/notes.md) |
| ✔ **Domain Join Experience** | Simulate joining a Windows client to the domain | [📄 notes and screenshots](./domain-join-experience/notes.md) |
---

### 🎧 Real Helpdesk Scenarios
Practice common IT support tasks that you would handle on the job.

| Scenario | Task |
|---|---|
| User locked out | Unlock account in ADUC |
| Password reset request | Reset password and force change at next login |
| New employee onboarding | Create user, assign to group and OU |
| Employee offboarding | Disable account and remove group memberships |
| Apply software restriction | Create and link a Group Policy to an OU |
| Computer not on domain | Join machine to domain using domain credentials |

---
## 📚 Resources
- Install VMware 17 pro for personal use free [https://www.youtube.com/watch?v=1w6CH6eTZhM]
- Install Windows Server 2025 on VMwaren[https://www.youtube.com/watch?v=SsjV_qYc4GA]
- Practice using Active Directory [https://www.youtube.com/watch?v=GsmJowwIh8Q&t=633s]


---
Last Updated: December 2025