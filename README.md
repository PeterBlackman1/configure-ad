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
  
<img width="1440" alt="Screen Shot 2023-01-29 at 9 50 32 AM" src="https://user-images.githubusercontent.com/120864279/215338304-04c0a527-66a9-4047-8956-5efbaaa34fc2.png">

<p>

Created my resourse group, virtual network and subnet. I set the Domain Controller VM to Windows Server 2021 and named it DC-1

<p>

<img width="1440" alt="Screen Shot 2023-01-21 at 2 58 58 PM" src="https://user-images.githubusercontent.com/120864279/213887027-30103312-5b44-4ad6-9a44-a3bc6cc60079.png">

<p>

Creating my client VM machine using Windows 10 and naming it Client-1

<p>

https://user-images.githubusercontent.com/120864279/215353208-5e6fbc43-dc5b-4bbe-8f06-3e0df63bf3a4.mp4

<p>

Setting the domain controller's NIC private IP address to be static.

<p>
  
![Screen Shot 2023-01-29 at 1 31 18 PM (2)](https://user-images.githubusercontent.com/120864279/215351200-abcc1c05-3927-475b-b55d-9ab648169cda.png)
  
A view of the NetworkWatcher topology showing that all of my networks are both in the same Vnet.
