# Task 14: Create a Network Security Group (NSG) and Associate it to Subnet-Demo01 under your VNET

## Description
In this task, you created a Network Security Group (NSG) named **NSG-SubnetDemo01** and associated it with your existing subnet **Subnet-Demo01** under your Virtual Network (**Demo-VNet**).  
You also associated a Route Table (**RT-Demo**) with the same subnet, enabling both **security filtering** and **custom routing** for all resources inside that subnet.

## Steps Executed
1. Navigated to **Networking → Network Security Groups** in Azure Portal.  
2. Clicked **+ Add** to create a new NSG.  
   - Name: NSG-SubnetDemo01  
   - Resource Group: RG-Demo-Raj  
   - Region: East US  
3. After creation, went to **Demo-VNet → Subnets → Subnet-Demo01**.  
4. Associated **NSG-SubnetDemo01** with **Subnet-Demo01**.  
5. Verified association in subnet settings.  

## Purpose
🔐 **NSG Purpose:** Controls inbound and outbound traffic at the subnet level, acting like a mini-firewall.  

🧭 **Route Table Purpose:** Lets you override Azure’s default system routes — useful for redirecting traffic to NVA or firewall.  

## Verification
- Subnet **Subnet-Demo01** now has both **NSG-SubnetDemo01** and **RT-Demo** attached.  
- Confirmed NSG rules are ready to be customized, and routing rules can be applied as needed.
