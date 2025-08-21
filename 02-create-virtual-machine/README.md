# Task 02 - Create Virtual Machine (AravindVM1)

## 🎯 Objective
Deploy a Virtual Machine in Azure named **AravindVM1** inside the existing resource group.

---

## 📝 Steps

1. **Navigate to Azure Portal**  
   - Sign in to [Azure Portal](https://portal.azure.com).  
   - Go to **Virtual Machines** → **Create**.

2. **Basics Tab**  
   - Subscription: *Select your active subscription*  
   - Resource Group: *Choose your lab RG*  
   - Virtual Machine Name: **AravindVM1**  
   - Region: *Select region close to you (e.g., Central India)*  
   - Image: *Windows Server 2022 Datacenter* (or Ubuntu if Linux VM)  
   - Size: **Standard_B2s** (2 vCPU, 4 GB RAM)  
   - Authentication type: Password  
   - Username: `azureadmin`  
   - Password: *Set a strong password*  

3. **Disks Tab**  
   - OS Disk: Standard SSD (Default)  
   - Leave Data Disks empty (for now).  

4. **Networking Tab**  
   - Virtual Network: *Select existing VNet or create new*  
   - Subnet: Default  
   - Public IP: Enabled  
   - NIC Network Security Group: Basic → Allow **RDP (3389)** for Windows or **SSH (22)** for Linux.  

5. **Management, Monitoring, Advanced, Tags**  
   - Leave defaults (unless needed).  

6. **Review + Create**  
   - Validate settings.  
   - Click **Create**.  
   - Wait for deployment completion.  

---

## ✅ Verification

- Go to **Virtual Machines** → **AravindVM1** → **Overview**.  

