
1. Click on a container - You can view a summary of your container <br>
![1](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/f221ca3f-9823-4dfd-8837-47e5d1a46a8d)


2. ***Press*** `Start` button to run a container<br>
![2](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/3ecaa0a2-55f3-4e99-8008-67c5e2c78a86)
3. ***Go to*** the `Console` section - you will see CUI - ***type in*** login: root and ***hit Enter*** on your keyboard
![3](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/6bcb2a0d-1def-49a4-8661-ffff9d643776)

4. Now, put in the password you created during the container creation then ***press the Enter*** button on your keyboard<br>
![4](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/283cee78-e8e8-4028-9fe3-0917bffd43c0)

5. ***Type*** `apt update -y` and press Enter to confirm <br>
![5](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/6b88cb2c-dd63-4aa3-b27a-2fd1d467d6a4)<br>
you will get result like this:<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/3e1d9f12-a52a-4f8c-a7d3-ac187ed64488)<br>
now (like a command above) you can use: `apt upgrade -y` to update all installed packages on the operating system to their latest available versions
6. Install gnupg tool - using this command 👉 `apt install gnupg gnupg1 gnupg2` (type `y` and ***press*** Enter - on every prompt `Do you want to continue?`)<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/f634041b-07fc-43d9-82ce-607ec623b3b4)<br>



7. Use next command: `apt install software-properties-common` (type `y` and ***press*** Enter - on every prompt `Do you want to continue?`)<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/0440396c-1936-450f-abfa-7e7796a14299)>br>
software-properties-common" in Ubuntu is a package that contains tools for managing software repositories, such as "add-apt-repository," allowing the addition of new software repositories to the system via a terminal command<br>
You should get result like this:<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/b279950b-39cf-4093-b384-73ed398a0d48)<br>


8. Install  `curl` - use the command: `apt install curl` (type `y` and ***press*** Enter - on every prompt `Do you want to continue?`) or use a command with an option `-y` 👉 `apt install curl -y` <br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/b6b8d1e0-6938-401a-8537-d55e42284b49)<br>

9. Now you can use first command from Microsoft's instruction:<br>
`curl -fsSL https://packages.microsoft.com/keys/microsoft.asc | sudo gpg --dearmor -o /usr/share/keyrings/microsoft-prod.gpg`
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/f8e85a34-af3b-4a53-9a6b-33b4e6bcb841)<br>

and next - step 2- command:<br>
`curl -fsSL https://packages.microsoft.com/config/ubuntu/22.04/mssql-server-2022.list | sudo tee /etc/apt/sources.list.d/mssql-server-2022.list`

10. Use the following commands to install MS SQL Server:<br>
- `apt update` - if you receive a warning like this:<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/00bd4a82-35a3-452f-98a9-fb0393df2f1e)<br>
use second command from Microsoft's guide([ss above](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/f8e85a34-af3b-4a53-9a6b-33b4e6bcb841)) - step 1 
`curl https://packages.microsoft.com/keys/microsoft.asc | sudo tee /etc/apt/trusted.gpg.d/microsoft.asc`<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/76d30832-7dda-4c1e-aa4c-decd3b85a036)<br>
then use:<br>
- `apt install -y mssql-server`<br>
you will get output like this:<br>
`Please run 'sudo /opt/mssql/bin/mssql-conf setup'`<br>
`to complete the setup of Microsoft SQL Server`<br>
`+--------------------------------------------------------------+`<br>
`Processing triggers for man-db (2.10.2-1) ...`<br>
`Processing triggers for libc-bin (2.35-0ubuntu3.7) ...`<br>
11. ***Type in*** `sudo /opt/mssql/bin/mssql-conf setup`<br>
1️⃣ then ***select version*** - in this example, I'm selecting the express version<br>
2️⃣ next prompt ➡️ ***type***: yes and hit Enter<br>
3️⃣ ***create*** sever admin password
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/d0eed908-6429-4b1e-b488-c2a08b8c52ce)

## Now your MS SQL Server is ready to go 👍



