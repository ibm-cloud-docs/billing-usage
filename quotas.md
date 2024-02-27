---

copyright:
  years: 2020, 2024
lastupdated: "2024-02-26"

keywords: quotas, resource group quotas

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Checking your resource group quotas
{: #quotas}

Quotas provide limits for accounts, {{site.data.keyword.ibmcf_full}} orgs and spaces, and resource groups. This documentation discusses quotas for resource groups. For more information, see [Quotas and service limits](https://cloud.ibm.com/docs/vpc?topic=vpc-quotas).

Quotas for [resource groups](/docs/account?topic=account-rgs) limit the number of apps, instances, and memory allowed for that specific resource group. Each resource group in your account has a specific set of quotas. Standard quotas are for resource groups that are created by users with a Lite account, and Pay-As-You-Go quotas are for resource groups that are created with a Pay-As-You-Go account.

The following table shows resource group quota limits.

| Type                | Max apps | Max instances per app | Max app instances memory | Total app memory | Max service instances |
|---------------------|----------|-----------------------|--------------------------|------------------|-----------------------|
| Pay-as-you-go quota | 100      | 32                    | 512G                     | 512G             | 30,000                |
| Standard quota      | 4        | 2                     | 1G                       | 1G               | 1,000                 |
{: caption="Table 1. Resource group quota limits" caption-side="bottom"}

The following definitions explain the quota limit categories for resource groups.


Type
:   Either Pay-As-You-Go quota for Pay-As-You-Go accounts or standard quota for Lite accounts.

Max Apps
:   The maximum number of web applications that you can create in a resource group.

Max Instances Per App
:   The maximum number of instances of the same web application that you can create in a resource group.

Max App Instance Memory
:   The maximum amount of memory allowed for each individual web application instance.

Total App Memory
:   The maximum amount of memory allowed for each individual web application.

Max Service Instances
:   The maximum service instances per resource group. Service instances are different from web application instances.

## Using the CLI to check your quotas
{: #using-cli-quotas}

If you're not sure what your resource group quotas are, you can check by using the {{site.data.keyword.Bluemix_notm}} CLI. The CLI is the only way to check your account's resource group quotas. Before you can check your quotas, you need the [{{site.data.keyword.Bluemix_notm}} CLI installed](/docs/cli?topic=cli-install-ibmcloud-cli).

To check your quotas, type the following command into the CLI:

```
ibmcloud resource quotas
```
{: codeblock}

For more information about using the CLI to check your quotas, see [ibmcloud resource quotas](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_quotas).
