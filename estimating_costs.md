---

copyright:
  years: 2015, 2023


lastupdated: "2023-02-13"


keywords: quote cost, find cost, estimate cost, estimate bill, total cost, service cost, cost estimator, infrastructure quote, compute quote, vsi quote, bare metal quote, savings plan

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Estimating your costs
{: #cost}

You can use the cost estimator to estimate the cost of {{site.data.keyword.Bluemix}} products by customizing plans that fit your business needs. Your account type doesn't affect your estimates. Explore the catalog to find available products to add to an estimate.

Estimates can now be saved to an account. Make sure you're in the account that you want to save the estimate to. If you have existing estimates, they must be converted to a saved estimate that is attached to an account.
{: important}

## Creating an estimate
{: #new-estimate}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Cost estimator** icon![Cost estimator icon](../icons/calculator.svg "Cost estimator").
1. From the Estimating your costs page, click **Create estimate**.
1. Enter a name and description for the estimate.
1. Click **Create**
1. From the estimate details page, click **Go to catalog** to add products to the estimate.
1. Select the product that you are interested in.

      Depending on the product, an interim informational page might be displayed. For example, if you select {{site.data.keyword.baremetal_short}}, an informational page that describes various features is displayed. Click **Continue**.

1. Select your pricing plan and enter other configuration details if needed. Then, click **Add to estimate**.

   Some products might require that you log in to add them to an estimate.
   {: note}

1.  Enter your estimated usage, and click **Calculate Cost**. You can adjust the estimated usage and recalculate the cost to see how different usage levels affect the overall cost.

      By default, the estimator shows the pricing and billing currency set for your account. Pricing can vary by region. If you're estimating costs for a different location or currency, you might have to select the appropriate currency on the order summary page for the product or change the currency on your account.

1. Click **Save** and select the estimate that you'd like to add the product to, and then add the calculated cost to your estimate by clicking **Save**.
1. When you're done adding products to your estimate, review the product details, and click **View estimate**.

## Updating an existing estimate
{: #update-estimate}

You can always update the name and description of an estimate as your needs change. To edit an estimate, complete the following steps:

1. From the **View Estimate** page, identify the estimate that you want to edit.
1. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Edit**.
1. Enter the updated name and description.
1. Click **Save**

## Saving and sharing your estimate
{: #share-estimate}

When you create an estimate, you can save each estimate's unique link to share or revisit directly through your browser. To share an estimate, complete the following steps:

1. From the **View Estimate** page, identify the estimate that you want to share.
1. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Share**.
1. Click **Copy link** and share the link with users in your account.

## Creating quotes for classic infrastructure services
{: #quotes}

You can generate and view quotes for only {{site.data.keyword.baremetal_short}}, Virtual Server, and Gateway add-ons. Any user with access to the account can create quotes. To view quotes, you need to either be the account owner or have the Add/Upgrade Storage (StorageLayer), Add Server, or Add/Upgrade Services [classic infrastructure permission](/docs/account?topic=account-mngclassicinfra).

1. Generate a quote by clicking **Save as quote** from the Order Summary section on the product details page. Or contact a {{site.data.keyword.Bluemix_notm}} sales representative.

      If you're in a Lite account, select **Email quote** when you enter your contact details so that you can view your quote after you create it. Only billable accounts can view quotes in the console.

1. View your quote by going to **Manage > Billing and usage**, and select **Sales > Device quotes**. If you have access, you can purchase the quoted product by clicking the quote and confirming the order.


## Supported billing currencies
{: #supported-bill-currencies}

The following table lists the supported billing currencies.

Any Pay-As-You-Go accounts created after 25 October 2021 are billed in USD. There are exceptions that apply to users in India who are billed in INR by using a credit card. Also, if you're working with {{site.data.keyword.cloud_notm}} Sales to set up a Subscription account or the Enterprise Savings Plan billing model, you can still be billed in your local currency.
{: note}

| ISO 4217 code | Currency             |
|---------------|----------------------|
|AUD            | Australian dollar    |
|BRL            |	Brazilian real       |
|CAD            |	Canadian dollar      |
|CHF            |	Swiss franc          |
|DKK            |	Danish krone         |
|EUR            |	Euro                 |
|GBP            |	Pound sterling       |
|INR            |	Indian rupee         |
|JPY            |	Japanese yen         |
|KRW            |	South Korean won     |
|NOK            |	Norwegian krone      |
|NZD            |	New Zealand dollar   |
|SEK            |	Swedish krona        |
|USD            | United States dollar |
|ZAR            |	South African rand   |
{: caption="Table 1. Supported currencies" caption-side="top"}
