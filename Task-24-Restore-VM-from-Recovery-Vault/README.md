# Task 24: Restore Azure Virtual Machine from Recovery Services Vault Backup

## Description
Restored a previously backed-up virtual machine by creating a **new VM** from a selected recovery point using **Azure Recovery Services Vault (RSV)**.

---

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
- Specified restore settings:  
  - Created a **new VM** (RestoredVM1).  
  - Chose same **Region: Central India**.  
  - Selected appropriate **Resource Group**.  
  - Networking and storage auto-linked to new resources.  

- Clicked **Review + Restore → Restore**.  

### Step 6: Verification
- Deployment completed successfully.  
- Verified new VM **RestoredVM1** appeared in the Resource Group.  
- Confirmed OS disk and configuration were restored from the snapshot.  

---

✅ **Outcome**: Successfully restored VM (**RestoredVM1**) from Recovery Vault backup. This simulates a real-world **Disaster Recovery (DR)** scenario where workloads can be brought back online quickly.  
