---

copyright:
  years: 2019
lastupdated: "2019-09-04"

keywords: enterprise usage, view enterprise costs, account group usage, account usage, cost recovery, chargeback, support cost

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:external: target="_blank" .external}
{:note: .note}


# Viewing usage in an enterprise
{: #enterprise-usage}

You can track resource and support costs from accounts in your {{site.data.keyword.Bluemix}} enterprise by viewing their usage. The accounts and account groups that you can view usage for depends on your assigned access.
{: shortdesc}

{{site.data.keyword.Bluemix_notm}} enterprises enable you to centrally manage multiple {{site.data.keyword.Bluemix_notm}} accounts. As an enterprise user, you can keep an eye on resource usage and the associated costs for any account in the enterprise. See [What is an enterprise?](/docs/account?topic=account-enterprise) for more information.

## Required access for viewing enterprise usage
{: #enterprise-usage-access}

In an enterprise, access to usage information is controlled by the Enterprise service. To view usage information, users must be invited to the enterprise account and have the Usage Reports Viewer, Editor, or Administrator role on the Enterprise service. The Usage Reports Viewer role provides access only to viewing usage reports, while the Editor and Administrator roles enable additional enterprise management actions. In keeping with security best practices, assign the least amount of access that is needed for the user to complete their task. For more information, see [Enterprise actions and roles](/docs/iam?topic=iam-account-services#enterprise-account-management).

You can give users granular access so that they can view usage for a certain account or account group. For example, say that your enterprise has account groups for each department, and each department has account groups for each team. You can scope the access so that each enterprise user can see only the information that is needed to fulfill their job role.
   * Your financial officer needs to view usage for the entire enterprise so that they can track and recover costs for each department, but they don't need to create accounts or account groups. Assign them the Usage Reports Viewer role for the enterprise.
   * Each department lead needs to view usage for their department, and they also need to create and manage accounts and account groups for their teams. Assign each department lead the Editor role for their department's account group.
   * Each team lead needs to view their team's usage, but you want them to get department approval to add new accounts to their team. Assign each team lead the Usage Reports Viewer role for their team's account group. They can view usage from all accounts within the account group, but not the usage from the account groups of other teams in the department.

For detailed steps about assigning enterprise access, see [Assigning enterprise access](/docs/iam?topic=iam-assign-access-enterprise).

## Viewing enterprise usage
{: #enterprise-usage-console}

1. Log in to the enterprise account.
1. Go to **Manage > Billing and usage**, and select **Usage**.

   The Usage page displays the costs for all resource usage in the entire enterprise during the current month. Usage is organized according to your enterprise hierarchy, so costs are broken down by the accounts and account groups that are directly under the enterprise. 
   
   In the Support section, you can view the total support costs for all accounts within your enterprise. The starting credit reflects the monthly amount in your support subscription. If the support usage for the month was more than this amount, it's displayed as overage.

   Usage information for classic infrastructure services is not included for the current billing period. However, it is included for previous billing periods, which you can view by selecting an earlier month from the **Time frame** menu. For more information, see [Viewing usage for your classic infrastructure resources](/docs/billing-usage?topic=billing-usage-infra-usage).
1. To view usage within an account group, click the account group name in the table or in the **Enterprise level** menu. Similar to the enterprise level, usage is broken down by the account and account group.

   If an account group doesn't contain any accounts, it isn't displayed on the Usage page.

1. To view usage by resource, go to the account level by clicking through account groups in the table or selecting the account from the **Enterprise level** menu. Costs for each type of resource that was used during the time frame are displayed.

   From the enterprise account, you can't view usage data for the resource plan or instance because it requires access within the account. If you're a user in the account, switch to the account to view this data. You need billing access to the resources and services in the account as described in [Viewing your usage](/docs/billing-usage?topic=billing-usage-viewingusage).

Only data for usage that is incurred by accounts in the enterprise is displayed in the enterprise account. To view usage from before an account was added to the enterprise, log in to that account and select the relevant time frame.
{: note}

### Viewing enterprise usage by using the CLI
{: #enterprise-usage-cli}

You can get a report of usage for the enterprise, an account group, or a specific account.

1. Log in, and select the enterprise account.

   ```
   ibmcloud login
   ```
   {:codeblock}

1. If you want to view usage for a specific account group or account, find the name or ID by running the **`ibmcloud enterprise`** command.

   For example, the following command displays all account groups in an enterprise.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}

1. View usage by running the **`ibmcloud billing`** command as shown in the following examples.

   * View usage for the entire enterprise for the current month.

      ```
      ibmcloud billing enterprise-usage
      ```
      {: codeblock}

   * View usage for the `Development` account group for July 2019.

      ```
      ibmcloud billing enterprise-usage --account-group Development --month 2019-07
      ```
      {:codeblock}

   * View the usage for the account groups and accounts that are directly under the enterprise.

      ```
      ibmcloud billing enterprise-usage --children
      ```
      {:codeblock}

   By default, the commands output the usage report for the current month in the following format. Most costs are listed as billable costs. Non-billable costs are listed only in rare cases, such as for the month when you add a trial account to the enterprise.

   ```
   Name             Type            Billable Cost   Non-billable Cost   Currency   Month   
Example Corp     account         123.45          0                   USD        2019-07   
Development      account_group   234.56          0                   USD        2019-07   
Marketing        account_group   345.67          0                   USD        2019-07   
Sales            account_group   456.78          0                   USD        2019-07
   ```

   You can output the report in JSON format by specifying the `--output JSON` option.
   {: tip}

### Viewing enterprise usage by using the API
{: #enterprise-usage-api}

You can get usage reports from an enterprise and its accounts by calling the [Enterprise Usage Reports API (Beta)](https://{DomainName}/apidocs/enterprise-apis/resource-usage-reports){: external}. You can base the query in your API call on an enterprise, an account group, or an account and specify whether to view the entity or its children. The Enterprise Usage Reports API is a beta release.

The following examples show queries that you can use to get different usage reports. When you call the API, replace the ID variables and IAM token with the values from your enterprise.

View usage for the entire enterprise for the current month.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

View usage for an account group for July 2019.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?account_group_id=$ACCOUNT_GROUP_ID&month=2019-07" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

View usage for account groups and accounts directly under the enterprise.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID&children=true" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}


## Recovering costs for enterprise usage
{: #enterprise-cost-recovery}

An enterprise consolidates billing from all of its accounts and account groups to a single invoice, which simplifies billing management. You can recover the costs from resource usage in the enterprise by charging the usage costs for each account group or account to the associated department or team.

To view your enterprise hierarchy and any usage, you need an access policy with the Editor or Administrator role on the Enterprise service for the entire enterprise. The following steps use the {{site.data.keyword.Bluemix_notm}} console as an example, but you can also perform these steps by using the CLI or API.

1. Find the usage costs for each department by going to **Manage > Usage** in the enterprise account. From the **Time frame** menu, select the previous month to view the usage that is included in the latest invoice.

  The costs for your account groups are listed in the table. These costs include all charges except any tax that's charged in your billing region. If you want a further breakdown of usage costs, click the account group name to view the accounts and account groups that it contains.

1. Identify the departments within your company that correspond with the account groups.

   If the contacts that are assigned to your account groups are associated with the department that you want to recover costs from, finding the contact is one way to find this information. Go to **Manage > Enterprise** and select **Accounts**. The contact for each account group is listed in the table.

   However, billing practices vary by company. For example, the account group contact might be a technical focal that's not associated with the department that you want to charge. Always verify the correct department according to your company's accounting processes.

   If your company uses billing codes to charge back costs to departments, add the billing code to the account group name to easily identify the code. For example,`Sales - A2B3`.
   {: tip}

1. Pair the usage costs for each account group with the identified department, and follow your company's processes to submit the charges.
