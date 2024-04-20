## 💾 MS SQL Server onto a Proxmox LXC Container

### **Description**: 
<div>A MS SQL Server instance created in an LXC container is essentially a self-contained environment where SQL Server software is installed and configured to run within the containerized environment provided by Proxmox.

Hosting an MS SQL Server in a properly configured LXC container allows access to it within the local network
</div>

### **How-to:**
1.  ***Log in*** to Proxmox
2.  ***Download*** Ubuntu CT template (here is [how to do that](www.google.pl))<br>

When the download is completed<br>

3.  ***Click on*** `Create CT` in the top right corner

![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/6ee54306-eb02-480f-90a1-981d77bf398d)

4.  On `General` tab⤵️<br>
***choose*** the `Node` <sup> or leave the default</sup>, <br>
***set***: `CT ID`, `Hostname`,<br>
***type in*** your root password in the `Password` and `Confirm password` fields

![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/00e2ac21-3a07-4e21-8850-f4cbf52411c9)<br>
you can leave `Unprivileged container` and `Nesting` checkboxes as it is set by default (✅) and ***click*** the `Next` button

5.  On the next (`Template`) tab ➡️ ***select*** the `Storage` location for the downloaded Ubuntu template , and ***choose*** the Ubuntu image for the `Template`.<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/433457e6-6e6c-4ee5-a4fc-8c85abc59334)<br>
and tap on `Next`

6.  `Disks` tab<br>
***select*** the `Storage` where the LXC container will be created, and ***enter*** the `Disk size`<br>
👉Microsoft's [Ubuntu: Install SQL Server on Linux - Prerequisites](https://learn.microsoft.com/en-us/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver16&tabs=ubuntu2204#prerequisites)
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/a410a0f0-d289-488d-80a8-34d97468336f)<br>
Continue to the next tab

7.  On the `CPU` section, ***choose*** the number of CPUs you want
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/b29c1847-f8d5-48e6-95d4-131dcdde7e5c)<br>
In my example, I'll give it 2 cores<br>
Proceed to the next page

8.  In the 'Memory' section, ***allocate*** as many megabytes as you require and ***press*** `Next`<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/6c55ea30-c415-4292-96e5-32a41d7651c6)<br>
<sup>In my example - I allocated 2048 MB</sup>


9.   `Network` tab:<br>
***Enter*** an IP address that differs from your router's address in the `IPv4/CIDR` field.<br>
***Input*** your router's IP address in the `Gateway` field.<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/0716c914-be9e-4d58-93ab-3248bd7af79b)<br>
Leave the remaining fields as they are set by default
Click on ``

10.  Skip the `DNS` tab by clicking `Next`
11.  On the last tab: `Confirm`<br>
Complete the installation by ***press*** on `Finish` button
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/16f0ff0e-4dba-4d54-aaf9-d1792c57833c)

The installation has been completed successfully - a new  container has been created
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/2bf8aff2-85f3-4039-b506-5b81bb2a588a)




 **Links:**

[MS Official guide for SQL Server installation ](https://learn.microsoft.com/en-us/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver16&tabs=ubuntu2204)
Choose the storage location for the downloaded Ubuntu image.
