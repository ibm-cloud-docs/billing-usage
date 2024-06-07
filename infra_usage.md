---

copyright:
  years: 2018, 2022
lastupdated: "2022-06-15"

keywords: SoftLayer billing, classic infrastructure usage, orders, IaaS usage, invoice, billing item 

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:help: data-hd-content-type='help'} 
{:support: data-reuse='support'} 
{:new_window: target="_blank"}
{:tip: .tip}


# Viewing usage for your classic infrastructure resources
{: #infra-usage}

You can view your device usage and service purchases for classic infrastructure devices and services by going to **Manage > Billing and usage**.  
{: shortdesc}

## Viewing billing and usage information
{: #infra-billing}

To view billing and usage for classic infrastructure resources, you need an access policy with the Viewer role or higher on the Billing account management service. See [IAM access](/docs/account?topic=account-userroles) for more information.

* Select **Billing items** to view billing items and their associated devices. Billing items are services and products that are not a server, such as storage. Associating a billing item with a device helps you track and organize costs in your invoice.

   By default, the Billing items page displays all associated billing items. You can change your view by clicking the **Associated Billing Items** menu and selecting another option. You can associate or disassociate one item, or expand the **Bulk Actions** operation for multiple items at a time. You can cancel individual billing items at any time.
* Select **Invoices** to view detailed invoices that list your device and service usage and the billed amount for each item.

   To view your billed usage for the current invoicing period, click the link with your next invoice date under Next Recurring Invoice.

   You can download a PDF or spreadsheet copy of an invoice for your offline records by clicking the **Download** icon ![Download icon](../icons/download.svg "Download") and selecting your download options.
   {: tip}

## Viewing device and service purchase information
{: #infra-orders}
{: help} 
{: support}

You can view information about your classic infrastructure device and service purchases by selecting an option from the **Sales** navigation.

* Select **Device upgrades** to view specific information, such as which devices are upgraded and the date the case was created and completed. To view this page, you need an access policy with the Viewer role or higher on the Billing service. 

   You can view all open and closed cases for your infrastructure device upgrades. You can also track the progress of the case, view a logged correspondence with support, and keep track of cases that are opened and completed.
* Select **Orders** to view a list of all the orders made in your account. To view this page, you need the Add/Upgrade Storage (StorageLayer), Add Server, or Add/Upgrade Services [classic infrastructure permission](/docs/account?topic=account-mngclassicinfra). 
* Select **Cancellations** to view all cancellations on your account. To view this page, you need both the Cancel server and Cancel services classic infrastructure permissions.

   You can view a list of all of the cancellations made in the account, and you can view them by type of device or service. The cancellations show the device name and the case number. This list tracks ongoing and closed cases, and you can view your messages with support.  
* Select **Shipments** to view your digital shipments, such as data transfer requests or physical shipments. To view this page, you need an access policy with the Viewer role or higher on the Billing service.
