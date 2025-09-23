# Task 23 – Create a New Virtual Machine from Snapshot (Disaster Recovery)

## 📌 Objective
Simulate a **disaster recovery** scenario by creating a brand new Virtual Machine using an OS disk that was generated from a snapshot of a previous VM.  
This process demonstrates how to recover from a failed or deleted VM by restoring it from its snapshot.

---

## 🛠️ Steps Performed

1. Navigated to the **managed disk** created from the snapshot (`osdisk-from-snapshot-vm1`).  
2. Clicked **Create VM** option from the disk blade.  
3. Entered the following VM details:  
   - **Name:** `RestoredVM1`  
   - **Region:** Central India  
   - **Size:** Standard B1s  
   - **OS Disk:** Premium SSD (Gen2) (based on the snapshot)  
4. Enabled **RDP access** in Networking for login and basic connectivity tests.  
5. Clicked **Review + Create → Create**.  
   - Deployment completed successfully (`CreateVm-osdisk-from-snapshot-vm1-20250725164935`).  
6. Verified that the VM `RestoredVM1` was running and accessible through RDP.

---

## 📖 Key Learnings
- Snapshots + Managed Disks = complete **VM recovery workflow**.  
- A VM can be recreated **entirely from its snapshot**, enabling:  
  - Disaster recovery after deletion/corruption.  
  - Migration or duplication of VMs.  
- Ensuring RDP/SSH access is key for verifying the restored VM’s usability.  

---

## ✅ Proof

- Status: Deployment succeeded and VM `RestoredVM1` is accessible.  
