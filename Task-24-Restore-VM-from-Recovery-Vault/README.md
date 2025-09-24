# Task 24: Restore Azure Virtual Machine from Recovery Services Vault Backup

## Description
Restore a previously backed-up virtual machine by creating a new VM from a selected recovery point using **Azure Recovery Services Vault**.

## 🧱 Step-by-Step Execution

### Step 1: Go to Recovery Services Vault
- Navigated to **VMBackupVault01** under Recovery Services vaults.  
- This vault already had backup data of the original VM (**AravindVM1**).

### Step 2: Open Backup Items
- Clicked on **Backup Items** from the left-side menu.  
- Selected **Azure Virtual Machine → 1 item (RestoredVM1)**.

### Step 3: Initiate Restore Process
- Clicked the backed-up VM item.  
- Chose **Restore VM** option to start the restore wizard.

### Step 4: Choose Restore Point
- Selected restore point from **July 25, 2025 – 6:37:26 PM**.  
- Chose type: **Application Consistent snapshot**.  
- Clicked **OK** to confirm restore point.

### Step 5: Restore Configuration
In the **Restore Virtual Machine** blade:
- **Restore Type:** Create new virtual machine  
- **VM Name:** RestoredVM1  
- **Resource Group:** RG-Demo-Raj  
- **Virtual Network:** Default VNet (selected from dropdown)  
- **Subnet:** Default subnet (auto-filled)  
- **Staging Location:** Created new storage account  

### Step 6: Create Storage Account
- Went to **Create Storage Account**:  
  - **Name:** stgrestorevm01  
  - **Region:** Central India  
  - **Performance:** Standard  
  - **Redundancy:** GRS  
- Clicked **Review + Create** → Deployed the storage account.

### Step 7: Finalize Restore
- Returned to the restore wizard.  
- Selected newly created **stgrestorevm01** as staging location.  
- Clicked **Restore** to trigger restore operation.

### Step 8: Monitor Restore Progress
- Navigated to **Backup Jobs** under vault.  
- Saw 3 job entries:  
  - Configure Backup → ✅ Completed  
  - Backup → ✅ Completed  
  - Restore → ✅ Completed  

### Step 9: Verify Virtual Machine
- Went to **Virtual Machines** in Azure portal.  
- Confirmed the new VM **RestoredVM1** was in **Running** state.  
- Region, OS, resource group were all intact as per backup.

---

## ✅ Outcome
- Successfully restored a new VM (**RestoredVM1**) from a backup recovery point.  
- Verified that the restored VM was up and running with correct configuration, resource group, and region.  
- Demonstrated **disaster recovery readiness** using Recovery Services Vault in Azure.
