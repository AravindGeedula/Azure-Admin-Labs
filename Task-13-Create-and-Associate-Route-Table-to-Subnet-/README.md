# Task 13: Create and Associate a Route Table to Subnet

## Description
Created a custom route table **RT-Demo** and added a user-defined route. Associated it with the subnet **Subnet-Demo01 (10.1.1.0/24)** in **Demo-VNet** (RG: Demo-Raj). This ensures traffic routing control for resources inside the subnet.

## Steps Executed
1. Navigated to **Azure Portal → Route tables → + Create**.
2. Entered details:
   - **Name:** RT-Demo
   - **Resource Group:** RG-Demo-Raj
   - **Region:** Same as Demo-VNet
3. After deployment, opened **RT-Demo** → **Routes** → **+ Add**.
4. Added a custom route:
   - **Route name:** Route-To-Internet  
   - **Address prefix:** 0.0.0.0/0  
   - **Next hop type:** Internet
5. Went to **Subnets** → Associated **Subnet-Demo01 (10.1.1.0/24)** with RT-Demo.
6. Saved and confirmed association.

## Verification
- Confirmed **RT-Demo** listed under Subnet-Demo01.  
- Verified custom route **Route-To-Internet (0.0.0.0/0 → Internet)** exists.  
- Subnet traffic now flows via RT-Demo.

