---

copyright:
  years: 2015, 2021
lastupdated: "2021-09-26"

keywords: payment method, credit card, payment, billing method, pay, pay my bill, billing items, ibm billing, 

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}

# Managing payments
{: #linkedusage}

Depending on your account type, you can easily manage your payment methods by using the [Payments](/billing/payments) page in the {{site.data.keyword.cloud}} console or by going to [{{site.data.keyword.IBM}} Billing](https://myibm.ibm.com/billing/). 
{: shortdesc}

A valid credit card is required for all Pay-As-You-Go and Subscription accounts. Every month, the credit card is charged with the usage amount that is accumulated during that month. When updates to your payment details are approved, they are applied to your account within 24 hours. The contact specified in the billing address section receives an email confirming that the updates are applied. 

You can contact {{site.data.keyword.cloud_notm}} Support to get help with payment-related issues. From the console, click **Support** > **Create a case** to get in touch.
{: tip}

## Before you begin
{: #prereqs-payments} 

To manage payments, you need to be assigned the operator role or higher on the billing account management service. See [Assigning access to account management services](/docs/account?topic=account-account-services) for more information.

## Managing payment methods for new US-based Pay-As-You-Go accounts with credit card billing
{: #manage-paygo-us-account}

If you're a new Pay-As-You-Go account owner located in the US and you are paying with a credit card, you can replace your current card with a new one or edit the details of an existing card. In either case, you manage your credit card from the [Payments](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console.

Complete the following steps to replace your existing credit card with a new one: 

1. Click **Add card**. 
2. Enter the card information, and click **Save**. Updates to your card details are reflected immediately. 

You can have only one credit card on file. When you add a new card, your existing card is removed from the account.
{: note}

Complete the following steps to edit your active card:

1. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Edit**.  menu. 
2. Update the card number or expiration date. 
3. To update the billing address, contact [{{site.data.keyword.cloud_notm}} Support](https://cloud.ibm.com/unifiedsupport/supportcenter){: external}.

##  Managing payment methods for all other accounts 

The steps to update a payment method apply to the following types of accounts: 

 * New and existing Pay-As-You-Go accounts based in the US with any payment method other than a credit card
 * New and existing Pay-As-You-Go accounts not based in the US
 * New and existing Subscription accounts worldwide

1. Go to the [Payments](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console. 
2. In the Add Payment Method section, enter the billing information for your new card, and click **Add credit card**.
 
The process for updating a credit card requires a manual review that might take a few days to process. To view your open change request cases, go to [{{site.data.keyword.cloud_notm}} Support](https://cloud.ibm.com/unifiedsupport/supportcenter).
{: tip}

American Express can't be used as a payment method for India, Singapore, and South Africa based accounts that are billed in US dollars.
{: note}

### Updating PayPal or other payment methods
{: #changepaymethod-paypal}

If you're using a payment method that's not a credit card, complete the following steps to switch to your payment method:

1. Go to the [Payments](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console. 
2. Click **Payment method**.
3. In the Add Payment Method section, select **Pay with Other**, and click **Submit change request**. A support case to change your payment method is then created for you. 

Some payment methods, such as PayPal, aren't accepted as recurring payment methods. You must manually submit the payment each month.
{: note}

### Making a one-time payment
{: #makepayment}

You can make a one-time payment at any time for any amount, whether it is for the full balance or a partial sum. The details that you enter for the one-time payment aren't recorded for future use, and aren't filled out with a defaulted amount. Payment methods for one-time payments include credit card and PayPal. PayPal can’t be used as a payment method for recurring payments.

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
