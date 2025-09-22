# Task 21: Create a Snapshot of a Virtual Machine OS Disk

## Description
Simulated a real-world backup scenario by creating a snapshot of the Virtual Machine's OS disk using the Azure Portal.  

This snapshot can be used later to restore the VM or create a new VM from the same OS state.

## Steps Executed
1. Navigated to **Disks** → selected the **OS Disk** attached to VM **AravindVM1**.  
2. Clicked **Create Snapshot**.  
3. Entered details:  
   - **Name:** snap-osdisk-vm1-20250725  
   - **Snapshot type:** Full  
   - **Resource Group:** RG-Demo-Raj  
   - **Region:** Central India  
4. Clicked **Review + Create** → **Create**.  
5. Deployment completed successfully ✅ (screenshot attached).

## Verification
- Snapshot resource **snap-osdisk-vm1-20250725** appeared under Resource Group **RG-Demo-Raj**.  
- Confirmed availability for future restore or VM creation.
