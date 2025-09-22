# Task 20: Resize a VM’s OS Disk and Extend the C: Drive (Windows VM)

## Description
Simulated a common real-world scenario where disk space needs to be increased for better performance or storage.

## Steps Executed
1. **Stopped the VM**
   - Stopped **AravindVM1** from the Azure Portal.

2. **Resized the OS Disk**
   - Navigated to **Disks ➜ OS Disk (AravindVM1)**.
   - Updated the size from **127 GB ➜ 256 GB (approx).**

3. **Restarted the VM**
   - Restarted **AravindVM1** from the Portal after resizing.

4. **Extended C: Drive inside Windows**
   - Connected via **RDP** to **AravindVM1**.
   - Opened **Disk Management (diskmgmt.msc)**.
   - Extended the C: drive volume to use the new disk space.

## Verification
- Confirmed in Disk Management that **Windows (C:) drive** shows **255.45 GB** and is fully expanded.
- Verified the VM booted successfully after the resize.
