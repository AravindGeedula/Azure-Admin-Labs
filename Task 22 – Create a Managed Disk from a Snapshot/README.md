# Task 22 – Create a Managed Disk from a Snapshot

## 📌 Objective
Simulate a recovery scenario by creating a new managed disk from a previously created snapshot (`snap-osdisk-vm1-20250725`).  
This helps restore VM data or the OS to a previous state — commonly used in **backup and disaster recovery strategies**.

---

## 🛠️ Steps Performed

1. Navigated to the **snapshot resource** in the Azure Portal.  
2. Clicked **"Create Disk"** from the snapshot blade.  
3. Entered details:  
   - Name: `disk-from-snapshot-vm1`  
   - Resource Group: `RG-Demo-Raj`  
   - Region/Storage: kept default  
4. Clicked **Review + Create → Create**.  
   - Deployment: `CreateDiskBlade-20250725123819` completed successfully.  
5. Verified that the new managed disk appeared in the portal with the correct **size and properties**.

---

## 📖 Key Learnings
- Snapshots capture the **point-in-time state** of a disk.  
- Managed disks created from snapshots can:  
  - Be attached to an existing VM.  
  - Be used to create a new VM.  
  - Restore workloads during **backup and disaster recovery**.  

---

## ✅ Proof

- Status: Deployment succeeded and disk available in the portal.  
