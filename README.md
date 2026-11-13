# configure-ad
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Building the infrastructure and deploying Active Directory</h1>
- Project 1. Azure Infrastructure & Active Directory Deployment <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Network)
- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services


<h2>Operating Systems Used </h2>

- Windows Server 2025
- Windows 11 Pro (25H2)

<h2> Before You Begin: Prerequisites</h2>

Before starting this lab, ensure you have the following:

- An Active Microsoft Azure account.
- Access to the Azure Portal.
- An Available Azure subscription.
- Permission to create and manage Azure resources.
- Access to a Windows Server VM image.

<h2>Configuration Steps</h2>

- Step 1. Create a Resource Group.
- Step 2. Create A Virtual Network.
- Step 3. Create a Virtual Machine(VM) for your Domain Controller(DC).
- Step 4. Set the DCs Network Interface Controller(NIC) private IP address to "Static."
- Step 5. Set up Active Directory Domain Services(AD DS).
- Step 6. Confirmation of Successful Installation for AD DS.

<h1> Step 1</h1>

- At the top of the home screen, there should be a search bar; type “resource group”. Click on "Resource Group.”

<img width="671" height="640" alt="Step 1" src="https://github.com/user-attachments/assets/0f547bb8-df10-407b-8e1a-886d1d941051" />


- Click on either the center “+ Create” or the top left of the screen. Next, you will need to create a name for your resource group.

<img width="2086" height="1010" alt="Step 1 5" src="https://github.com/user-attachments/assets/bb55f0e1-2e07-4176-98fe-a84fdf33c030" />


- Next, you will need to create a name for your resource group. Make sure to remember what region you selected. Click on “Review+create” to continue.

<img width="904" height="1102" alt="Step 2 5" src="https://github.com/user-attachments/assets/2a4db8a6-dff6-4606-83ad-9feeeeab8055" />

<h1> Step 2</h1>







