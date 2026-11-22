<p align= "center">
<img src= "https://imgur.com/ZGyg1pf.png"/>
</p>

<h1>Managing Active Directory</h1>
In this tutorial, I'll demonstrate how a user can utilize Active Directory from Azure.

<h2>Environments & Technologies Used</h2>

- Microsoft Azure
- Remote Desktop
- Powershell
- Active Directory Domain Services

<h2>Operating Systems Used</h2>

- Windows 10
- Windows Server 2022

<h2>Configuration Steps</h2>

- Prepare AD Infrastructure
- Deploy Active Directory
- Create Users With PowerShell
- Group Policy & Managing Accounts

<h1>Step 1</h1>

- Created a Domain Controller running windows server and VM running window 10 Pro along with a VNET
<img width="1374" height="569" alt="image" src="https://github.com/user-attachments/assets/175eeaba-2b93-4869-9839-c227a1581be9" />


<h1>Step 2</h1>

- Clicked on Virtual NIC that dc-1 uses to configure its IP settings (change it from dynamic to static)
<img width="1148" height="544" alt="image" src="https://github.com/user-attachments/assets/96c948bb-019c-41d2-af3b-050f66331075" />


<h1>Step 3</h1>

- Changed Private IP settings for dc-1
<img width="1289" height="650" alt="image" src="https://github.com/user-attachments/assets/c4c6394a-62bd-431d-918b-57b139eacd9a" />


<h1>Step 4</h1>

- Logged into our domain controller (dc-1) using Windows Remote Desktop
<img width="1289" height="650" alt="image" src="https://github.com/user-attachments/assets/abc11eca-0811-4b5f-86ef-84187aaeb866" />


<h1>Step 5</h1>

- Used run command to bring up Windows Firewall inside our domain controller
<img width="481" height="350" alt="image" src="https://github.com/user-attachments/assets/9e34ac5a-20d4-42d3-a716-204d55d43812" />


<h1>Step 6</h1>
            
- Turned all firewalls off inside dc-1 (for the sake of the lab)
<img width="1164" height="810" alt="image" src="https://github.com/user-attachments/assets/19c1dc6d-57df-4034-9435-d9808e6ef1fb" />


<h1>Step 7</h1>

- Copied dc-1s private IP address and made client-1 point to that DNS server by adding private IP address to client-1s DNS servers inside its Network Interface Card look to dc-1 for info
<img width="1112" height="721" alt="image" src="https://github.com/user-attachments/assets/7ffa8b70-e5bc-458f-a3a0-7712f7671c29" />


<h1>Step 8</h1>

- Logged into client-1 VM using Remote Desktop opened Windows Powershell to successfully ping dc-1s private IP
<img width="748" height="501" alt="image" src="https://github.com/user-attachments/assets/62623987-2b49-4272-b994-d08f9459f054" />


<h1>Step 9</h1>

- Ran a command in Windows Powershell to observe that client-1s DNS server is pointing to our domain controller (dc-1)
<img width="852" height="677" alt="image" src="https://github.com/user-attachments/assets/147663d7-c43c-4785-adf1-b09638c29681" />


<h1>Step 10</h1>

- Back in dc-1 we ran the same command and observed dc-1s DNS server is still the VNet server
<img width="975" height="516" alt="image" src="https://github.com/user-attachments/assets/12a3adde-5f0d-4be8-b711-53c0fbfaf2c3" />


<h1>Step 11</h1>

- Within dc-1 using Server Manager we installed Active Directory Domain Services feature to our server
<img width="1618" height="752" alt="image" src="https://github.com/user-attachments/assets/0c5b9809-2dda-44ca-8a13-c711ebea37c3" />


<h1>Step 12</h1>

- Promoted dc-1 to a Domain Controller by adding a new forest within Server Manager (mydomain)
<img width="1651" height="900" alt="image" src="https://github.com/user-attachments/assets/809ae819-0986-4bb2-a4a7-5495ab9a921b" />


<h1>Step 13</h1>

- Logged back in to dc-1 using domain name and username (not signing in locally)
<img width="1698" height="1080" alt="image" src="https://github.com/user-attachments/assets/eae6ebc3-916c-4848-b92c-6de8416bd2ca" />



<h1>Step 14</h1>

- Inside dc-1 Active Directory Users and Computers we added two new organizational Units (OU)
<img width="1317" height="778" alt="image" src="https://github.com/user-attachments/assets/0d36506f-2dce-45f7-8c95-d234f3de4012" />








