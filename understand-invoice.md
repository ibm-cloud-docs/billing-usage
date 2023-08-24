---

copyright:
  years: 2022, 2023

lastupdated: "2023-08-24"

keywords: invoices, understanding invoice, iaas invoice, paas invoice, IBM invoices, invoice information, currency change

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Understanding my invoice
{: #understand-invoices}

Billable accounts receive a monthly invoice for the usage charges and other fees that are incurred. At any time, you can view your invoice or expected invoiced charges by going to the [Invoices](https://cloud.ibm.com/billing/invoices){: external} page from the billing and usage dashboard in the {{site.data.keyword.cloud}} console.
{: shortdesc}

If your account is billed through a separate billing platform, you can see the following message on the Invoices page:

`The account is invoiced on a separate billing platform. This page reflects only classic infrastructure charges. To view your official invoice and for any pricing inquiries, visit IBM Invoices. To sign up and view your invoices, you must provide your IBM customer number. If you don't know your customer number, contact IBM Cloud Support by calling 1-866-325-0045 and selecting the third option.`

In this situation, go to [Invoices@IBM](https://www.ibm.com/support/customer/invoices/welcome){: external} to review your upcoming invoice, past invoices, or details about service charges.

## Invoicing for different account types
{: #different-acct-invoice}

Depending on your account type, your usage is incurred and reflected differently on your invoice. Review the following differences for billing based on your account type:

* Subscription: The billed interval is contractual and depends on a negotiated payment for usage credits.
* Pay-As-You-Go: An estimation of your charges is found on the [Usage](/billing/usage) page. Charges from platform and classic infrastructure services are included if your account uses both types. Infrastructure as a Service (IaaS) charges aren't included.

Third-party services, such as SendGrid, don't bill for their service through {{site.data.keyword.Bluemix_notm}} if you signed up for their service outside of {{site.data.keyword.Bluemix_notm}}.
{: note}

An {{site.data.keyword.Bluemix_notm}} service might provide a free allocation before the start of your billing period. To determine whether your service instance provides a free allocation, go to the [Resources list](/resources) in the {{site.data.keyword.cloud_notm}} console. Click the service name, and then click **Plan**. Review the feature description for each plan to see whether the service offers free allocations. Free allocations are applied to the account level and not the organization level.

<!-- Removed by Bill Wentworth on 20 April 2023 because we don't durrently support it
## Updating currency on your invoice
{: #invoice-currency}

You can change the currency on an invoice by going to the [Monthly Payment Method](/billing/payments){: external} form in the {{site.data.keyword.cloud_notm}} console. Review the following before you update the currency:

* Verify that your account has a $0.00 US dollar balance. Your account can't be changed to local currency if there's a remaining balance.
* Ensure that the credit card information is for an account that can be billed in the new currency.
* Verify that the billing address information in the form matches the billing information on the credit card in the account.
* Provide a tax identification number in the VAT ID field if your account is a business.
* Select the correct currency for the **Request Currency Change to** option.
* Add a physical address to the account to change to a currency other than US dollars. Post office addresses are not accepted.

An account that is invoiced in a currency other than US dollars can't be converted to US dollar invoicing.
{: note}
-->
