# User Management

The **User management** page in FinOps for Cloud displays a list of existing members within your organization. For each member, you can view details, such as their name, unique ID, last login time, email address, and assigned roles.

From this page, Organization Managers can also invite new members or remove existing members from the organization.&#x20;

## Role overview

In FinOps for Cloud, roles can be assigned when [inviting a user to the organization](../../finops-for-cloud/getting-started/invite-users-to-your-organization.md). &#x20;

By default, the Member role is assigned to allow the individual to have read-only access. You can select other roles and assign them at the pool level. When assigning roles, we recommend assigning the Organization Manager role only to those individuals who need the highest level of access and permission to perform actions without any restrictions.&#x20;

The following table lists the roles in FinOps for Cloud. These roles cannot be edited, and you cannot create new ones.

<table><thead><tr><th width="196">Role</th><th>Description</th></tr></thead><tbody><tr><td><strong>Member</strong></td><td>The <strong>Member</strong> role is assigned by default to all users. <strong>Members</strong> have read-only access across the platform and can view dashboards, resources, pools, policies, recommendations, and analysis features. They can also download reports and exports where supported. <strong>Members</strong> cannot make any modifications to the platform.</td></tr><tr><td><strong>Engineer</strong></td><td>The <strong>Engineer</strong> role is assigned at the resource level. <strong>Engineers</strong> can view the entire platform. This includes pool structures, recommendations, and analysis views, but their editing capabilities are limited to the specific resources they are responsible for. All other areas are available in read-only mode.</td></tr><tr><td><strong>Manager</strong></td><td>The <strong>Manager</strong> role is assigned at the pool level. <strong>Managers</strong> can administer the pools they have been assigned to, including creating and deleting sub-pools, configuring assignment rules, and re-applying resource assignment rules. This permission cascades downward: a <strong>Manager</strong> assigned to a pool automatically has the same management permissions over all child pools beneath it, at every level of nesting. Areas of the platform outside their assigned pools are available in read-only mode.</td></tr><tr><td><strong>Organization Manager</strong></td><td>The <strong>Organization Manager</strong> has full administrative control over the entire FinOps for Cloud environment. This role can invite and remove users, manage all pools and sub-pools across the organization, configure all policy types (anomaly detection, quotas and budgets, and tagging policies), and fully manage data sources. <strong>Organization Managers</strong> also have unrestricted access to all analysis, reporting, and configuration features. This role should be assigned only to individuals who require the highest level of access.</td></tr></tbody></table>

## Which role should I assign?

