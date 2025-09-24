# Task 25: Create and Configure a Virtual Machine Scale Set (VMSS) with Public Load Balancer in Azure

## Description
Deployed a high-availability auto-scaling infrastructure using a **Virtual Machine Scale Set (VMSS)** integrated with an **Azure Standard Public Load Balancer**.  
This setup enables traffic distribution across multiple VMs with health monitoring and frontend NAT rules.

---

## Steps Executed

### Step 1: Create Virtual Machine Scale Set (VMSS)
- **OS:** Windows Server  
- **Orchestration:** Uniform  
- **Instance Count:** 2  
- **Login Method:** Username + Password  
- **Boot diagnostics:** Enabled using managed storage  

### Step 2: Create Networking Resources
- **Virtual Network:** vnet-southindia  
- **Subnet:** snet-southindia-1 (172.16.0.0/24)  

### Step 3: Configure Public Load Balancer (Standard SKU)
- **Name:** lb-vmss-demo  
- **Public IP:** pip-vmss-demo (Static)  
- **Frontend IP configuration:** frontend-vmss  
- **Backend pool:** backend-vmss (auto-linked to VMSS)  

### Step 4: Add Load Balancer Rules
- **Health Probe:** http-probe (HTTP, Port 80, Path /)  
- **Load Balancing Rule:** http-rule (TCP 80 → 80)  
- **Inbound NAT Rule:** Port 80 mapped to backend instances  

### Step 5: Enable Management Features
- **Overprovisioning:** ✅ Enabled  
- **Auto Guest OS Updates:** ✅ Enabled  
- **Identity, Backup, Standby Pools:** ❌ Disabled  

### Step 6: Verify Deployment
- ✅ Public IP assigned  
- ✅ Load Balancer components visible (Probe, Rule, Pool)  
- ✅ VMSS created with 2 instances running  
- ✅ Successfully connected via Load Balancer IP  

---

## ✅ Outcome
- Deployed a **high-availability VM Scale Set** with integrated **Public Load Balancer**.  
- Verified load balancing, health probe monitoring, and NAT rules.  
- Demonstrated scalable infrastructure setup for production-grade web or app workloads.
