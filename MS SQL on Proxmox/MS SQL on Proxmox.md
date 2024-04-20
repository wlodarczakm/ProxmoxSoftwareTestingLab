## 💾 MS SQL Server onto a Proxmox LXC Container

### **Description**: 
<div>A MS SQL Server instance created in an LXC container is essentially a self-contained environment where SQL Server software is installed and configured to run within the containerized environment provided by Proxmox.

Hosting an MS SQL Server in a properly configured LXC container allows access to it within the local network
</div>

### **How-to:**
1.  Log in to Proxmox
2.  Download Ubuntu CT template (here is [how to do that](www.google.pl))<br>

When the download is completed<br>

3.  Click on `Create CT` in the top right corner

![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/6ee54306-eb02-480f-90a1-981d77bf398d)

4.  On `General` tab:<br>
choose the `Node` <sup> or leave the default</sup>, <br>
set: `CT ID`, `Hostname`,<br>
type in your root password in the `Password` and `Confirm password` fields

![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/00e2ac21-3a07-4e21-8850-f4cbf52411c9)<br>
you can leave `Unprivileged container` and `Nesting` checkboxes as it is set by default (✅) and click the `Next` button

5.  On the next tab, select the `Storage` where the LXC container will be created, and choose the Ubuntu image for the `Template`.<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/433457e6-6e6c-4ee5-a4fc-8c85abc59334)<br>
and tap on `Next`

6.  `Disks` tab
7.  sd
8.  sd
9.  ds
10.    

 **Links:**

[MS Official guide for SQL Server installation ](https://learn.microsoft.com/en-us/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver16&tabs=ubuntu2204)
