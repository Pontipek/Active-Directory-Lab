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

**YouTube Video:** *(coming soon)*

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

**YouTube Video:** *(coming soon)*

#### 3. Set Up Active Directory
- Open **Server Manager**  
- Select **Add Roles and Features**  
- Choose **Role-based installation**  
- Enable **Active Directory Domain Services**  
- Install → Promote to Domain Controller  
- Create a new forest: `corp.local`  
- Restart the server  
- Log in as the Domain Administrator  

You should have a working **Domain Controller** after following the steps above.

## 🧩 Active Directory for IT Usage
#### ✔ User & Group Management  
#### ✔ Organizational Units (OUs)
#### ✔ Group Policy Management 
#### ✔ Domain Join Experience 
#### ✔ Real Helpdesk Scenarios

## 📚 Resources
- Install VMware 17 pro for personal use free [https://www.youtube.com/watch?v=1w6CH6eTZhM]
- Install Windows Server 2025 on VMwaren[https://www.youtube.com/watch?v=SsjV_qYc4GA]
- Practice using Active Directory [https://www.youtube.com/watch?v=GsmJowwIh8Q&t=633s]


---
Last Updated: December 2025