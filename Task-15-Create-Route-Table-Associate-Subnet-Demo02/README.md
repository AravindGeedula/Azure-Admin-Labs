# Task 15: Create a Route Table and Associate It with Subnet-Demo02

## Description  
In this task, we created a custom route table (**RT-Demo01**) inside the resource group **RG-Demo-Raj**, and added a new subnet (**Subnet-Demo02**) inside the existing virtual network (**Demo-VNet**).  

The subnet was assigned an IP range of **10.1.2.0/24**, which fits within the VNet's **10.1.0.0/16** address space.  

## Purpose  
- Enables **custom routing** for traffic flows.  
- Provides future control for scenarios such as redirecting traffic through **NVAs, firewalls, or peering routes**.  
- Improves **network segmentation** by isolating Subnet-Demo02 workloads.  

## Steps Executed  
1. Navigated to **Demo-VNet → Settings → Subnets**.  
2. Created a new subnet:  
   - **Name:** Subnet-Demo02  
   - **Range:** 10.1.2.0/24  
3. Created a route table:  
   - **Name:** RT-Demo01  
   - **Resource Group:** RG-Demo-Raj  
4. Associated **RT-Demo01** with **Subnet-Demo02**.  
5. Verified association under the **Subnet settings**.  

✅ Subnet-Demo02 is now connected to RT-Demo01, ready for custom route rules.  
