# Quotas and Budgets

Quotas and budgets are two crucial concepts to consider when managing cloud storage. These tools help organizations control costs and manage resources efficiently.&#x20;

Budgets refer to the financial limits an organization sets to manage the costs associated with cloud storage usage, and quotas limit the storage resources a user, application, or department can consume.

### Quotas and budgets in FinOps for Cloud

In FinOps for Cloud, quotas and budgets are used to create policies that ensure cost optimization and compliance with your budget constraints.&#x20;

FinOps for Cloud supports three types of policies, including resource quota, recurring budget, and expiring budget. You can define the policy type along with thresholds and filters during policy creation.&#x20;

Once the policy is created, you can view it on the **Quotas and budgets** page.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/ffc_quotasandbudgets.png" alt=""><figcaption><p>Quotas and budgets in FinOps for Cloud.</p></figcaption></figure></div>

### Additional actions <a href="#additional-actions" id="additional-actions"></a>

From the **Quotas and budgets** page, you can create a new policy and view your existing quotas or budgets. You can also do the following:

* Select a policy to view detailed policy information, including violations if applicable.
* View the timestamp of the last check.&#x20;
* See the current resource count or expense value in the **Status** column. Use the progress bar to understand how close the current value is to the set threshold. The color of the progress bar reflects the ratio of the current value to the quota or budget.
  * **Red** - Indicates that the resource count or expenses exceed the quota or budget.
  * **Yellow** - Indicates that the resource count or expenses are approaching the threshold, specifically in the range of 90% and 100%.
  * **Green** - Indicates that the values are within the limit and don't exceed the quota or budget.
* View all filters that display the criteria used to select resources for the quota or budget.
* View resources connected to a quota or budget by selecting the **Show resources** icon in the **Actions** column.
