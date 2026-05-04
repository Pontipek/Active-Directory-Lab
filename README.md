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

---

### 👤 User & Group Management
Create and manage user accounts and groups inside Active Directory Users and Computers (ADUC).

**Steps:**
1. Open **Active Directory Users and Computers** from Server Manager > Tools
2. Expand your domain (e.g., `corp.local`)
3. Right-click **Users** > **New** > **User**
4. Fill in the first name, last name, and username (e.g., `jsmith`)
5. Set a password and configure password settings
6. Click **Finish** to create the user
7. To create a group, right-click **Users** > **New** > **Group**
8. Name the group (e.g., IT Support), set scope to **Global** and type to **Security**
9. Open the group > **Members** tab > **Add** to assign users

---

### 🗂 Organizational Units (OUs)
OUs let you organize users, computers, and groups into logical containers — similar to folders.

**Steps:**
1. In ADUC, right-click your domain > **New** > **Organizational Unit**
2. Name the OU (e.g., IT Department, HR, Finance)
3. Drag and drop users or computers into the appropriate OU
4. OUs can have Group Policies applied to them individually

---

### 🔒 Group Policy Management
Group Policies let you enforce settings and rules across users and computers in the domain.

**Steps:**
1. Open **Group Policy Management** from Server Manager > Tools
2. Expand your domain > right-click **Group Policy Objects** > **New**
3. Name the policy (e.g., Password Policy, Desktop Lockdown)
4. Right-click the policy > **Edit** to open the Group Policy Editor
5. Navigate to the setting you want to configure (e.g., Computer Configuration > Policies > Windows Settings > Security Settings)
6. Link the policy to an OU by dragging it or right-clicking the OU > **Link an Existing GPO**
7. Run `gpupdate /force` on a client machine to apply changes immediately

---

### 💻 Domain Join Experience
Simulate joining a Windows client machine to your domain.

**Steps:**
1. Set up a second VM running Windows 10 or 11
2. Set its DNS server to the IP address of your Domain Controller
3. Go to **Settings** > **System** > **About** > **Domain or workgroup**
4. Click **Change** and enter your domain name (e.g., `corp.local`)
5. Enter Domain Administrator credentials when prompted
6. Restart the VM
7. Log in using a domain user account (e.g., `corp\jsmith`)

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