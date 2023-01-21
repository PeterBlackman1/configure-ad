<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Configure Active Directiry Domain Services
- Create service accounts 
- Add Hosts to DNS Service
- Install Active Diretory Certificate Servicers Tool

<h2>Deployment and Configuration Steps</h2>

<p>
  
<img width="1440" alt="Screen Shot 2023-01-21 at 2 50 43 PM" src="https://user-images.githubusercontent.com/120864279/213886702-2157a958-8485-4959-96d5-469c75b26115.png">

<p>

Created my resourse group, virtual network and subnet. I set the Domain Controller VM to Windows Server 2021 and named it DC-1

<p>
