---

copyright:
  years: 2024

lastupdated: "2024-09-18"

keywords: pricing, global catalog api

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Getting dynamic pricing
{: #getting-pricing-api}

As a seller, reseller, or a user that wants to pull pricing programmatically, you may want to get pricing dynamically so that you can quote true prices and do cost predictions on what a service or software is going to cost. To do this, you can leverage the Global Catalog API to get that dynamic pricing. To use the API, you need to have the correct [authentication](/apidocs/resource-catalog/global-catalog#authentication).
{: shortdesc}

This document is only valid for offerings that have the `deployment_regions` field. Further updates are going to be made to account for all services.
{: important}

## Getting pricing
{: #getting-pricing}

You can use the [Global Catalog API](/apidocs/resource-catalog/global-catalog#intro) to find regional pricing for a service but you need to know the object's ID. For each object of the service, there is a different ID. The best way to find the ID is to use the Global Catalog UI. As an example, with the following steps, we'll find the deployment plan ID for Cloud Object Storage.

To get pricing by using the API, the `Kind` of the object needs to be `Deployment`.
{: note}

1. Go to the [Global Catalog](https://globalcatalog.cloud.ibm.com/){: external} and click **Global Catalog Search**.
1. Search for `Cloud Object Storage` and select **Object Storage** from the results. The service we want will have the display name `Object Storage` and the name `object-storage-group`.
1. From the navigation menu, select **Cloud Object Storage** > **Standard** > **Premium Global Deployment**.
1. Select the **Overview** tab to view the deployment ID. For Cloud Object storage, it is `744bfc56-d12c-4866-88d5-dac9139e0e5d:global`.

Now that you know the ID for the object, you can use the following steps to get pricing.

You can use {{site.data.keyword.cloud-shell_full}} to enter commands. For more information, see [Working in Cloud Shell](/docs/cloud-shell?topic=cloud-shell-shell-ui).
{: tip}

1. Run the following command to call the Global Catalog pricing API for the global deployment plan ID.

   ```sh
   curl --request GET
   --url 'https://globalcatalog.cloud.ibm.com/api/v1/744bfc56-d12c-4866-88d5-dac9139e0e5d:global/pricing'
   --header 'accept: application/json'
   ```
   {: codeblock}
   {: curl}

   The response includes the list of pricing deployment regions. Look for `deployment_regions` in the response. For Cloud Object Storage, you'll find that the available regions are `us-south`, `us-east`, and `eu-de`.
1. Call the pricing API again, but this time add the query parameter `deployment_regions` and specify one of the regions that is contained within the list. For this example, we'll use `us-south`.

   ```sh
   curl --request GET
   --url 'https://globalcatalog.cloud.ibm.com/api/v1/744bfc56-d12c-4866-88d5-dac9139e0e5d:global/pricing?deployment_region=us-south'
   --header 'accept: application/json'
   ```
   {: codeblock}
   {: curl}

1. Repeat step three as needed to get pricing for all regions.


### Example response
{: #example-response}

The following is an example response for the curl command from the previous steps. For more information, see [Understanding JSON fields](#understanding-json-fields).

```
{
  "deployment_id": "744bfc56-d12c-4866-88d5-dac9139e0e5d:global",
  "deployment_location": "global",
  "deployment_region": "us-south",
  "origin": "pricing_catalog",
  "type": "paygo",
  "url": "https://globalcatalog.test.cloud.ibm.com/api/v1/744bfc56-d12c-4866-88d5-dac9139e0e5d:global/pricing?deployment_region=us-south",
  "i18n": {},
  "starting_price": {},
  "effective_from": "2024-09-01T00:00:00Z",
  "effective_until": "9999-12-31T00:00:00Z",
  "metrics": [
    {
      "part_ref": "",
      "metric_id": "COSSTDBAND",
      "tier_model": "Graduated Tier",
      "resource_display_name": "Standard bandwidth",
      "charge_unit_display_name": "GIGABYTE",
      "charge_unit_name": "STANDARD_BANDWIDTH",
      "charge_unit": "GIGABYTE",
      "charge_unit_quantity": 1,
      "amounts": [
        {
          "country": "USA",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 50000,
              "price": 0.09
            },
            {
              "quantity_tier": 150000,
              "price": 0.07
            },
            {
              "quantity_tier": 999999999,
              "price": 0.05
            }
          ]
        },
```
{: codeblock}

#### Understanding JSON fields
{: #understanding-json-fields}

The following table shows the response body fields and their descriptions. For more information, see the [Global Catalog API documentation](/apidocs/resource-catalog/global-catalog).

| JSON field                 | Description |
|----------------------------|-------------|
| `deployment_id`            | The deployment object ID this pricing is from. |
| `deployment_location`      | The deployment location this pricing is from. Such as `global`. |
| `deployment_region`        | This is the region where the deployment plan is to retrieve plan pricing for a global deployment. For this example it is `us-south`.  |
| `origin`                   | Where the pricing data comes from. For this example, it's `pricing_catalog` and is designated by the Pricing Source in the Global Catalog UI. |
| `type`                     | Type of plan. Valid values are `free`, `trial`, `paygo`, `bluemix-subscription`, and `ibm-subscription`. For more information, see [Account types](/docs/account?topic=account-accounts). |
| `url`                      | The url for the artifact. This is the url that you can use to get pricing. |
| `starting_price`           | Plan-specific starting price information. |
| `effective_from`           | The start date for the available pricing. |
| `effective_until`          | The end date for the available pricing. |
| `metrics`                  | Specifications of resources or operations that determine usage for pricing. |
| `part_ref`                 | The IBM assigned part reference number for the metric. |
| `metric_id`                | The metric ID or part number. |
| `tier_model`               | The tier pricing model [^tabletext]. For this example it's `Graduated Tier`. In the graduated tier model, the unit price per tier decreases as your level of usage increases. For more information, see [How you're charged](/docs/billing-usage?topic=billing-usage-charges#charges-services). |
| `resource_display_name`    | Display name of the resource. This is how the metric appears in the catalog. |
| `charge_unit_display_name` | Display name of the charge unit. Unit friendly display name for the `charge_unit`. |
| `charge_unit_name`         | An assigned name for the charge unit. This is the ID that is used to measure usages for the metric. |
| `charge_unit`              | This is the chargable unit. For this example, it's `GIGABYTE`. |
| `charge_unit_quantity`     | The chargable unit quantity. In the example response, the charge unit is 1, which means you are charged for each gigabyte used. |
| `amounts`                  | The pricing per metric by country and currency. |
| `country`                  | Country for which this object's price is applicable. |
| `currency`                 | Currency for the prices. |
| `quantity_tier`            | Level of usage for that price in that tier. |
| `price`                    | Price per unit for this tier. Since the `charge_unit_quantity` is `1`, and the `charge_unit` is `GIGABYTE`, you are charged for each gigabyte. Also, since this is graduated tier pricing model, you're charged .09 USD for each gigabyte up to 50,000, and .07 USD for units between 50,000 and 150,000. |
{: caption="Table 1. Example response JSON fields" caption-side="bottom"}

[^tabletext]: For tiered pricing, you pay based on your runtime and service consumption. However, tiered charges add more pricing levels, often offering discounted rates on products for higher consumption tiers. Tiered pricing is offered in simple, graduated, or block.

### Graduated tier pricing example
{: #graduated_tier}

In the following tables, we're showing an example of what the graduated tier pricing could be. In the graduated tier model, the unit price per tier decreases as your level of usage increases. The total price is the cumulative charges for each level of usage, consisting of your quantity multiplied by the unit price at that tier, for example:

| Quantity of Items          |	Unit Price for Items in the Tier |
|----------------------------|-----------------------------------|
| Tier 1: 1 - 50000          |	$0.09 USD                        |
| Tier 2: 50000 - 150000     |	$0.07 USD                        |
| Tier 3: 150000 or more     |	$0.05 USD                        |
{: caption="Table 2. Graduated tier pricing table" caption-side="top"}

The following table illustrates how much you pay with a plan that is based on a graduated tier pricing model:

|Quantity of Items | Charge Calculation                                                               | Total Price |
|------------------|----------------------------------------------------------------------------------|-------------|
| 2500             | 2500 × .09 (unit price for Tier 1) = 225                                            |	$225 USD    |
| 125000           | (50000 × .09 (unit price for Tier 1)) + (75000 × .07 (unit price for Tier 2)) = 9750 |	$9750 USD   |
| 250000           | (50000 × .09 (unit price for Tier 1)) + (100000 × .07 (unit price for Tier 2)) + (100000 × .05 (unit price for Tier 3)) = 16500 | $16500 USD |
{: caption="Table 3. Charge calculation by using the graduated tier pricing model" caption-side="top"}
