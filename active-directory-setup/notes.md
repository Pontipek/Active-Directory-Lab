### Set Up Active Directory

## Step 1: Set a Static IP Address
 
Before installing Active Directory, assign a static IP so the server's address does not change.
 
> Before picking an IP, check your current network range. Open **Command Prompt** and run:
> ```
> ipconfig
> ```
> If your current IP is something like `192.168.1.x`, then `192.168.1.50` is fine. If it is `10.0.0.x`, use something like `10.0.0.50` instead.
 
1. Open **Server Manager**
2. Click **Local Server** on the left
3. Next to **Ethernet**, click the blue network link
4. Right-click your network adapter (usually **Ethernet0**)
5. Click **Properties**
6. Select **Internet Protocol Version 4 (TCP/IPv4)**
7. Click **Properties**
8. Select **Use the following IP address**
9. Enter your static IP settings — example:
| Field | Example Value |
|---|---|
| IP Address | 192.168.1.50 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.1.1 |
| Preferred DNS | 192.168.1.50 |
| Alternate DNS | 8.8.8.8 |
 
10. Click **OK** to save
> Set the Preferred DNS to the server's own IP address. Domain Controllers run their own DNS service, so the server needs to point to itself.
 
## Step 2: Add Roles and Features

1. Open **Server Manager**
2. Click **Manage** in the top-right corner
3. Select **Add Roles and Features**
4. Click **Next** on the Before You Begin page
6. Select **Role-based or feature-based installation** > click **Next**
7. Choose your local server (e.g., `DC01`) > click **Next**
---
 
## Step 3: Enable Active Directory Domain Services
 
1. On the server roles page, check **Active Directory Domain Services**
2. When prompted, click **Add Features**
3. Click **Next** through the Features page (leave defaults)
4. Click **Next** through the AD DS info page
5. Click **Install** on the confirmation page
6. Wait for the installation to complete
> The server is not yet a Domain Controller — that happens in the next step.
 
---
 
## Step 4: Promote to Domain Controller
 
1. In Server Manager, click the **notification flag** in the top-right corner
2. Select **Promote this server to a domain controller**
3. On the deployment page, select **Add a new forest**
4. Enter the root domain name: `corp.local` > click **Next**
---
 
## Step 5: Configure Domain Controller Options
 
1. Leave **DNS server** and **Global Catalog (GC)** checked
2. Set a **Directory Services Restore Mode (DSRM)** password
3. Save this password somewhere safe — it is used for recovery and is separate from the admin password
4. Click **Next**
---
 
## Step 6: Finish Configuration
 
1. **DNS Options** — you may see a delegation warning, this is normal in a lab > click **Next**
2. **NetBIOS name** — confirm it shows `CORP` > click **Next**
3. **Paths** — leave the default database, log, and SYSVOL paths > click **Next**
4. **Review** — confirm your settings > click **Next**
5. Wait for prerequisite checks to pass > click **Install**
The server will now configure Active Directory, install DNS, create the forest, and promote itself to a Domain Controller.
 
---
 
## Step 7: Restart and Log In
 
1. The server will restart automatically after installation
2. At the login screen, log in as the Domain Administrator:
```
CORP\Administrator
```
 
or
 
```
Administrator@corp.local
```
 
---
 