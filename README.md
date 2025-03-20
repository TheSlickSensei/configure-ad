# configure-ad
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

- Step 1
- Step 2
- Step 3
- Step 4
- Step 5
- Step 6

<h2>Deployment and Configuration Steps</h2>

Step 1
![Step 1 AD project](https://github.com/user-attachments/assets/ee066f1d-946e-4a9c-b627-cda7cdd6224f)


After creating a Domain Controller, a Virtual Machine and subnet in Microsoft Azure, we're ready to start Deploying an Active Directory 

<br />

<p>

</p>
<p>

</p>

Step 2
![Step 2 AD project](https://github.com/user-attachments/assets/39dedd42-0bb4-4e70-a386-820a4620d1fe)


<p>
Don't forget to set your VM's (Virtual Machine) to the IP address of your Domain Controller. This allows your VM to join the Domain and access information through it instead of your Virtual Subnet.
</p>
<br />


Step 3 
![Step 3 AD project](https://github.com/user-attachments/assets/583bc5b3-922c-41bc-b013-ba314eb94aa9)

Log into Domain Controller and install Active Directory Domain Services.

![step 3-2 AD project](https://github.com/user-attachments/assets/dc0e414d-f1ef-4937-bce2-44527ef43de8)

Promote as a Domain Controller and setup a new forest as mydomain.com (in reality this can be any name you desire) 
![Step 3-3 AD project](https://github.com/user-attachments/assets/9a171e72-d0f2-476a-9080-11868809cb85)


Step 4 
![Step 4 AD project](https://github.com/user-attachments/assets/520df3f5-be35-4369-a3fe-ab8ca2582919)

After restarting the Domain Controller, we can now create some organizational units (OU) that we'll call "_EMPLOYEES" & "_ADMINS" 

Step 5
![Step 5 AD project](https://github.com/user-attachments/assets/b666aa52-5105-457d-b83c-c9cbbef36349)

Create a new Admin named Jane Doe.

![Step 5-2 AD project](https://github.com/user-attachments/assets/09088938-9496-4836-9283-5036b2be7523)
Add jane_admin to the "Domain Admins" security group. 

![step 5-3 AD project](https://github.com/user-attachments/assets/679dcddf-5138-4ce5-a6c0-00f0a630ddca)

We're then going to log back into our Domain Controller as Jane Doe to make sure she has Admin level access.

Step 6

![Deploying AD final step](https://github.com/user-attachments/assets/1a24fd66-e655-4c26-8935-c8308d0fc533)

We connect our Virtual Machine to our Domain Controller DNS server and log back into our Domain Controller and verfy that Client 1 (Our VM) shows up!
Congratulations, You have set up your first Active Directory!  
