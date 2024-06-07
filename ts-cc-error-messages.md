---

copyright:
  years: 2022, 2023
lastupdated: "2023-03-07"

keywords: credit card, payment method, error credit card, credit card error, payment issue, card issue, card error, card error message, payment error message

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}


# Credit card error messages
{: #cc-error-messages}

An issue might occur when you try to update, add, or remove a credit card. Review the following credit card error messages for detailed self-help information.
{: shortdesc}

## Why was my credit card transaction rejected?
{: #trans-rejected}
{: troubleshoot}

Protecting your identity is a priority and {{site.data.keyword.cloud_notm}} takes credit card verification seriously.
{: shortdesc}

An issue occurred that caused the transaction to fail. For example, the name and address on file with {{site.data.keyword.cloud_notm}} doesn't match the information on file with the company that issued your credit card. This error might prompt the following message:
{: tsSymptoms}

> Error: Could not place order. Problem authorizing the credit card. We are unable to process your request: Transaction Rejected

Something went wrong when verifying your credit card, and the transaction wasn't successful.
{: tsCauses}

To ensure that your credit card verification is successful, complete the following steps:
{: tsResolve}

1. Verify that the name and address for your {{site.data.keyword.cloud_notm}} account matches the name and address on file with your credit card issuer.
2. Verify that the country associated with a VAT or tax identification number matches the country in your {{site.data.keyword.cloud_notm}} account. For example, a VAT ID registered in France can't be associated with an {{site.data.keyword.cloud_notm}} account that is registered in Finland.
3. Verify that you are creating a business account and not a personal account if you are specifying a VAT ID or tax identification number.
4. Review the error message that was displayed. If your transaction was rejected and an email address was not provided, contact your credit card issuer.
5. Contact us by calling 1-866-325-0045 and selecting the third option.

## Why do I get an error when I try to update my credit card?
{: #ts_cc-payment}
{: troubleshoot}

You tried to change your payment method by adding a new credit card in the {{site.data.keyword.cloud_notm}} console [Payments page](/billing/payments){: external}.
{: shortdesc}

After you entered your credit card information and saved it, the following message displayed:
{: tsSymptoms}

> Failed to complete the Change Request process due to the following error: We are unable to process your request: Transaction Rejected.

Something went wrong when verifying your credit card, and the update wasn't successful.
{: tsCauses}

Go to the [Support Center](/unifiedsupport/supportcenter) and click **Create a case**.
{: tsResolve}

## Why was there a general decline of my credit card?
{: #ts-auth-card}
{: troubleshoot}

You tried to make a payment or place an order in the {{site.data.keyword.cloud_notm}} console [Payments page](/billing/payments){: external}, but you get the following error message:
{: tsSymptoms}

> Could not place order. Problem authorizing the credit card. We're afraid this transaction has been rejected. General decline of the card. No other information provided by the issuing bank.

Your credit card issuer has declined the transaction.
{: tsCauses}

Contact your credit card issuer for more information.
{: tsResolve}

## Why is my credit card inactive or not authorized?
{: #ts-inactive-cc-file}
{: troubleshoot}

You tried to make a payment or place an order in the {{site.data.keyword.cloud_notm}} console [Payments page](/billing/payments){: external}, but you get the following error message:
{: tsSymptoms}

> Could not place order. Problem authorizing the credit card. We're afraid this transaction has been rejected. Inactive card or card not authorized for card-not-present transactions.

Some credit card issuers don't allow transactions when it is being initiated by using a credit card on file. You might see this error message if your credit card has been deactivated.
{: tsCauses}

Contact your credit card issuer for more information.
{: tsResolve}

## Why is my credit card not authorized to place an order?
{: #ts-cc-declined-issuer}
{: troubleshoot}

You tried to place an order in the {{site.data.keyword.cloud_notm}} console [Payments page](/billing/payments){: external}, but you get the following error message:
{: tsSymptoms}

> Could not place order. Problem authorizing the credit card.

Your credit card issuer has declined the transaction.
{: tsCauses}

Contact your credit card issuer for more information.
{: tsResolve}

## Why is {{site.data.keyword.cloud_notm}} unable to process my order request?
{: #ts-cc-enablement-issue}
{: troubleshoot}

You tried to place an order in the {{site.data.keyword.cloud_notm}} console [Payments page](/billing/payments){: external}, but you get the following error message:
{: tsSymptoms}

> Could not place order. Problem authorizing the credit card. We are unable to process your request: Transaction Rejected. Please contact Cloud Trust Enablement at verify@us.ibm.com.

{{site.data.keyword.Bluemix}} was unable to process your transaction.
{: tsCauses}

Contact the Cloud Trust and Enablement team by email at verify@us.ibm.com.
{: tsResolve}

## Why was my change request rejected?
{: #ts-cc-change-reject}
{: troubleshoot}

You tried to place an order in the {{site.data.keyword.cloud_notm}} console [Payments page](/billing/payments){: external}, but you get one of the following error messages:
{: tsSymptoms}

> Failed to complete the Change Request process due to the following error: We're afraid this transaction has been rejected. Invalid account number.

or

> Failed to complete the Change Request process due to the following error: We are unable to process your request: Transaction Rejected.

Your credit card number was not recognized by your credit card issuer.
{: tsCauses}

Contact your credit card issuer for more information.
{: tsResolve}

## Why was my change request rejected because of a VAT ID?
{: #ts-cc-change-vat}
{: troubleshoot}

You tried to complete a change request {{site.data.keyword.cloud_notm}} console [Payments page](/billing/payments){: external}, but you get the following error message:
{: tsSymptoms}

> Failed to complete the Change Request process due to the following error: VAT ID is a required field for ...

Your VAT ID, CST or other tax identification number cannot be validated.
{: tsCauses}

Complete the following steps to verify the VAT ID:
{: tsResolve}

1. Verify that tax identification number is valid.
1. Verify that the tax identification number is associated with the same country as the physical country of residence in your {{site.data.keyword.cloud_notm}} profile.
1. Verify whether a VAT ID is required to create an {{site.data.keyword.cloud_notm}} account in your country of residence. For more information, see [Personal use availability](/docs/account?topic=account-account-getting-started#signup-personalaccts).
1. Verify that you are creating the correct account type: personal or business.

## Why was there an error in the payment process?
{: #ts-payment-process-error}
{: troubleshoot}

An issue occurred that caused the payment process to fail. This error might prompt the following message:
{: tsSymptoms}

> There was an error in the payment process: We're afraid this transaction has been rejected. General decline of the card. No other information provided by the issuing bank.

Your credit card issuer has declined the transaction.
{: tsCauses}

Contact your credit card issuer for more information.
{: tsResolve}

## Why is the transaction already processed?
{: #ts-dupe-transaction}
{: troubleshoot}

An issue occurred that caused the payment process to fail. This error might prompt the following message:
{: tsSymptoms}

> Transaction already processed.

Our payment system has detected multiple similar payments within a short period of time. {{site.data.keyword.cloud_notm}} is attempting to avoid unintentional duplicate payments.
{: tsCauses}

Wait 3-4 hours for the manual payment to be processed and posted to your {{site.data.keyword.cloud_notm}} account. Verify your account balance on the [Payments page](https://cloud.ibm.com/billing/payments).
{: tsResolve}

## Why can't I upgrade my account?
{: #ts-upgrade-fail}
{: troubleshoot}

An issue occurred that caused the payment process to fail. This error might prompt the following message:
{: tsSymptoms}

> Your account couldn't be upgraded. Click Upgrade account to try again.

{{site.data.keyword.cloud_notm}} was unable to process your transaction.
{: tsCauses}

Submit your account upgrade information again. If the error continues to occur, you can contact [{{site.data.keyword.Bluemix_notm}} Support](/unifiedsupport/supportcenter){: external}.
{: tsResolve}

## Why can't I save my credit card to the account?
{: #ts-save-cc}
{: troubleshoot}

An issue occurred that caused the payment process to fail. This error might prompt the following message:
{: tsSymptoms}

> Your card could not be saved. Please try another card.

Your card information was incorrect.
{: tsCauses}

Use a different credit card to process your transaction.
{: tsResolve}

## Why was my credit card declined?
{: #ts-decline-cc}
{: troubleshoot}

An issue occurred that caused your credit card to decline. This error might prompt the following message:
{: tsSymptoms}

*Your payment was declined for invoice number…*

You have a credit card on file and it was declined.
{: tsCauses}

Update your credit card information on the [Payments page](https://cloud.ibm.com/billing/payments). Credit card transactions are automatically retried within 24 hours after you update the information.
{: tsResolve}
