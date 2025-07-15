# User Management

The **User management** page lets you view current members and invite new ones to your organization. From this page, you can also remove an individual from your organization.

## User management roles

In FinOps for Cloud, you can assign roles when you are [inviting a user to your organization](../../finops-for-cloud/getting-started/invite-users-to-your-organization.md). &#x20;

By default, the Member role is assigned to allow the individual to have read-only access. You can select other roles and assign them at the pool level. When assigning roles, we recommend assigning the Organization Manager role only to those individuals who need the highest level of access and permission to perform actions without any restrictions.&#x20;

The following table lists the predefined roles available in FinOps for Cloud. These roles cannot be edited, and you cannot create new ones.

<table><thead><tr><th width="196">Role</th><th>Description</th></tr></thead><tbody><tr><td>Organization manager</td><td><p>This role has the highest level of access and control. It can perform all actions, including inviting new users, changing roles, creating pools and sub-pools, and managing policies such as anomaly detection, quotas, budgets, and tagging. </p><p>Organization managers can also add new data sources and manage all resources within the organization.</p></td></tr><tr><td>Manager</td><td><p>This role is assigned at the Pool level and can create sub-pools within that pool. </p><p>Managers can manage resources within their assigned pools, ensuring they are utilized efficiently. The access is limited to the Pool level, and they don't have the same level of control as the Organization Manager. Other functionalities are available in read-only mode.</p></td></tr><tr><td>Engineer</td><td><p>This role is assigned at the resource level and has read-only access to the other functionalities. </p><p>Engineers can manage their resources, ensuring they are used efficiently and effectively. However, they can't create new pools or sub-pools.</p></td></tr><tr><td>Member</td><td><p>Members have read-only access to all features. </p><p>They can view the information and stay updated through notifications, but they can't make any changes or manage resources.</p></td></tr></tbody></table>
