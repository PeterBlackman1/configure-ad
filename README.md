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
  
<img width="1440" alt="Screen Shot 2023-01-29 at 8 48 15 PM" src="https://user-images.githubusercontent.com/120864279/215377373-e38688f7-a978-4afc-80a5-e7efc620fe19.png">
<p>

Created my resourse group, virtual network and subnet. I set the Domain Controller VM to Windows 10 and named it DC-1.

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

<p>
  
<img width="1440" alt="Screen Shot 2023-01-29 at 7 04 16 PM" src="https://user-images.githubusercontent.com/120864279/215367526-0ecd2e23-47d6-4600-8ac3-521c1c35ca59.png">

Here im going into DC-1 Windows Defender Firewall to enable ICMPv4 in the inbound rules to enable ICMPv4 traffic between DC-1 and Client-1. 

<p>
  
![Screen Shot 2023-01-29 at 7 15 18 PM (2)](https://user-images.githubusercontent.com/120864279/215368307-401de4c5-0766-463f-8ac9-b077d64e58d7.png)
  
Testing ping to be sure that I'm able to communicate between DC-1 and CLient-1.

<p>

<img width="1440" alt="Screen Shot 2023-01-30 at 11 52 22 AM" src="https://user-images.githubusercontent.com/120864279/215555253-3b31b14e-7e83-43b1-bd5f-cb7c54f31ec5.png">

Now I'm going to open the server manager, therefore; I can install Active Directory Domain Services

<p>
 
 https://user-images.githubusercontent.com/120864279/215569435-456f8f5e-9771-472a-bac9-5cc7e9a6518d.mp4
  
 In the server manager I select add roles and features to begin the installation process for Active Directory. As I go through the installation process and get to select the server roles, I add the Active Directory and Domain Services role.

 <p>
   
 <img width="1440" alt="Screen Shot 2023-01-30 at 1 14 26 PM" src="https://user-images.githubusercontent.com/120864279/215572697-51dcca8e-bec4-44a8-b66d-c8d42afe68ff.png">



After Active Directory is finished installing I close the window. Then I click the notification at the top right and select Promote this server to Domain Controller.

<p>
 

<img width="1440" alt="Screen Shot 2023-01-30 at 1 18 51 PM" src="https://user-images.githubusercontent.com/120864279/215573994-b1ec13aa-9a88-41f0-8b04-0eeca9b70c08.png">

After promoting to Active Directory I have to configure deployment. I select ad new forest since I'm making my own domain name.

<p>
  
 
 
