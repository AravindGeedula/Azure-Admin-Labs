# Task 18: Detach and Delete a Managed Data Disk

## Description
Detached a 1 TB managed data disk (**datadisk-central01**) from VM **AravindVM1** using Azure CLI in Cloud Shell, then deleted the disk to prevent unnecessary costs.

## Steps Executed
1. **Verified the disk attachment**
   - Checked in Azure Portal ➜ VM **AravindVM1** ➜ Disks.
   - Confirmed `datadisk-central01` was attached.

2. **Detached the disk using Azure CLI**
   ```bash
   az vm disk detach \
     --resource-group RG-DEMO-RAJ \
     --vm-name AravindVM1 \
     --name datadisk-central01

   az disk list --query "[?name=='datadisk-central01']"  bash code to give

   Output showed:

"diskState": "Unattached"

"managedBy": null

Deleted the disk

Navigated to Disks in the Portal.

Selected datadisk-central01 ➜ Delete.

Confirmed deletion to free up resources.

Verification

Disk no longer appears under AravindVM1 ➜ Data Disks.

az disk list confirms the disk resource is deleted.

Verified in Portal that the resource is gone.

