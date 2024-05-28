<p align="center">
  
  ![Title_pic](https://github.com/88Qua19/Deploying-On-Premises-Active-Directory-In-Cloud-Azure-/assets/169956201/d70aeed0-d6d0-423b-9937-f8d85a6b0029)
 
# Deploying-On-Premises-Active-Directory-In-Cloud-Azure
</p>
<p>This tutorial outlines how to implement on-premises Active Directory within Azure Virtual Machines.</p> 

<h2>Environments and Technologies</h2>
<ul>
<li> Microsoft Azure (Virtual Machines) </li>
<li>Remote Desktop</li>
<li>Active Directory Domain Services</li>
<li>Powershell Ise</li>
</ul>

<h2>Operating systems</h2>
<ul>
  <li>Windows Server 2022 Datacenter</li>
  <li>Windows 10 22h2</li>
</ul>

<h2> Configuration steps</h2>
<ul>
  <li>Step 1 -Set up resources in Azure</li>
  
  <li>Step 2- Ensure Connectivity between the client and domain controller</li>
  <li>Step 3 - Install Active Directory</li>
  <li>Step 4- Create admin and normal user accounts in Active Directory</li>
  <li>Step 5- Join Client-1 to the domain</li>
  <li>Step 6- Setup remote desktop for non-administrative users on Client-1</li>
  <li>Step 7- Create additional users using Powershell script</li>
  </ul>

  
  <H3>
Setup Virtual Machines in Azure Cloud
    
 ![AD_1](https://github.com/88Qua19/Deploying-On-Premises-Active-Directory-In-Cloud-Azure-/assets/169956201/7d678875-296f-4a05-acaa-093c2079b941) 


Using remote desktop we logged into Client-1's virtual machine and initiated a perpetual ping using DC-1's private IP address. We observed the success of the ping.

![AD_pic2](https://github.com/88Qua19/Deploying-On-Premises-Active-Directory-In-Cloud-Azure-/assets/169956201/1625edcc-f839-4006-b3b0-02dcf343955e)

Within Active Directory Users and Computers we will create two organizational units, _EMPLOYEES & _ADMINS. We will be adding Jane doe as an employee. She will also be added into security group "Domain Admins".

![AD_pic3](https://github.com/88Qua19/Deploying-On-Premises-Active-Directory-In-Cloud-Azure-/assets/169956201/6e9f4e8b-64ea-4180-8621-e77b02fea368)

Join Client-1 to the domain (mydomain.com)

![AD_pic5](https://github.com/88Qua19/Deploying-On-Premises-Active-Directory-In-Cloud-Azure-/assets/169956201/51cedd2f-af08-4200-be71-2ea0c4b39db9)


