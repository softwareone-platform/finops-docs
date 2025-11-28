# Anomaly Detection

Anomaly detection is an integral part of a cloud security and management strategy.&#x20;

It helps maintain the integrity and performance of cloud services while identifying and addressing potential issues before they cause significant damage or disruption. An anomaly is defined as a deviation from the normal pattern of cost or usage for a specific resource or group of resources.&#x20;

### Anomaly detection in FinOps for Cloud

Anomaly detection in FinOps for Cloud helps you identify unusual behavior that may indicate a security breach, system malfunction, or other operational challenges.&#x20;

You can create new anomaly detection policies and manage them from the **Anomaly detection** page.

FinOps for Cloud supports two types of anomaly detection policies, including resource-count and cost:

* **Resource count** - These anomalies refer to inconsistencies or unexpected variances in the number of resources being utilized or allocated compared to what is expected or provisioned. Resource count anomalies can occur in various cloud resources, such as virtual machines, storage, network bandwidth, or cloud services, like databases and application servers.&#x20;
* **Expense** - These anomalies refer to instances where the actual financial expenditure on cloud resources deviates significantly from expected or budgeted costs. Expense anomalies can represent underlying issues, such as inefficient resource utilization, misconfigurations, unauthorized access, or even billing errors from cloud service providers.&#x20;

When creating policies, you can also define the evaluation period, thresholds, and filters.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/anomaly_detection (1).png" alt=""><figcaption><p>Anomaly detection in FinOps for Cloud.</p></figcaption></figure></div>

### Additional actions <a href="#additional-actions" id="additional-actions"></a>

From the **Anomaly detection** page, you can create new policies and view existing policies. You can also do the following:

* Select a policy to view detailed policy information, including violations if applicable.
* Search for a specific policy by its name or description.&#x20;
* Track the dynamics in the **Status** column and hover over it to see both the average and current values.
* Check the instances where the policy is applicable. An en dash (–) in the **Filters** column means the policy applies to all cases.
* View the resources connected to policy by selecting the **Show resources** icon in the **Actions** column.&#x20;
