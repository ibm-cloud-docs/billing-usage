---



copyright:

  years: 2017, 2018, 2019
lastupdated: "2019-01-09"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# Troubleshooting for managing billing and usage
{: #troubleshoot}

General problems with managing your billing and usage might include the required authority to access your billing information. In many cases, you can recover from the problem by following a few easy steps.
{:shortdesc}


## Why can't I access billing information?
{: #cannot-access-billing-info}
{: troubleshoot}

When you try to access your billing information, such as payments and invoices, you get a message that says the function isn't available.
{: tsSymptoms}

You will get this message because you don't have authorization to view the billing information for the account. You must be an account owner, Cloud Foundry org billing manager, or have an IAM policy on all account management services with the administrator role assigned.
{: tsCauses}

You can view billing information on any account that you're an account owner. A billing manager is able to view billing information for a Cloud Foundry organization. And, for IAM-enabled resources, you must have an IAM policy on all account management services with the Administrator role assigned.

Check your access by completing the following steps:

  1. Go to **Manage > Access (IAM)**, and select **Users**.
  2. Click your name from the Users page.
  3. Click **Access policies** to view your assigned IAM access policies.
  4. Click **Cloud Foundry access** and expand the rows for your assigned orgs to see whether you have an Account owner or Billing manager role.

For more information about IAM access, see [Cloud IAM roles](/docs/iam?topic=iam-userroles). And, for more information about Cloud Foundry access, see [Cloud Foundry roles](/docs/iam?topic=iam-cfaccess).
{: tsResolve}
