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