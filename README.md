# Azure-Admin-Projects







## Implement the Azure Iaas

#### 1. Create a virtual network in East & West US
   
a. Sign into Azure and go to virtual networks

b. Under virtual networks click on create

c. In the basics tab - select the subscription -> create a new/ select an existing resource group-> Name the VN as VNET1 and select the region as East US
Repeat steps to create for West US 

#### 2.	Create and test virtual machines in both networks 
a.	In azure find virtual machines

b.	Click create under virtual machines and select azure virtual machine

c.	In the basics tab, select the correct subscription, then choose the correct resource group. Give it a name of VM1 and select East US. Choose windows server 2022 data center, leave everything else as default. 

d.	Use admin account, provide a username, such as virtualmachineuser1 and a password. 

e.	Inbound port rules – allow selected ports, select RDP then click next

f.	Select OS Disk Type- Standard HDD then click next 

g.	Under Networking select virtual network as VNET1 and its subnet, leave the remaining as default and select the review create button

h.	After that hit the create button at the bottom of the page.

Repeat steps to create for West US 

#### 3.	Create the connectivity between both the networks using VNet Peering
a.	Go to the virtual networks tab select VNET1

b.	Then go to Peering Tab in VNET1

c.	Click on add
 
d.	Click add and the peering is completed 

#### 4.	Make sure connectivity is established properly 
a.	Connect first VM by Native RDP 
 
b.	Connect second VM by Native RDP
 
c.	After the login, open windows defender firewall in both VM’s and in the advanced settings allow ICMP traffic in inbound rules 
 
d.	Now go to the command prompt on both VM’s by typing cmd and then type ipconfig to see the IP’s on both VM’s with each other by the Ping command.
 
e.	Both VM’s are able to ping each other. 
