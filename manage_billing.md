---

copyright:
  years: 2015, 2020
lastupdated: "2020-09-14"

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

You can use the {{site.data.keyword.cloud}} billing and usage dashboard to make a one-time payment, change your credit card details, view your billing items, and view your invoices.
{: shortdesc}

To manage payments, you need an access policy with the Operator role or higher on the Billing account management service. See [IAM access](/docs/account?topic=account-userroles) for more information.

## Making a one-time payment
{: #makepayment}

You can make a one-time payment at any time, for any amount, whether it is for the full balance or a partial sum. The details that you enter for the one-time payment aren't recorded for future use, and aren't filled out with a defaulted amount. Payment methods for one-time payments include credit card and PayPal. PayPal can’t be used as a payment method for recurring payments.

To make a one-time payment, in the {{site.data.keyword.cloud}} console, go to **Manage > Billing and usage**, and select **Payments**. Complete the fields in the make a one-time payment section. The account balance is updated after the payment is accepted.


## Managing your payment method
{: #changepaymethod}

You can easily manage your payment methods by using the [Payments](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console. Each billable account must have a valid credit card. Every month, the credit card is charged with the usage amount that is accumulated during that month. When your payment details are approved, they are available to use in your account within 24 hours. A confirmation email is sent to the contact entered in the card billing address section.

### Updating your credit card 
{: #update-creditcard}

Updating your credit card is just like adding a new one. Go to the [Payments](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console. In the Add Payment Method section, enter the billing information for your new card, and click **Add credit card**.

Your payment methods might be managed outside of the console. To manage your payment, complete the following steps: 
  1. Go to [ibm.com](http://www.ibm.com){: external} and log in with the same IBMid and password that you use to log in to {{site.data.keyword.Bluemix_notm}}.
  1. Click the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg), and select **Billing**.
  1. Click **Manage payment method**.
  1. Enter your credit card information, and click **Register**.

### Updating PayPal or other payment methods
{: #changepaymethod-paypal}

If you are using a payment method other than a credit card like PayPal, complete the following steps to switch to a different payment method: 

1. In the console, go to **Manage** > **Billing and usage**, and select **Payments**. Then, click **Payment method**.
2. In the Add Payment Method section, select **Pay with Other**, and click **Submit change request**. A support case to change your payment method is then created for you. 

Some payment methods, such as PayPal, aren't accepted as recurring payment methods. You must manually submit the payment each month.
{: note}

## Managing your payment method outside of the console 
{: #payment-method-ibm}

You might manage your payment method on a separate billing platform. You can easily register, update, or delete a payment method by going to [IBM Billing](https://myibm.ibm.com/billing/). You must log in with your IBMid and password. You are also required to enter the temporary passcode that's emailed to you. From there, select **Manage payment method** and then **Manage my wallet** to register, update, or remove your payment method. 

## Getting help with your payments
{: #getting-help-payments}

To report any problems that are related to payments, you can contact the Support team. From the console, click **Support** > **Create a case**.
