# Task 12: Create and Associate a Subnet to an Existing VNet

## Description
Created a new custom subnet inside an existing Virtual Network (VNet) named **Demo-VNet** to logically segment IP ranges and isolate workloads.

## Steps Executed
1. Navigated to **Demo-VNet ➜ Settings ➜ Subnets**.  
2. Clicked on **+ Subnet**.  
3. Entered subnet details:  
   - **Name:** Subnet-Demo01  
   - **IPv4 Address space:** 10.1.0.0/16  
   - **Starting address:** 10.1.1.0  
   - **Size:** /24 (256 addresses)  
   - Subnet address range auto-generated: **10.1.1.0 – 10.1.1.255**  
4. Clicked **Add** → Subnet successfully created.

## Result
Now **Demo-VNet** contains:  
- **default subnet** → 10.1.0.0/24  
- **Subnet-Demo01** → 10.1.1.0/24  

## Purpose
Logical network segmentation for traffic isolation, security, and better IP address management in Azure networking.

---

## ✅ Outcome
- Successfully created a new subnet (**Subnet-Demo01**) within **Demo-VNet**.  
- Confirmed both default and custom subnets exist, enabling **segmentation of workloads** inside the same VNet.  
- This setup prepares the environment for attaching VMs or services with **dedicated IP ranges** for better control and security.
