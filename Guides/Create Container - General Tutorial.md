## This guide provides step-by-step instructions on how to Create a Container using Ubuntu `CT Template`

1. If you are already logged in to Proxmox, the first step is to ***click*** on `Create CT` in the top right corner

![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/6ee54306-eb02-480f-90a1-981d77bf398d)

2.  On `General` tab⤵️<br>
***choose*** the `Node` <sup> or leave the default</sup>, <br>
***set***: `CT ID`, `Hostname`,<br>
***type in*** your root password in the `Password` and `Confirm password` fields

![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/00e2ac21-3a07-4e21-8850-f4cbf52411c9)<br>
you can leave `Unprivileged container` and `Nesting` checkboxes as it is set by default (✅) and ***click*** the `Next` button

3.  On the next (`Template`) tab ➡️ ***select*** the `Storage` location for the downloaded Ubuntu template , and ***choose*** the Ubuntu image for the `Template`.<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/433457e6-6e6c-4ee5-a4fc-8c85abc59334)<br>
and tap on `Next`

4.  `Disks` tab<br>
***select*** the `Storage` where the LXC container will be created, and ***enter*** the `Disk size`<br>
Continue to the next tab

5.  On the `CPU` section, ***choose*** the number of CPUs you want
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/b29c1847-f8d5-48e6-95d4-131dcdde7e5c)<br>
In my example, I'll give it 2 cores<br>
Proceed to the next page

6.  In the 'Memory' section, ***allocate*** as many megabytes as you require and ***press*** `Next`<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/6c55ea30-c415-4292-96e5-32a41d7651c6)<br>
<sup>In my example - I allocated 2048 MB</sup>


7.   `Network` tab:<br>
***Enter*** an IP address that differs from your router's address in the `IPv4/CIDR` field.<br>
***Input*** your router's IP address in the `Gateway` field.<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/2b348125-cf88-4e8a-b2f1-a46546523ebd)
<br>
Leave the remaining fields as they are set by default
Click on ``

8.  Skip the `DNS` tab by clicking `Next`
9.  On the last tab: `Confirm`<br>
Complete the installation by ***press*** on `Finish` button
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/16f0ff0e-4dba-4d54-aaf9-d1792c57833c)

The installation has been completed successfully - a new  container has been created
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/2bf8aff2-85f3-4039-b506-5b81bb2a588a)
