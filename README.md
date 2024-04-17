<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1. (setup resources in azure)
- Step 2 (ensure connectivity between the client and domain controller)
- Step 3 (install active directory)
- Step 4 (create an admin and normal user account in AD(ACTIVE DIRECTORY)
- Step 5 (join client 1 to your domain (mydomain.com)
- Step 6 (setup remote desktop for non-administrative users on client-1
- Step 7 (create a number of users and attempt to log into client 1)

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/mZdDXt9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/AUpJ6p5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
<img src="https://i.imgur.com/yj03piL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
</p>
<p>
 
Above is a list of deployment and configuration steps to install an active directory on a Windows 10 (21H2). 
Active Directory (AD) is Microsoft's proprietary directory service. It runs on Windows Server and enables administrators to manage permissions 
and access to network resources. Active Directory stores data as objects. An object is a single element, 
such as a user, group, application, or device such as a printer.
</p>
<br />

<p>
<img src="https://i.imgur.com/LHbyytH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
 Above is an image of a VM with an IP address set to static. When a device is assigned a static IP address
 the address does not change. it is ideal for devices on your network that need to be accessed very reliably by
 other systems or devices on the network
</p>
<br />

 
 
 <p>
<img src="https://i.imgur.com/I3hR0Vy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 </p>
 <p>
Above is an example of how to check the connectivity between client-1 and the domain controller by 
 launching the command prompt from the start menu and -t10.2.0.4(perpetual ping). if it's showing (request timed out)
 domain controller's firewall is blocking ICMP traffic. 
</p>
<br />
 
 
 
 <img src="https://i.imgur.com/GjsrG14.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <img src="https://i.imgur.com/YXn7TWK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Above is an example of how to enable the inbound rules for ICMPv4 traffic on the domain controller firewall.
once complete launch the command prompt from the start menu and ping 
-t10.2.0.4(perpetual ping). There should be a reply from the domain controller's IP address ensuring 
connectivity to client-1. 
</p>
<br />

<p>
<img src="https://i.imgur.com/bma7IRd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p> 
<p>
 Above is an example of 
</p>
 
 
 
 <img src="https://i.imgur.com/DA4IdPA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Above is an example of how to setup Active Directory Services and promote the server to the domain controller 
 
</p>
<br />

<p>
<img src="https://i.imgur.com/qjhS95Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/pUqdY7C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Above is an example of how to create an admin and normal user accounts in an active directory
</p>
<br />

<p>
<img src="https://i.imgur.com/jH5wxV2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Above is an example of how to change client-1s DNS settings to the Domain Controller private IP address
</p>
<br />

<p>
<img src="https://i.imgur.com/hd6PeFH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Iaamz1W.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/V2Dqj6O.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Above is an example of how to remote desktop for non-admin users
</p>
<br />
