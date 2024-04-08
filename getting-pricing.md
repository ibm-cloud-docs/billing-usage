---

copyright:
  years: 2024

lastupdated: "2024-04-02"

keywords: pricing

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Getting pricing by using the API
{: #getting-pricing}

As a seller, reseller, or a user that wants to pull pricing programmatically, you may want to get pricing dynamically so that you can quote true prices and do cost predictions on what a service or software is going to cost. To do this, you can leverage the API to get that dynamic pricing. To use the API, you need to have the correct [authentication](/apidocs/resource-catalog/global-catalog#authentication).
{: shortdesc}

You can use {{site.data.keyword.cloud-shell_full}} to enter commands. For more information, see [Working in Cloud Shell](/docs/cloud-shell?topic=cloud-shell-shell-ui).
{: tip}

In the following example, we're going to get the pricing for DNS Services.

1. To get pricing you first need to know the service's ID. To find that, you need to run a curl command to view all services, or you can run the a curl command with the service's programmatic name.

   If you don't know the programmatic name of the service, run the following command and search the results:

   ```
   curl --request GET \
   --url `https://globalcatalog.cloud.ibm.com/api/v1?q=kind:service` \
   --header `accept: application/json`
   ```
   {: codeblock}

   Or, since we already know the programmatic name for DNS Services, we can run the following:

   ```
   curl --request GET \
   --url `https://globalcatalog.cloud.ibm.com/api/v1?q=dns-svcs` \
   --header `accept: application/json`
   ```
   {: codeblock}

   In the response, locate the `_id` of the service. In this case, it is `b4ed8a30-936f-11e9-b289-1d079699cbe5`.

   You can also find the programmatic name or the service's ID by going to the [Global Catalog](https://globalcatalog.cloud.ibm.com/){: external}, click **Global Catalog Search**, search and select the service that you want, and then select the **Overview** tab.
   {: note}

2. After you have the service's ID, you can programmatically get pricing for a services by using the [Global Catalog API](/apidocs/resource-catalog/global-catalog#get-pricing) as shown in the following sample request.

   ```sh
   curl --request GET \
   --url 'https://globalcatalog.cloud.ibm.com/api/v1/b4ed8a30-936f-11e9-b289-1d079699cbe5' \
   --header 'accept: application/json'
   ```
   {: codeblock}
   {: curl}

   ```java
   GetPricingOptions getPricingOptions = new GetPricingOptions.Builder()
       .id("b4ed8a30-936f-11e9-b289-1d079699cbe5").build();

   Response<PricingGet> response = service.getPricing(getPricingOptions).execute();
   PricingGet pricingGet = response.getResult();

   System.out.println(pricingGet);
   ```
   {: codeblock}
   {: java}

   ```javascript
   const params = {
     id: "b4ed8a30-936f-11e9-b289-1d079699cbe5",
   };

   globalCatalogService.getPricing(params)
     .then(res => {
       console.log(JSON.stringify(res.result, null, 2));
     })
     .catch(err => {
       console.warn(err)
     });
   ```
   {: codeblock}
   {: javascript}

   ```python
   pricing_get = global_catalog_service.get_pricing(
     id="b4ed8a30-936f-11e9-b289-1d079699cbe5",
   ).get_result()

   print(json.dumps(pricing_get, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   getPricingOptions := globalCatalogService.NewGetPricingOptions(
     "b4ed8a30-936f-11e9-b289-1d079699cbe5",
   )

   pricingGet, response, err := globalCatalogService.GetPricing(getPricingOptions)
   if err != nil {
     panic(err)
   }
   b, _ := json.MarshalIndent(pricingGet, "", "  ")
   fmt.Println(string(b))
   ```
   {: codeblock}
   {: go}
