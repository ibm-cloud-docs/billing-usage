---

copyright:
  years: 2015, 2024
lastupdated: "2024-01-03"


keywords: payment method, credit card, payment, billing method, pay, pay my bill, billing items, ibm billing,

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Managing payments
{: #linkedusage}

Depending on your account type, you can easily manage your payment methods by using the [Payments](/billing/payments) page in the {{site.data.keyword.cloud}} console or by going to [{{site.data.keyword.IBM}} Billing](https://myibm.ibm.com/billing/).
{: shortdesc}

A valid credit card is required for all Pay-As-You-Go and Subscription accounts. Every month, the credit card is charged with the usage amount that is accumulated during that month. When updates to your payment details are approved, they are applied to your account within 24 hours. The contact that is specified in the billing address section receives an email confirming that the updates are applied.

You can contact {{site.data.keyword.cloud_notm}} Support to get help with payment-related issues. From the console menu bar, click the **Help** icon ![Help icon](../icons/help.svg "Help") > **Support center**, and then click **Create a case** to get in touch.
{: tip}

## Before you begin
{: #prereqs-payments}

To manage payments, you need to be assigned the operator role or higher on the billing account management service. See [Assigning access to account management services](/docs/account?topic=account-account-services) for more information.

## Managing payment methods for new US-based Pay-As-You-Go accounts with credit card billing
{: #manage-paygo-us-account}

If you're a new Pay-As-You-Go account owner that is located in the US and you are paying with a credit card, can you add multiple cards to the account, replace your default card with a saved one, or edit the details of a card. You manage your credit card from the [Payments](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console.

Complete the following steps to add a new payment method to the account:

1. Click **Add payment method**.
2. Enter the card details, and click **Save**. Updates to your card details are reflected immediately.

You can’t enter a PO Box as the billing address.
{: important}

When you add a new credit card, it becomes the default credit card. Recurring payments are charged to the default payment method.

Complete the following steps to edit your active payment method:

1. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Edit** menu.
1. To edit the billing address, click **Edit** and update the billing address.
1. To edit the card details, click **Edit** and update the card number or expiration date.

You can only have one address that's associated with your payment methods. All credit cards in the account will be updated to the same address.
{: note}

Complete the following steps to set a new default payment method:

1. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Set as default**.
2. Confirm that you want to make this payment method the default. The default payment method is charged for recurring payments


## Managing payment methods for all other accounts
{: #manage-other-account}

The steps to update your credit card apply to the following types of accounts:

* New and existing Pay-As-You-Go accounts based in the US with any payment method other than a credit card
* New and existing Pay-As-You-Go accounts not based in the US
* New and existing Subscription accounts worldwide

1. Go to the [Payments](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console.
2. In the Add Payment Method section, enter the billing information for your new card, and click **Add credit card**.

The process for updating a credit card requires a manual review that might take a few days to process. To view your open change request cases, go to [{{site.data.keyword.cloud_notm}} Support](https://cloud.ibm.com/unifiedsupport/supportcenter).

American Express can't be used as a payment method for India, Singapore, and South Africa based accounts that are billed in US dollars.
{: note}


###  India-based customers with accounts that are billed in US Dollars
{: #rupees-billing}

Due to current banking regulations, recurring credit card transactions might be unsuccessful for India-based customers with accounts that are billed in US Dollars. You can use one of the following methods to make a payment:
 * [Make a one-time payment](/docs/billing-usage?topic=billing-usage-linkedusage#makepayment)
 * Request to migrate your account to be billed in India Rupees. To make a request, provide a credit card that is billed in India Rupees on the [Payment Method](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console. Specify that India Rupees are in the **Payment Currency** section. Additional information might be requested through a Support case during the migration process.

### Making a one-time payment
{: #makepayment}

You can use a credit card to make a one-time payment at any time for any amount, whether it's for the full balance or a partial sum. The details that you enter for the one-time payment aren't recorded for future use, and aren't populated with a default amount.

To make a one-time payment, in the {{site.data.keyword.cloud_notm}} console, go to **Manage > Billing and usage**, and select **Payments**. Click **Manual Payment** and complete the fields in the one-time payment section. One-time payments are reviewed and processed each day. The account balance is updated after the payment is accepted. If a late fee is assessed and you have submitted a one-time payment, contact the [{{site.data.keyword.cloud_notm}} Support Center](https://cloud.ibm.com/unifiedsupport/supportcenter){: external}.

## Managing your payment method outside of the console
{: #payment-method-ibm}

You might manage your payment method on a separate billing platform. You can easily register, update, or delete a payment method by going to [IBM Billing](https://myibm.ibm.com/billing/) and log in with your IBMid and password. You are also required to enter the temporary passcode that's emailed to you.

To add a payment method, complete the following steps:
1. Go to [ibm.com](http://www.ibm.com){: external} and log in with the same IBMid and password that you use to log in to {{site.data.keyword.Bluemix_notm}}.
1. Click the **Avatar** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar"), and select **Billing**.
1. Click **Manage payment method**.
1. Enter your payment information, and click **Register**. A temporary passcode is emailed to you after the registration process is complete.

After you register a payment method, when you click **Manage payment method**, you can view the Manage my wallet page to update or delete your payment methods by clicking the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
{: tip}
