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



<h1>Step 3</h1>

- Changed Private IP settings for dc-1


<h1>Step 4</h1

- Logged into our domain controller (dc-1) using Windows Remote Desktop



<h1>Step 5</h1

- Used run command to bring up Windows Firewall inside our domain controller



<h1>Step 6</h1
