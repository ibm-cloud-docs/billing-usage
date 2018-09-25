---

copyright:

  years: 2015, 2018

lastupdated: "2018-09-25"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Estimating your costs
{: #cost}

You can use different methods to estimate the cost of using {{site.data.keyword.Bluemix}} platform as a service (PaaS) and infrastructure as a service (IaaS) resources to build and host your apps.
{:shortdesc}

You can use the following methods to determine your costs:
* Use the [pricing calculator ![External link icon](../icons/launch-glyph.svg)](https://console.bluemix.net/pricing/){: new_window} to estimate the total cost of the platform and infrastructure resources that you want to use.
* Use the cost estimators on the {{site.data.keyword.Bluemix_notm}} {{site.data.keyword.pricing_sheet}}
to see a rough estimation of the cost based on the size of your app.
* Use the cost calculator on the Pricing page to see accurate app prices based on your input of runtime and service usages.
* Calculate your cost manually.

## Using the pricing calculator
{: #pricing-calculator}

You can use the pricing calculator to estimate the cost of platform and many infrastructure resources before you make a purchase.
The pricing calculator provides the following functions:
  * Cost estimates that are currently provided in USD currency.
  * Estimates for infrastructure resources that are currently available for the **Compute** and **Containers** categories.
  * Cost estimates of resources that do not currently include discounts.
  * Estimates of costs are provided for planning purposes.

1. Access the pricing calculator in one of the following ways:
  * From the [Pricing page ![External link icon](../icons/launch-glyph.svg)](https://www.ibm.com/cloud/pricing){: new_window}, click **Try the calculator** from the Explore our solutions section.
  * If you are not currently logged in to {{site.data.keyword.Bluemix_notm}}, click **Pricing** from the [{{site.data.keyword.Bluemix_notm}} home page ![External link icon](../icons/launch-glyph.svg)](https://console.bluemix.net/).
2. From the **Infrastructure** or **Platform** lists, select the category of the resource you want to price. The resources in the category that you selected are shown, and you can also search the category for a specific resource.
3. Select a resource in the category to see a description of it. Some resources have multiple options. For example, if you select **Infrastructure** > **Compute** > **Bare metal servers**, you can choose from a list of servers.
4. Select the quantity of the resource to add.
5. Click **Add to estimate**.
6. Continue adding resources from the **Infrastructure** and **Platform** categories until you add what you want to estimate. The **Estimate** panel shows the resources you added, the price for each one, and a total price.
7. Optionally, to create a PDF of the information in the **Estimate** panel when you have finished compiling your list of resources, click **Download PDF**. You might want to create a PDF, for example, to review the resources you are pricing before you purchase or to use as a guide when you are purchasing your resources.


If you are pricing only platform resources, to see an estimate in a currency other than USD, you can click **Looking for the Classic Calculator?**. The classic calculator does not include infrastructure resources.
{: tip}

### Using the classic calculator for platform resources
{: #calculator}

To calculate your platform resource costs in a currency other than USD, you can use the classic calculator. The classic calculator does not provide pricing estimates for infrastructure resources.

1. Go to the {{site.data.keyword.Bluemix_notm}} {{site.data.keyword.pricing_sheet}}.
2. Select one of the options in the Infrastructure to support all your workloads section.

To use the calculator, type your projected monthly usage of the listed resources; for example, number of instances or push notifications. The calculator displays the price for your input immediately. You can also adjust the calculator to display yearly costs instead of monthly costs.

## Calculating your costs manually
{: #manual}

You might want to estimate your {{site.data.keyword.Bluemix_notm}} costs yourself to better understand how {{site.data.keyword.Bluemix_notm}} costs are calculated. You can calculate the total price of using {{site.data.keyword.Bluemix_notm}} to build and host your app by considering the prices of the runtime and the services it uses. The prices of runtimes and services sometimes change, so you must refer to the latest information on the {{site.data.keyword.Bluemix_notm}} Pricing Sheet when you calculate the total price.

## Supported billing currencies

The following table lists the billing currencies that are available.

|ISO 4217 code| Currency|
|-------------|---------|
|AUD |	  Australian dollar|
|BRL |	  Brazilian real|
|CAD |	  Canadian dollar|
|CHF |	  Swiss franc|
|DKK |	  Danish krone|
|EUR |	  Euro|
|GBP |	  Pound sterling|
|INR |	  Indian rupee|
|JPY |	  Japanese yen|
|KRW |	  South Korean won|
|NOK |	  Norwegian krone|
|NZD |	  New Zealand dollar|
|SEK |	  Swedish krona|
|USD |    United States dollar|
|ZAR |	  South African rand|
{:caption="Table 1. Supported currencies" caption-side="top"}

If you linked your {{site.data.keyword.Bluemix_notm}} and SoftLayer accounts, the single invoice you receive is in United States dollars (USD) only. For more information, see [Consolidated billing for linked accounts](/docs/account/linking_accounts.html).
{: tip}
