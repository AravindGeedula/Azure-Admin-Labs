# Task 27 – Delete Backup Data & Recovery Services Vault Cleanup

## 🎯 Goal
Stop backup billing by permanently removing a VM backup item and cleaning up the Recovery Services Vault.

---

## 💡 Why This Matters
Backups (protected instances, restore points, GRS storage, snapshots) continue to incur costs even if the VM itself is deleted.  
To stop billing, you must **delete backup data** (not just “stop backup”) and then remove the vault.

---

## ✅ Prerequisites
- **Permissions**: Owner or Contributor + Backup Contributor on the vault’s resource group.  
- **No resource locks** on the vault or RG (remove if present).  
- **Vault Name**: `VMBackupVault01`  
- **Backup Item**: `RestoredVM1`

---

## ⚙️ Steps (Azure Portal)

### 1) Find the Vault and Backup Item
- Go to **Recovery Services vaults** → open `VMBackupVault01`.  
- Left menu → **Backup items** → **Azure Virtual Machine** → locate **RestoredVM1**.

---

### 2) Handle Soft Delete (if item not selectable)
- Vault → **Properties** → **Security and Soft Delete settings**.  
- Uncheck:
  - `Enable soft delete for cloud workloads`  
  - (If shown) `Enable soft delete and security for hybrid workloads`  
- Save.  
- If item shows **Undelete**, click it first → then proceed to deletion.  

> ⏳ Note: After disabling soft delete, portal may take a few minutes before showing **Delete backup data** option.

---

### 3) Stop Protection and Delete Backup Data
- Select **RestoredVM1** → `Delete backup data` (or `Stop backup with delete data`).  
- Confirm prompts (may need to type the item name).  
- This removes all restore points and stops charges for this item.

---

### 4) Verify Deletion Jobs
- Portal → **Backup Center** → **Jobs**.  
- Confirm **Completed** status for:
  - `Undelete` (if applicable)  
  - `Delete backup data`  

📸 Screenshot this page for evidence.

---

### 5) Delete the Empty Recovery Services Vault
- Go back to `VMBackupVault01`.  
- Verify **Backup items = 0**.  
- Ensure these are empty:
  - Site Recovery (no replicated items)  
  - Backup Policies (delete custom ones if blocking deletion)  
  - Diagnostic settings / Private endpoints / Locks (remove if any)  
- From **Overview** → `Delete Vault`.

---

## 📊 Verification (Billing & Cleanliness)
- **Jobs**: Deletion entries show ✅ Completed.  
- **Vault**: Deleted successfully.  
- **Cost Management → Cost Analysis**: No new charges under:
  - Azure Backup  
  - GRS/RA-GRS Storage  
  - VM Protected Instances  
  - Snapshots  
- (Optional) Azure **Disks** blade: verify no unattached disks/snapshots remain.

---

## 🛠️ Troubleshooting
- **Item not clickable** → Soft-delete retention: disable, then undelete, then delete.  
- **Vault delete blocked** → Remove leftover policies, replicated items, diagnostic settings, or locks.  
- **Still blocked** → Wait for retention expiry or open Microsoft Support request to purge soft-deleted data.

---

## 🏁 Outcome
- Backup item `RestoredVM1` fully deleted.  
- Recovery Services Vault `VMBackupVault01` removed.  
- No residual backup-related charges in subscription.








