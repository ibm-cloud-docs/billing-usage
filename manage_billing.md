---



copyright:

  years: 2015, 2018
lastupdated: "2018-04-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Managing usage for {{site.data.keyword.Bluemix_notm}} linked accounts
{: #linkedusage}

If you have a linked {{site.data.keyword.Bluemix}} and SoftLayer account, you can use the customer portal to make a one-off payment, change your payment card details, view your billing items, and view your invoices.
{: shortdesc}

The billing and usage options that are displayed in the {{site.data.keyword.Bluemix_notm}} console can be different if you have a Lite account or you don't have a linked account.
{: tip}

## Making a payment
{: #makepayment}

You can make a one-off payment at any time. The payment can be for the full balance or a partial amount. The details that you enter for the payment are not recorded. Complete the following steps to make a one-off payment:

1. From the menu bar, click **Manage** > **Billing and Usage** > **Make a Payment**.  
2. In the **Payment Amount** field, enter the amount that you want to pay.
3. Select your payment method:
 * Paying with a credit card. Enter your card details and the card billing address. Then, click **Make Credit Card Payment**.
 * Paying with PayPal. Enter your details when prompted to complete the payment.

Resolve any reported problems with the payment. The account balance is updated after the payment is accepted. You can contact the Support team by clicking **Support** > **Add Ticket**.

## Changing your payment method
{: #changepaymethod}

Each billable account must have a registered credit card that is valid. Every month, the credit card is charged with the usage amount that is accumulated during that month. In the {{site.data.keyword.Bluemix_notm}} console, complete the following steps to add or change your payment details:

1. From the menu bar, click **Manage** > **Billing and Usage** > **Modify Payment Method**.  
2. In the Add Payment Method section, enter your credit card details and the card billing address. Then, click **Add Credit Card**.

Your card details are validated and your card is then available to use in your account within 24 hours. A confirmation email is sent to contact entered in the card billing address section.

## Viewing your billing items
{: #viewbilling}

You can associate or disassociate billing items to specific devices. By default, the **Billing Items** page displays associated billing items. You can change the view by selecting an option from the display menu. You can associate or disassociate one item or use the Bulk Actions operation to associate or disassociate multiple items at a time. You can also cancel individual billing items at any time. 

1. Select the **Menu icon ![Menu icon](../icons/icon_hamburger.svg) > Infrastructure** option. 
2. From the menu bar, click **Account** > **Billing** > **Billing Items**.
3. To filter your view, select a billing item option from the list.

## Viewing your invoices
{: #viewinvoices}

You can view or pay your invoices at any time. Each invoice is summarized by Invoice Number, Date, Invoice Type, and various monetary balances. The invoice types are described in the following list:

 *  New: the first invoice in a series of recurring invoices
 *  Recurring: an invoice for recurring charges that are active on the account for more than one month
 *  One-time charge: a one-time charge for various expenses, which might include overages
 *  Credit: a credit from {{site.data.keyword.Bluemix_notm}} to the account balance
 *  Refund: a refund, or reversal, for either a one-time or recurring charge

The **Invoices** page also displays a billing summary for the account, which includes the current and estimated next balance, the payment method, and the last and next recurring invoice dates.

Complete the following steps to view an invoice:

1. Select the **Menu icon ![Menu icon](../icons/icon_hamburger.svg) > Infrastructure** option. 
2. From the menu bar, click **Account** > **Billing** > **Invoices**.
3. You can view an invoice in the customer portal or download the invoice.

## Using {{site.data.keyword.Bluemix_notm}} services with SoftLayer assets
{: #combined}

You can easily use API-based public {{site.data.keyword.Bluemix_notm}} services with your SoftLayer assets. All APIs are secure and encrypted so that your data is protected.

For example, do you want to add cognitive capabilities from Watson to your apps that are running on bare metal servers from SoftLayer? You can add a service such as {{site.data.keyword.personalityinsightsshort}} to help understand your app's user in four steps:

1. Find the service in the catalog.
2. Provision an instance of the service with just a few clicks.
3. Set up the service to run with your existing code by copying the service credentials and adding them to your application.
4. After the update to the app, deploy the new version on your SoftLayer infrastructure.

You can gain Insights and Cognitive knowledge by calling Watson APIs from your apps in SoftLayer to make them more personalized. Or, use Data and Analytics services to tap into high-performance analytics for your apps. Or, choose database-as-a-service where you can leave the management to {{site.data.keyword.Bluemix_notm}}.

Modernize your application development by using containers with services like {{site.data.keyword.activedeployshort}} and {{site.data.keyword.deliverypipeline}}. You can then use the {{site.data.keyword.vpn_short}} service to communicate with SoftLayer to connect your container in a private network to the SoftLayer private network. All of the usage charges of the compute resources and services are reflected in your {{site.data.keyword.Bluemix_notm}} bill.
