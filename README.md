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
- [Step 2: Create a Virtual Network (VNET)](#step-2-create-a-virtual-network-vnet)
- [Step 3: Deploy a Domain Controller (DC) Virtual Machine (VM)](#step-3-deploy-a-domain-controller-dc-virtual-machine-vm)
- [Step 4: Configure a Static Private IP](#step-4-configure-a-static-private-ip)
- [Step 5: Open Remote Desktop Connection (RDC)](#step-5-open-remote-desktop-connection-rdc)
- [Step 6: Install Active Directory Domain Services (AD DS)](#step-6-install-active-directory-domain-services-ad-ds)
- [Step 7: Verify AD DS Installation](#step-6-verify-ad-ds-installation)
- [Step 8: Configure and Verify DNS](#step-7-configure-and-verify-dns)

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

## Step 2: Create a Virtual Network (VNET)

### Screenshot 4: Navigating to Virtual Network(VNET)
- From the search bar, type and click on Virtual Network

<img width="715" height="536" alt="create a virtual network step 2" src="https://github.com/user-attachments/assets/276c2d62-d854-443d-9918-1d601a2ba024" />

### Screenshot 5: Configuring the VNET 
- Select the Resource Group you just created, give the VNET a name, and select the same region as your Resource Group. Click on "Review+create, then "Create" on the next page.

<img width="786" height="1149" alt="virtual network step 2" src="https://github.com/user-attachments/assets/af022dba-d931-49fa-a3be-8e69ae27a6f1" />

## Step 3: Deploy a Domain Controller (DC) Virtual Machine (VM)

### Screenshot 6: Navigating to Virtual Machine(VM) 
- From the search bar, type and click on Virtual Network

<img width="693" height="539" alt="Step 3 VM" src="https://github.com/user-attachments/assets/b8625290-d0b9-44cf-8955-391045593f61" />

### Screenshot 7: Configuring the VM 
- Select the same Resource Group you created, give it a name, and select the same region. For the image and size, select any Windows Server that is available.

<img width="851" height="1020" alt="Step 3" src="https://github.com/user-attachments/assets/e605a8c2-f50c-4535-bb25-eb764dd2325c" />

### Sreenshot 8: VM username and password
- Create a username and password. Confirm the two blue boxes on the bottom of the page and click "Next" to continue onto the Networking section.

<img width="786" height="970" alt="Step 3 5" src="https://github.com/user-attachments/assets/1a35bd51-f879-4cef-b502-d721769f8f5f" />

### Screenshot 9: Networking Section of VM 
- Select the VNET you created and click on "Review+create and "Create" on the last page to create your VM

<img width="891" height="1102" alt="Step 3 select VN" src="https://github.com/user-attachments/assets/97df851b-5603-40b5-9da9-7b7ef4322bbc" />

## Step 4: Configure a Static Private IP

### Screenshot 10: DCs Network Settings
- Go to your VM page and select your DC VM. On the left-hand side menu, select the networking section and click on Network settings." Then click on your "dc primary/ipconfig primary."

<img width="1066" height="947" alt="Step 5" src="https://github.com/user-attachments/assets/36dc2cac-0e20-44a7-87bb-87b2bb3e42e0" />

### Screenshot 11: DCs Network Interface Controller(NIC) settings
- Click on "ipconfig1"

<img width="1105" height="760" alt="Step 5 1" src="https://github.com/user-attachments/assets/82eee9f8-4d40-4c6c-bf36-f8fed00bf020" />

### Screenshot 12: Configure Network Settings
- Set the allocation to "Static" and click "Save"

<img width="692" height="1181" alt="Step 5 2" src="https://github.com/user-attachments/assets/b79b5a42-0a93-48c6-87c6-dac7dfede201" />

## Step 5: Open Remote Desktop Connection (RDC)

### Screenshot 13: Acquire DCs public IP 
- Go to your VM page and select your DC VM. Copy the public IP address.

<img width="2107" height="868" alt="Step 6" src="https://github.com/user-attachments/assets/3cc03a8e-77f3-40d9-898f-dd6afe74c684" />

### Screenshot 14-17: Remote Desktop Connection 
- Open your RDC application from your computer and click on "show options." Enter your DCs public IP and username. Click "Connect" and it will prompt you to enter the password of the DC and click "Ok." Then click "Yes" on the next prompt.

<img width="416" height="269" alt="Step 6 2" src="https://github.com/user-attachments/assets/1bb6377a-300b-412a-992d-35977e27eeed" />
<img width="414" height="499" alt="Step 6 1" src="https://github.com/user-attachments/assets/de56d6b0-cd69-4a35-9107-72dad8c33012" />
<img width="463" height="440" alt="Screenshot 2026-11-13 124207" src="https://github.com/user-attachments/assets/378ebac0-32cc-4a27-9b83-83ca17ad4d9e" />
<img width="408" height="469" alt="Step 6 3" src="https://github.com/user-attachments/assets/33b342a7-fc38-465e-a2e0-8b1c5e2b099e" />

## Step 6: Install Active Directory Domain Services (AD DS)























