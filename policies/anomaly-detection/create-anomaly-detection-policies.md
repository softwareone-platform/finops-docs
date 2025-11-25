# Create New Policies

Organization managers can create a new policy by defining the policy name and description, and configuring the policy parameters. Two types of policies can be created:

* **Resource count** - These anomalies refer to inconsistencies or unexpected variances in the number of resources being utilized or allocated compared to what is expected or what has been provisioned. These anomalies can occur in various cloud resources, such as virtual machines, storage, network bandwidth, or cloud services, like databases and application servers.&#x20;
* **Expense** - These anomalies refer to instances where the actual financial expenditure on cloud resources deviates significantly from expected or budgeted costs. These anomalies can represent underlying issues, such as inefficient resource utilization, misconfigurations, unauthorized access, or even billing errors from cloud service providers.&#x20;

## Creating a new anomaly detection policy

To create a new anomaly detection policy:

1. Navigate to the **Anomaly detection** page, then select **Add**. The **Create anomaly detection policy** page opens.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>The Create anomaly detection policy page.</p></figcaption></figure></div>

2. Enter a descriptive name for the policy and select the policy type:
   * Select **Resource count** if the daily resource count must not exceed the average amount over the last evaluation period, according to the threshold percentage.
   * Select **Expense** if you want FinOps for Cloud to detect when everyday expenses exceed the average sum for the last evaluation period above the threshold percentage.
3. Enter the evaluation period in days and define the threshold percentage.
4. (Optional) Select any filters that will be used to trigger policy alerts. You can apply multiple filters. If applicable, select **Show more** to view all filter options.
5. Select **Save** to finish creating the new policy.

Once the policy has been created, FinOps for Cloud sends an email notification to the Organization Manager every time an anomaly is detected.
