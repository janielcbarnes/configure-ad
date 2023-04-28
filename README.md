# configure-ad<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This brief tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Creating Domain Contoller and Client virtual machines in Azure
- Joining the Client and Domain Controller
- Installing Active Directory in Domain Controller VM
- Configure remote desktop for non-admin users in Client VM
<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/lBP0lNx.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
To initiate Active Directory configuration, we would create two virtual machines inside the Acure Porta; Domain Controller and Cliet to see how exacctly the active directory works.  The Domain Controller VM is created with a windows server 2022; this server allows the use of 2 CPUs. After creating the Domain Controller, we would then set the private IP address to static so that it never changes. The Client VM is created with the windows 10 server. After the creation, we would then ensure the connection between the two by use of remote desktop by logigin in to Client VM and pinging DC VM ip (ping -t>ip address).
</p>
<br />

<p>
<img src="https://i.imgur.com/RoBWMjm.png" height="60%" width="60%" alt="active"/>
</p>
<p>
To see the connection between both VMs, they would both need to be open through a remote desktop connection. Then, we would configure rules within the windows firewall to enable the connection. Next, we would install the Active Directory Domain Services through the server manager under Active Directory Users and Computers. Here we would create the organizational units then assign users. 
</p>
<br />

<p>
<img src="https://i.imgur.com/fYiRgPM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After creating the Active Directory in the Domain VM, we would then connect Client VM by changing the DNS settings to the Domain's private IP address and restart the computer. After logging back in, should see user name of Client VM in the active directory. Once there, then we are now able to change permissions of that particular user to possibly the administrator. Now as the administrator, we should then be able to open Powershell and create users as well. 
</p>
<br />
