# Task 16: Restrict VM Sizes Using Azure Policy (Allow Only B-Series VMs)

## Description  
Created a custom Azure Policy to restrict VM creation, allowing **only B-Series VM sizes** in the resource group. This enforces cost control and governance by preventing the deployment of larger VM sizes.

---

## Steps Executed  

1. **Created Custom Policy Definition**  
   - **Name:** `Allow-B-Series-VMs`  
   - **Logic:** Deny creation of any VM not in the allowed SKUs (`Standard_B1s`, `Standard_B2s`).  
   - Used Azure CLI with `--rules` JSON block to define allowed VM SKUs.  

2. **Assigned Policy at Resource Group Scope**  
   - **Assignment Name:** `Enforce-B-Only`  
   - **Scope:** Resource Group `RG-Demo-Raj`  
   - Used Azure CLI to assign the policy definition at RG level.  

3. **Validation in Azure Portal**  
   - Navigated to **Policy > Definitions** → Verified `Allow-B-Series-VMs` exists.  
   - Navigated to **Policy > Assignments** → Confirmed `Enforce-B-Only` is active.  

---

## Verification  
✅ Only B-Series VM sizes are allowed.  
❌ Any attempt to create a VM outside the allowed SKUs (e.g., D-Series or F-Series) is denied.  

---

## Purpose  
- Helps enforce **governance** in Azure.  
- Ensures developers or teams cannot create costly VMs accidentally.  
- Useful for **cost optimization** in dev/test environments.  

---
