### Group Policy Management
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