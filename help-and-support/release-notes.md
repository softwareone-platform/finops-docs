---
description: >-
  This page includes the latest enhancements, fixes, and new features in
  SoftwareOne’s FinOps for Cloud.
---

# Release Notes

## Release Date: 3 February 2026

### **AWS Data Source Configuration Updates (Read‑Only Compliance)**

To strengthen our alignment with a read‑only operating model and least‑privilege security practices, FinOps for Cloud will **no longer offer the ability to&#x20;**_**automatically**_**&#x20;create AWS Cost and Usage Reports (CUR) or provision their associated S3 buckets**.

#### **Required Action**

Administrative users must now **create and configure CUR exports and S3 buckets directly in AWS** before connecting them to FinOps for Cloud.

#### **Continuity of Service**

FinOps for Cloud continues to support **connecting to existing customer‑managed CUR exports** without requiring elevated permissions.&#x20;

***

## Release Date: 12 December 2025 <a href="#release-date-20-february-2025" id="release-date-20-february-2025"></a>

### Download Recommendations

You can now download insights directly from recommendation tiles, making it easier to export and share optimization suggestions.

### Fixes

* Removed all usages of the deprecated ADAL authentication library and upgraded all Microsoft authentication to MSAL. This is Microsoft's recommended library for all new development. Read about this more at [Microsoft Learn](https://learn.microsoft.com/en-us/entra/identity-platform/msal-migration).
* Minor improvements to **AWS Assumed Role** data source for better reliability.
* Various stability, reliability, and performance improvements.

***

## Release Date: 15 September 2025 <a href="#release-date-20-february-2025" id="release-date-20-february-2025"></a>

### Cost Map for Cloud Spend Analysis

Cost map is a new feature that offers a visual and interactive representation of your cloud spend across regions and cloud providers. The **Cost map** page includes two tabs:

* **Region** - This tab allows you to visualize your spending geographically across cloud deployments.
* **Network traffic** - This tab allows you to analyze costs associated with data transfer and connectivity.

Additionally, the Cost Explorer view now includes a new breakdown option called **Geography**, allowing you to analyze expenses by region.

### New Download Functionality

A new download option has been introduced to facilitate offline analysis, reporting, and integration with external tools. You can now download data from the following modules in FinOps for Cloud:

* **Resources** - Download your resource data as an Excel spreadsheet or JSON file. You can also download Charts as PNG files.
* **Cost explorer** - Download the data as a PDF.&#x20;
* **User management** - Export your list of users as an Excel spreadsheet or JSON file.&#x20;

### New Filters in Resource View

New filtering options are added to the [Resources](../insights/resources/) page to help you narrow down and analyze cloud assets more effectively. You can now filter resources by:

* **Multi-select fields** - This allows you to select multiple values across key dimensions for more flexible filtering.
* **First seen date** - This allows you to identify newly discovered resources.
* **Last seen date** - This allows you to track resources that might have been removed or are inactive.

### Improved Email Formatting

We have enhanced the formatting of monetary values in all email communications.&#x20;

Currency values are now presented consistently for better readability and a reduced risk of misinterpretation, especially in automated alerts and summaries.

***

## Release Date: 15 May 2025 <a href="#release-date-20-february-2025" id="release-date-20-february-2025"></a>

### Global Availability

SoftwareOne's  [FinOps for Cloud](https://portal.finops.softwareone.com/) is a new solution designed to help you optimize costs and manage your resources effectively.&#x20;

With FinOps for Cloud, you can explore and analyze your cloud expenses, monitor resource usage, and implement policies to ensure efficient and cost-effective cloud management. With a user-friendly interface and robust features, the solution provides greater visibility and control over cloud infrastructure. Use the left sidebar to learn more about these features in detail.
