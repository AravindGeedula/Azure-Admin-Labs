# Task 8: Create Security Group (Demo-Admins)

### Objective
Create a security group in Microsoft Entra ID called **Demo-Admins** and add a user into it.

### Steps
1. In the **Azure Portal**, navigate to **Microsoft Entra ID**.
2. Under **Manage**, select **Groups** → `+ New Group`.
3. Fill in the group details:
   - Group type: **Security**
   - Group name: `Demo-Admins`
   - Description: `Demo admin security group`
   - Membership type: **Assigned**
4. Add the user **testuser01** (created in Task 6) as a member.
5. Click **Create**.

### Verification
- Verified that `Demo-Admins` group appears in the **Groups list**.
- Confirmed that `testuser01` is listed as a member.

### Notes
This group will be used in **Task 10** to assign the Reader role at the group level.
