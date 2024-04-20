## 💾 MS SQL Server onto a Proxmox LXC Container

### **Description**: 
<div>A MS SQL Server instance created in an LXC container is essentially a self-contained environment where SQL Server software is installed and configured to run within the containerized environment provided by Proxmox.

Hosting an MS SQL Server in a properly configured LXC container allows access to it within the local network
</div>

### **How-to run MS SQL Server instance:**<br>
1.  ***Log in*** to Proxmox<br>
2.  ***Download*** Ubuntu CT template (here is [how to do that](www.google.pl))<br>
3.  ***Create*** a Container ([Guide: How to Create a container](Create%20Container%20-%20Ubuntu%20Template.md))<br>
4.  ***Run*** your Container (if You don't know how - [click here](/Guides/How%20to%20Run%20a%20Container.md))<br>
5.  [***Configure***  Ubuntu + ***Download and install*** **MS SQL Server**](Setup%20Ubuntu%20installation%20MS%20SQL%20Server.md)




 **Links:**

[MS Official guide for SQL Server installation ](https://learn.microsoft.com/en-us/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver16&tabs=ubuntu2204)
Choose the storage location for the downloaded Ubuntu image.
