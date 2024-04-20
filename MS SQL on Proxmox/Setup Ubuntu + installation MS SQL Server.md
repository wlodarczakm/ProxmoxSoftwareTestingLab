# How to setup Ubumtu and Install the MS SQL Server
1. Install gnupg tool - using this command 👉 `apt install gnupg gnupg1 gnupg2` (type `y` and ***press*** Enter - on every prompt `Do you want to continue?`)<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/f634041b-07fc-43d9-82ce-607ec623b3b4)<br>



2. Use next command: `apt install software-properties-common` (type `y` and ***press*** Enter - on every prompt `Do you want to continue?`)<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/0440396c-1936-450f-abfa-7e7796a14299)>br>
software-properties-common" in Ubuntu is a package that contains tools for managing software repositories, such as "add-apt-repository," allowing the addition of new software repositories to the system via a terminal command<br>
You should get result like this:<br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/b279950b-39cf-4093-b384-73ed398a0d48)<br>


3. Install  `curl` - use the command: `apt install curl` (type `y` and ***press*** Enter - on every prompt `Do you want to continue?`) or use a command with an option `-y` 👉 `apt install curl -y` <br>
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/b6b8d1e0-6938-401a-8537-d55e42284b49)<br>

4. Now you can use first command from Microsoft's instruction:<br>
`curl -fsSL https://packages.microsoft.com/keys/microsoft.asc | sudo gpg --dearmor -o /usr/share/keyrings/microsoft-prod.gpg`
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/f8e85a34-af3b-4a53-9a6b-33b4e6bcb841)<br>

and next - step 2- command:<br>
`curl -fsSL https://packages.microsoft.com/config/ubuntu/22.04/mssql-server-2022.list | sudo tee /etc/apt/sources.list.d/mssql-server-2022.list`

5. Use the following commands to install MS SQL Server:<br>
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
6. ***Type in*** `sudo /opt/mssql/bin/mssql-conf setup`<br>
1️⃣ then ***select version*** - in this example, I'm selecting the express version<br>
2️⃣ next prompt ➡️ ***type***: yes and hit Enter<br>
3️⃣ ***create*** sever admin password
![image](https://github.com/wlodarczakm/ProxmoxSoftwareTestingLab/assets/120977639/d0eed908-6429-4b1e-b488-c2a08b8c52ce)

## Now your MS SQL Server is ready to go 👍



