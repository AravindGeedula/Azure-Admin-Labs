# Task 10: Assign Reader Role to Group (Demo-Admins)

### Objective
Assign the **Reader** role to the security group `Demo-Admins` so that all its members inherit read-only access.

### Steps
1. In the **Azure Portal**, navigate to the **Resource Group** created in Task 1.
2. Go to **Access control (IAM)** → `+ Add` → **Add role assignment**.
3. In the Role tab:
   - Select **Reader** role.
4. In the Members tab:
   - Choose **User, group, or service principal**.
   - Select the group **Demo-Admins**.
5. Review + Assign.

### Verification
- Group `Demo-Admins` is listed under **Role assignments** with Reader role.
- Any member of the group (like `testuser01`) now automatically has Reader access.

### Notes
Using groups for RBAC ensures easier management of permissions at scale.