The right role depends on what a person needs to do in the platform. The table below maps each role to the kinds of team members most likely to need it, using the [FinOps Foundation's standard personas](https://www.finops.org/framework/personas/) as a reference point. In practice, one person may fulfil multiple personas, and not every organization will have all of these roles.

<table><thead><tr><th width="155">Platform role</th><th width="185.333251953125">Likely personas</th><th>Assign this role to people who...</th></tr></thead><tbody><tr><td><strong>Member</strong></td><td>Finance, Product, Procurement, Leadership, ITAM, Sustainability</td><td>Need visibility into cloud spend and usage to inform decisions, reporting, or governance, but have no need to make changes in the platform. A good default for anyone who needs to stay informed without being given edit access.</td></tr><tr><td><strong>Engineer</strong></td><td>Engineering</td><td>Build and operate the cloud infrastructure that generates the costs. They need visibility into recommendations and resource data to act on optimization opportunities, but their changes are scoped to the resources they own.</td></tr><tr><td><strong>Manager</strong></td><td>FinOps Practitioner, Finance, ITFM</td><td>Own cost accountability for a specific business unit, team, or project. They manage a defined pool of cloud spend and need to act on it, creating sub-pools, assigning resources, and responding to budget alerts, but don't need organization-wide control.</td></tr><tr><td><strong>Organization Manager</strong></td><td>FinOps Practitioner, Leadership</td><td>Lead the FinOps practice, own the platform configuration, and need unrestricted access to manage users, data sources, policies, and all pools across the organization. Typically, one or two people.</td></tr></tbody></table>

A few practical guidelines for Organization Managers assigning roles:

* **Default to Member** for anyone whose primary need is visibility or reporting. It is easy to upgrade later.
* **Assign Manager at the right pool level.** A Manager assigned to a top-level pool inherits access to all child pools beneath it, so take care when assigning to high-level pools.
* **Limit Organization Manager access.** This role has no restrictions. It can delete objects, disconnect data sources, and modify all policies. Assign it only to those who genuinely need full administrative control.

## Permissions reference

**Legend**

![][supported] Allowed  
![][notsupported] Not allowed  

### Home

| Feature / Permission | Member | Engineer | Manager | Organization Manager |
|---|---|---|---|---|
| View organization overview | ![][supported] | ![][supported] | ![][supported] | ![][supported] |

### Recommendations

| Feature / Permission | Member | Engineer | Manager | Organization Manager |
|---|---|---|---|---|
| **Overview** |||||
| View recommendations | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Filter recommendations (by data source, category, services) | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Change view (cards / table) | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Search recommendations | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| View recommendations archive | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Run recommendations check | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| Download script | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Download xlsx/json | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| **Recommendation** |||||
| View recommendation settings | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Edit recommendation settings | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| View excluded pools | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Edit excluded pools | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| Pin recommendations | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Dismiss recommendation | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |

### Resources

| Feature / Permission | Member | Engineer | Manager | Organization Manager |
|---|---|---|---|---|
| **Overview** |||||
| View resources | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Filter resources | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| View saved perspective (view) | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Create saved perspective (view) | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| Export expenses chart | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Download xlsx/json | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| **Resource** |||||
| View resource details | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Add assignment rule | ![][notsupported] | ![][notsupported] | ![][supported]¹ | ![][supported] |

### Pools

| Feature / Permission | Member | Engineer | Manager | Organization Manager |
|---|---|---|---|---|
| View pools | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Add / edit / delete pool | ![][notsupported] | ![][notsupported] | ![][supported]¹ | ![][supported] |

### FinOps

| Feature / Permission | Member | Engineer | Manager | Organization Manager |
|---|---|---|---|---|
| View cost explorer | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Filter cost explorer | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Download PDF | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| View expense breakdowns | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| View map | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Filter map | ![][supported] | ![][supported] | ![][supported] | ![][supported] |

### Policies

| Feature / Permission | Member | Engineer | Manager | Organization Manager |
|---|---|---|---|---|
| View anomaly detections | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Add / edit / delete anomaly detection | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| View anomaly detection details | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| View anomaly detection resources | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Export anomaly detection chart | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| View quota or budget | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Add / edit / delete quota or budget | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| View quota or budget resources | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| View tagging policy | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Add / edit / delete tagging policy | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| View tagging policy resources | ![][supported] | ![][supported] | ![][supported] | ![][supported] |

### System

| Feature / Permission | Member | Engineer | Manager | Organization Manager |
|---|---|---|---|---|
| Invite users | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| Download xlsx/json | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| View last login date and time | ![][notsupported] | ![][notsupported] | ![][supported] | ![][supported] |
| Delete users | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| View data sources | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Add data source | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| Rename data source | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| Update data source credentials | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| Perform billing re-import | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| Disconnect data source | ![][notsupported] | ![][notsupported] | ![][notsupported] | ![][supported] |
| View events | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Filter and search events | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| View organization details | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| View and accept invitations | ![][supported] | ![][supported] | ![][supported] | ![][supported] |
| Manage email notifications | ![][supported] | ![][supported] | ![][supported] | ![][supported] |

## Notifications reference

| Notification                          | Member | Engineer | Manager | Organization Manager |
| ------------------------------------- | ------ | -------- | ------- | -------------------- |
| **FinOps**                            |        |          |         |                      |
| Weekly expense report                 | —      | —        | Yes     | Yes                  |
| Pool limit exceed alert               | —      | —        | Yes     | Yes                  |
| Pool limit alert                      | Yes    | —        | Yes     | Yes                  |
| Saving spike                          | —      | —        | Yes     | Yes                  |
| **Policy alerts**                     |        |          |         |                      |
| Resource constraints report           | —      | Yes      | Yes     | Yes                  |
| Resource constraint violation alert   | —      | Yes      | Yes     | Yes                  |
| Anomaly detection                     | —      | —        | Yes     | Yes                  |
| Expiring budget policy violation      | —      | —        | Yes     | Yes                  |
| Quota policy violation                | —      | —        | Yes     | Yes                  |
| Recurring budget policy violation     | —      | —        | Yes     | Yes                  |
| Tagging policy violation              | —      | —        | Yes     | Yes                  |
| **Recommendations**                   |        |          |         |                      |
| New security recommendation detection | —      | —        | Yes     | Yes                  |
| **System notifications**              |        |          |         |                      |
| Environment changed                   | —      | Yes      | Yes     | Yes                  |
| Expenses initial processing completed | —      | —        | Yes     | Yes                  |
| Report import failed                  | —      | —        | Yes     | Yes                  |
| **Account management**                |        |          |         |                      |
| Invitation notification               | Yes    | Yes      | Yes     | Yes                  |

---

[supported]: ../../.gitbook/assets/dark_mode_icon_supported.png
[notsupported]: ../../.gitbook/assets/dark_mode_icon_notsupported.png
