# Azure-Admin-Projects







# Implement the Azure Iaas
## Description

OSS Corporation is a globally distributed firm. They have their headquarters in the East US with another branch office in the WEST US. Currently, they are working on a project and decided that the application tier of this project will reside in one of its branch regions. For security reasons, OSS Corporation management is adamant on keeping their data tier in the headquarter region. 

## Background of the problem statement:
As an organization, they are open to suggestions and are currently evaluating Azure as a deployment platform. To prepare for the deployment of IaaS Standard_B1ms, OSS Corporation must deploy an IaaS v2 virtual network in the headquarters region for its database. But for the application, it should create another IaaS v2 virtual network in the branch region. In addition, because the communication between App and data should happen over a private channel, one needs to prepare their branch office virtual network for establishing connectivity to the headquarter’s IaaS v2 virtual network by creating a virtual network gateway and deploy a test IaaS Standard_B1ms VM to the virtual networks for verifying the connection.
After the deployment team ensures the connectivity between both the networks, you can validate the same using Ping.

## Following requirements should be met:
Create virtual networks in the aforementioned region
Create test virtual machines in both the virtual network
Establish the connectivity between both the networks via VNet peering
Ensure connectivity is established properly


Step 1)  Create two virtual networks
Create the first virtual network in East US, 
Resource Group Name: Osscorp 
VNET Name: VNET1 
Subnet Name: SN1 :10.104.00/24
Location: East US

Create the second virtual network in West US, 
Resource Group Name: Osscorpbranch 
VNET Name: VNET2 
Subnet Name: SN1 :198.162.0.0/24
Location: West US 2 














Step 2) Create two virtual machines 
Create first virtual machine in East US 
Resource Group Name: Osscorp
Virtual Machine Name: VM1
OS Type: Windows Server 2022 Datacenter 
Instance Size: Standard B1s















Create first virtual machine in West US 
Resource Group Name: Osscorpbranch
Virtual Machine Name: VM2
OS Type: Windows Server 2022 Datacenter 
Instance Size: Standard B1s














Step 3) Establish connectivity between networks via Peering
Go to virtual networks tab 
Go to VNET1 Peerings Tab 



Click on add once set up 




Now you have a peering set up: VNET1-VNET2














Step 4) Establish connection to both virtual machines - copy the public IP address in to remote desktop - then use the username and password to login 










Go to Windows defender firewall in both VMs and then in Advanced Settings allow ICMP traffic in Inbound Rules






Now we will go to the command prompt on both VM’s - then type ipconfig to check the ips 

Try pinging the virtual machines using Ping (IP address of other vm) 





Both VM’s are able to Ping each other







