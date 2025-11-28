# Create Quota or Budget Policies

Organization Managers can create a new quota or budget policy using the **Add** option on the **Quota and budgets** page.

### Creating a new quota or budget

To create a new policy:

1. Navigate to the **Quota and Budgets** page, then select **Add**.&#x20;
2. On the **Create quota or budget policy** page, provide a descriptive name for the new policy and select the policy type. The following options are available:
   * **Resource quota** - Triggers once per day if the current number of resources exceeds the limit.&#x20;
   * **Recurring budget** - Triggers once per month if the expenses for the current month exceed the limit.
   * **Expiring budget** - Triggers when the total expenses from the start date exceed the limit.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/create_quota_budget.png" alt=""><figcaption><p>Create quota or budget policy in FinOps for Cloud. </p></figcaption></figure></div>

3. Enter the values in the additional fields according to your selected policy type.&#x20;
   * For a resource quota policy, enter the maximum number of resources.
   * For a recurring budget policy, enter the monthly budget value.
   * For an expiring budget policy, enter the total budget and the start date.
4. &#x20;(Optional) Apply additional filters as needed.
5. Select **Save** to finish creating the new policy.&#x20;

When the policy has been created, use the **Status** column on the **Quota and Budgets** page to view the current resource count or expense value. If the value exceeds the quota or budget, the progress bar turns red. Otherwise, it remains green. The progress bar also indicates how close the current value is to the set threshold values.
