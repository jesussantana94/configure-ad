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

## Configuration Steps

- [Step 1: Create an Azure Resource Group](#step-1-create-an-azure-resource-group)
- [Step 2: Create a Virtual Network(VNET)](#step-2-create-a-virtual-network)
- [Step 3: Deploy a Domain Controller Virtual Machine](#step-3-deploy-a-domain-controller-virtual-machine)
- [Step 4: Configure a Static Private IP](#step-4-configure-a-static-private-ip)
- [Step 5: Install Active Directory Domain Services](#step-5-install-active-directory-domain-services)
- [Step 6: Verify AD DS Installation](#step-6-verify-ad-ds-installation)
- [Step 7: Configure and Verify DNS](#step-7-configure-and-verify-dns)

## Step 1: Create an Azure Resource Group

### Screenshot 1: Navigating to Resource Group
- From the Azure portal homepage, locate the search bar at the top of the screen; type “resource group”. And select: "Resource Group.”

<img width="671" height="640" alt="Step 1" src="https://github.com/user-attachments/assets/0f547bb8-df10-407b-8e1a-886d1d941051" />

### Screenshot 2: Creating a Resource Group
- Click on either the center “+ Create” or the top left of the screen.

<img width="2086" height="1010" alt="Step 1 5" src="https://github.com/user-attachments/assets/bb55f0e1-2e07-4176-98fe-a84fdf33c030" />

### Screenshot 3: Configuring the Resource Group

- Next, enter a name for your Resource Group and select the desired Azure region. Make sure to remember which region you selected, as you'll use it when creating the other resources in this lab. Click on “Review+create” to continue.

<img width="904" height="1000" alt="Step 2 5" src="https://github.com/user-attachments/assets/2a4db8a6-dff6-4606-83ad-9feeeeab8055" /> 

## Step 2: Create a Virtual Network

### Screenshot 4: Navigating to Virtual Network(VNET)
- From the search bar, type and click on Virtual Network

<img width="715" height="536" alt="create a virtual network step 2" src="https://github.com/user-attachments/assets/276c2d62-d854-443d-9918-1d601a2ba024" />

### Screenshot 5: Configuring the VNET 
- Select the Resource Group you just created, give the VNET a name, and select the same region as your Resource Group. Click on "Review+create, then "Create" on the next page.

<img width="786" height="1149" alt="virtual network step 2" src="https://github.com/user-attachments/assets/af022dba-d931-49fa-a3be-8e69ae27a6f1" />

## Step 3: Deploy a Domain Controller Virtual Machine






