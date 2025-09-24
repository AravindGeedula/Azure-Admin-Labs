# Task 26: Enable Custom Auto-Scaling for VMSS based on CPU Utilization

## Description
Configured auto-scaling for an existing Virtual Machine Scale Set (**vmss-demo**) integrated with a Load Balancer (**lb-vmss-demo**) to automatically adjust instances based on CPU utilization.

## Steps Executed

1. **Pre-requisites**
   - Verified VMSS (**vmss-demo**) and Load Balancer (**lb-vmss-demo**) were already deployed.

2. **Navigate to Scaling Pane**
   - Opened VMSS → **Scaling**.
   - Selected **Custom autoscale** instead of manual scaling.

3. **Configured Scale Settings**
   - Mode: **Scale based on a metric**
   - Minimum instances: **2**
   - Maximum instances: **2**
   - Default instances: **2**
   - Schedule: Set to current date/time.

4. **Added Scale Rule**
   - Metric: **Percentage CPU**
   - Trigger: If CPU > **70%**, increase instance count by +1.
   - This rule simulates real-world scaling behavior for high CPU load.

5. **Resolved Error**
   - Subscription was not registered to use **Microsoft.Insights**.
   - Registered the resource provider manually from Azure CLI.

6. **Validation**
   - Saved and deployed autoscale settings.
   - Confirmed policy visible in **Azure Portal → Autoscale Settings**.

## Outcome
✅ VMSS now has auto-scaling enabled.  
✅ Scaling policy based on CPU utilization successfully applied.  
✅ Subscription registered and autoscale rules visible under monitoring.  
