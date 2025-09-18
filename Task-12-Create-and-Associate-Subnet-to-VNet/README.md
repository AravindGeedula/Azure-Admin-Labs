# Task 12: Create and Associate a Subnet to an Existing VNet

## Description
Created a new custom subnet inside an existing Virtual Network (VNet) named **Demo-VNet** (Resource Group: RG-Demo-Raj) to logically segment IP ranges and isolate workloads.

## Steps Executed
1. Navigated to **Demo-VNet → Settings → Subnets**.
2. Clicked **+ Subnet** to add a new subnet.
3. Entered details:
   - **Subnet Name:** Subnet-Demo01  
   - **IPv4 Address space (VNet):** 10.1.0.0/16  
   - **Starting address:** 10.1.1.0  
   - **Subnet Size:** /24 (256 addresses)  
   - **Subnet range auto-generated:** 10.1.1.0 – 10.1.1.255  
4. Clicked **Add** → Subnet successfully created.

## Verification
- Confirmed **Subnet-Demo01 (10.1.1.0/24)** appears under Demo-VNet.  
- Verified both **default subnet (10.1.0.0/24)** and new **Subnet-Demo01** exist without overlap.  
- Logical network segmentation achieved, enabling workload isolation.

## Screenshot
![Task 12 Screenshot](https://drive.google.com/file/d/1CRTwYu__J_MA9XApm4HbCuzNuSpopusI/view?usp=drive_link)
