---

copyright:

  years: 2015, 2018

lastupdated: "2018-04-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# How to calculate your costs
{: #cost}

You can use different methods to estimate the cost of using {{site.data.keyword.Bluemix}} PaaS and IaaS resources to build and host your apps.
{:shortdesc}

You can use the following methods to determine your costs:
* Use the [Pricing Calculator ![External link icon](../icons/launch-glyph.svg)](https://console.bluemix.net/pricing/){: new_window} to compile a list of the platform and infrastructure resources you want to use and estimate the total cost.
* Use the cost estimators on the {{site.data.keyword.Bluemix_notm}} {{site.data.keyword.pricing_sheet}}
to see a rough estimation of the cost based on the size of your app.
* Use the cost calculator on the Pricing page to see accurate app prices based on your input of runtime and service usages.
* Calculate your cost manually.

## Using the Pricing Calculator
{: #pricing-calculator}

You can use the Pricing Calculator to estimate the cost of platform and many infrastructure resources before you make a purchase.

1. Access the [Pricing Calculator ![External link icon](../icons/launch-glyph.svg)](https://console.bluemix.net/pricing/){: new_window} in one of the following ways:
  * From the [Pricing page ![External link icon](../icons/launch-glyph.svg)](https://www.ibm.com/cloud/pricing){: new_window}, select **Explore our solutions** > **Pricing calculator** > **Try the calculator**.
  * If you are not currently logged into {{site.data.keyword.Bluemix_notm}}, from the [{{site.data.keyword.Bluemix_notm}} home page ![External link icon](../icons/launch-glyph.svg)](https://console.bluemix.net/){: new_window} click **Pricing**.
2. From the **Infrastructure** or **Platform** lists, select the category of the resource you want to price. The resources in the category you selected are shown, and you can also search the category for a specific resource.
3. Select a resource in the category to see a description of it. Some resources have multiple options. For example, if you selected **Compute** under **Infrastructure** and then selected **Bare metal servers**, you have a list of servers to choose from. You can sort the list, and the select the right option for you.
4. Select the quantity of the resource to add.
5. Click **Add to estimate**.
6. Continue adding resources from the **Infrastructure** and **Platform** categories until you have added what you want to estimate.

The **Estimate** panel shows you the resources you've added, the price for each one, and a total price. You can click **Clear calculation** to start over with a new estimate.

The Pricing Calculator provides the following functions:
  * Cost estimates that are currently provided in USD currency.
  * Estimates for infrastructure resources that are currently available for the **Compute** and **Containers** categories.
  * Cost estimates of resources that do not currently including discounts.
  * Estimates of costs that are provided for planning purposes; you cannot purchase resources directly from the Pricing Calculator.

If you are pricing only platform resources, to see an estimate in a currency other than USD, you can click **Switch to Classic Calculator**. The Classic Calculator does not include infrastructure resources.
{: tip}

## Using the Classic Calculator for platform resources
{: #calculator}

To calculate your platform resource costs in a currency other than USD, you can use the Classic Calculator. The Classic Calculator does not provide pricing estimates for infrastructure resources.

1. Go to the {{site.data.keyword.Bluemix_notm}} {{site.data.keyword.pricing_sheet}}.
2. Use one of the Infrastructure widgets, or click **Pricing calculator**.

To use the calculator, type your projected monthly usage of the listed resources; for example, number of instances or push notifications. Click inside the **Monthly Usage** field for hints about the units that are expected in the field. The calculator displays the price for your input immediately. You can also adjust the calculator to display yearly costs instead of monthly costs.

## Calculating your costs manually
{: #manual}

You might want to estimate your {{site.data.keyword.Bluemix_notm}} costs yourself, to better understand how {{site.data.keyword.Bluemix_notm}} costs are calculated. You can calculate the total price of using {{site.data.keyword.Bluemix_notm}} to build and host your app by considering the prices of the runtime and the services it uses. The prices of runtimes and services sometimes change, so you must refer to the latest information on the {{site.data.keyword.Bluemix_notm}} Pricing Sheet when you calculate the total price.

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

If you linked your {{site.data.keyword.Bluemix_notm}} and SoftLayer accounts, the single invoice you receive is in United States dollars (USD) only. See [Using IBMids and linking accounts](/docs/account/softlayerlink.html) for more information.
{: tip}
