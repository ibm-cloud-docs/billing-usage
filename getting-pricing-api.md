---

copyright:
  years: 2024

lastupdated: "2024-10-04"

keywords: pricing, global catalog api

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Getting dynamic pricing
{: #getting-pricing-api}

As a seller, reseller, or a user that wants to pull pricing programmatically, you may want to get pricing dynamically so that you can quote true prices and do cost predictions on what a service or software is going to cost. To do this, you can leverage the Global Catalog API to get that dynamic pricing. To use the API, you need to have the correct [authentication](/apidocs/resource-catalog/global-catalog#authentication).
{: shortdesc}

## Identifying an offering and regional availability
{: #identify-offering-regional-availability}

With this example you'll see how to identify an offering and the regions that are available. To do this, you'll make an API call to the GC to list all offerings, filter results to identify the desired offering, and make an API call to get the regions where the offering is available. Note that you identify regions in which a specific plan is available and not if a service is available in all regions.

To list all offerings, use the following command:

```sh
curl --request GET
--url `https://globalcatalog.cloud.ibm.com/api/v1?q=kind:service`
--header `accept: application/json`
```
{: codeblock}
{: curl}

In the response, you can identify the service ID of Power Systems Virtual Server Group: `abd259f0-9990-11e8-acc8-b9f54a8f1661`.

So, you can run the following command to get the plan IDs for Power Systems Virtual Server Group.

```sh
curl -X 'GET'
--url 'https://globalcatalog.cloud.ibm.com/api/v1/abd259f0-9990-11e8-acc8-b9f54a8f1661/plan?_offset=0&_limit=50'
-H 'accept: application/json'
```
{: codeblock}
{: curl}

The following is an example response for the command that you just ran. The resources array lists all plans in the service. Each entry in the array is a plan. The important field in the plan object is the `id` field. In the following response, you'll see that `f165dd34-3a40-423b-9d95-e90a23f724dd` is the ID.

```
{
  "offset": 0,
  "limit": 50,
  "count": 2,
  "resource_count": 2,
  "first": "https://globalcatalog.cloud.ibm.com/api/v1/abd259f0-9990-11e8-acc8-b9f54a8f1661/plan?languages=en-US%2Cen%3Bq%3D0.9",
  "resources": [
    {
      "_id": "f165dd34-3a40-423b-9d95-e90a23f724dd",
      "_rev": "5-3709538cdcff35d2917d56c3cafb1fac",
      "active": true,
      "catalog_crn": "crn:v1:bluemix:public:globalcatalog::::plan:f165dd34-3a40-423b-9d95-e90a23f724dd",
      "children_url": "https://globalcatalog.cloud.ibm.com/api/v1/f165dd34-3a40-423b-9d95-e90a23f724dd/%2A",
      "complete": true,
      "created": "2019-06-14T22:52:18.378Z",
      "disabled": false,
      "geo_tags": [
        "che01",
        "dal10",
        "dal12",
        "eu-de-1",
        "eu-de-2",
        "lon04",
        "lon06",
        "mad02",
        "mad04",
        "mon01",
        "osa21",
        "sao01",
        "sao04",
        "syd04",
        "syd05",
        "tok04",
        "tor01",
        "wdc06",
        "wdc07",
        "us-east",
        "us-south"
      ],
      "id": "f165dd34-3a40-423b-9d95-e90a23f724dd",
      "images": {
        "feature_image": "https://cache.globalcatalog.cloud.ibm.com/api/v1/abd259f0-9990-11e8-acc8-b9f54a8f1661/artifacts/cache/66c89a2644c2ac54745d6ab9ecf4da8e-public/IBM_Power_CloudCatalog%202.svg",
        "image": "https://cache.globalcatalog.cloud.ibm.com/api/v1/abd259f0-9990-11e8-acc8-b9f54a8f1661/artifacts/cache/66c89a2644c2ac54745d6ab9ecf4da8e-public/IBM_Power_CloudCatalog%202.svg",
        "medium_image": "https://cache.globalcatalog.cloud.ibm.com/api/v1/abd259f0-9990-11e8-acc8-b9f54a8f1661/artifacts/cache/66c89a2644c2ac54745d6ab9ecf4da8e-public/IBM_Power_CloudCatalog%202.svg",
        "small_image": "https://cache.globalcatalog.cloud.ibm.com/api/v1/abd259f0-9990-11e8-acc8-b9f54a8f1661/artifacts/cache/66c89a2644c2ac54745d6ab9ecf4da8e-public/IBM_Power_CloudCatalog%202.svg"
      },
      "kind": "plan",
      "metadata": {
        "compliance": [
          "minisd"
        ],
        "original_name": "power-virtual-server-project",
        "other": {
          "pricing_schema_url": "https://power-iaas.cloud.ibm.com/cost-estimator"
        },
        "plan": {
          "allow_internal_users": true,
          "async_provisioning_supported": true,
          "async_unprovisioning_supported": true,
          "bindable": false,
          "reservable": false,
          "service_check_enabled": false,
          "single_scope_instance": "",
          "test_check_interval": 0
        },
        "pricing": {
          "metrics": null,
          "origin": "pricing_catalog",
          "starting_price": {},
          "type": "Paid",
          "url": "https://globalcatalog.cloud.ibm.com/api/v1/f165dd34-3a40-423b-9d95-e90a23f724dd/pricing"
        },
        "rc_compatible": true,
        "service": {
          "async_provisioning_supported": true,
          "async_unprovisioning_supported": true,
          "bindable": false,
          "custom_create_page_hybrid_enabled": false,
          "extension": null,
          "iam_compatible": true,
          "parameters": [],
          "plan_updateable": true,
          "rc_provisionable": true,
          "service_check_enabled": false,
          "service_key_supported": false,
          "state": "",
          "test_check_interval": 0,
          "type": "",
          "unique_api_key": false,
          "user_defined_service": null
        },
        "ui": {
          "strings": {
            "en": {
              "bullets": [
                {
                  "description": "Enables provisioning of Power Virtual Server LPARs in the chosen region."
                }
              ]
            }
          }
        }
      },
      "name": "power-virtual-server-group",
      "overview_ui": {
        "en": {
          "description": "A Power Systems Virtual Server group for the specified IBM Cloud region.",
          "display_name": "Power Systems Virtual Server Group",
          "long_description": "A Power Systems Virtual Server group for the specified IBM Cloud region."
        }
      },
      "parent_id": "abd259f0-9990-11e8-acc8-b9f54a8f1661",
      "parent_url": "https://globalcatalog.cloud.ibm.com/api/v1/abd259f0-9990-11e8-acc8-b9f54a8f1661",
      "pricing_tags": [
        "allow_internal_users",
        "paid",
        "paid_only"
      ],
      "provider": {
        "email": "pil@us.ibm.com",
        "name": "IBM"
      },
      "tags": [
        "apidocs_enabled",
        "beryllium",
        "freesia",
        "ibm_created",
        "rc_compatible"
      ],
      "updated": "2024-03-15T13:14:09.574263813-04:00",
      "url": "https://globalcatalog.cloud.ibm.com/api/v1/f165dd34-3a40-423b-9d95-e90a23f724dd?languages=en-US%2Cen%3Bq%3D0.9",
      "visibility": {
        "restrictions": "public"
      }
    },
    {
      "_id": "1112d6a9-71d6-4968-956b-eb3edbf0225b",
      "_rev": "22-c4780dfb7c2ca400029754649383507e",
      "active": true,
      "catalog_crn": "crn:v1:bluemix:public:globalcatalog::::plan:1112d6a9-71d6-4968-956b-eb3edbf0225b",
      "children_url": "https://globalcatalog.cloud.ibm.com/api/v1/1112d6a9-71d6-4968-956b-eb3edbf0225b/%2A",
      "complete": true,
      "created": "2024-02-14T11:00:24.476151306-05:00",
      "disabled": false,
      "geo_tags": [
        "satcon_dal",
        "satcon_fra",
        "satcon_mad",
        "satcon_osa",
        "satcon_sao",
        "satcon_syd",
        "satcon_tok",
        "satcon_tor",
        "satcon_wdc"
      ],
      "id": "1112d6a9-71d6-4968-956b-eb3edbf0225b",
      "images": {
        "feature_image": "https://cache.globalcatalog.cloud.ibm.com/api/v1/abd259f0-9990-11e8-acc8-b9f54a8f1661/artifacts/cache/66c89a2644c2ac54745d6ab9ecf4da8e-public/IBM_Power_CloudCatalog%202.svg",
        "image": "https://cache.globalcatalog.cloud.ibm.com/api/v1/abd259f0-9990-11e8-acc8-b9f54a8f1661/artifacts/cache/66c89a2644c2ac54745d6ab9ecf4da8e-public/IBM_Power_CloudCatalog%202.svg",
        "medium_image": "https://cache.globalcatalog.cloud.ibm.com/api/v1/abd259f0-9990-11e8-acc8-b9f54a8f1661/artifacts/cache/66c89a2644c2ac54745d6ab9ecf4da8e-public/IBM_Power_CloudCatalog%202.svg",
        "small_image": "https://cache.globalcatalog.cloud.ibm.com/api/v1/abd259f0-9990-11e8-acc8-b9f54a8f1661/artifacts/cache/66c89a2644c2ac54745d6ab9ecf4da8e-public/IBM_Power_CloudCatalog%202.svg"
      },
      "kind": "plan",
      "metadata": {
        "compliance": [
          "minisd"
        ],
        "original_name": "power-virtual-server-private-group",
        "plan": {
          "allow_internal_users": true,
          "async_provisioning_supported": false,
          "async_unprovisioning_supported": false,
          "bindable": false,
          "reservable": false,
          "service_check_enabled": false,
          "single_scope_instance": "",
          "test_check_interval": 0
        },
        "pricing": {
          "metrics": null,
          "origin": "pricing_catalog",
          "starting_price": {},
          "type": "free",
          "url": "https://globalcatalog.cloud.ibm.com/api/v1/1112d6a9-71d6-4968-956b-eb3edbf0225b/pricing"
        },
        "rc_compatible": true,
        "service": {
          "async_provisioning_supported": false,
          "async_unprovisioning_supported": false,
          "bindable": false,
          "custom_create_page_hybrid_enabled": false,
          "extension": null,
          "iam_compatible": true,
          "parameters": [],
          "plan_updateable": false,
          "rc_provisionable": true,
          "service_check_enabled": false,
          "service_key_supported": false,
          "state": "",
          "test_check_interval": 0,
          "type": "",
          "unique_api_key": false,
          "user_defined_service": null
        },
        "sla": {
          "dr": {
            "dr": true
          }
        },
        "ui": {
          "strings": {
            "en": {
              "bullets": [
                {
                  "description": "Enables use of Power Virtual Server Private Cloud resources in the chosen satellite location."
                }
              ]
            }
          }
        }
      },
      "name": "power-virtual-server-private-group",
      "overview_ui": {
        "en": {
          "description": "A Power Systems Virtual Server Private Cloud group for the specified IBM Cloud Satellite location.",
          "display_name": "Power Virtual Server Private Cloud Group",
          "long_description": "A Power Systems Virtual Server Private Cloud group for the specified IBM Cloud Satellite location."
        }
      },
      "parent_id": "abd259f0-9990-11e8-acc8-b9f54a8f1661",
      "parent_url": "https://globalcatalog.cloud.ibm.com/api/v1/abd259f0-9990-11e8-acc8-b9f54a8f1661",
      "pricing_tags": [
        "free",
        "allow_internal_users"
      ],
      "provider": {
        "email": "pil@us.ibm.com",
        "name": "IBM"
      },
      "tags": [
        "rc_compatible",
        "apidocs_enabled",
        "compute",
        "virtualservers",
        "ibm_created",
        "satellite_enabled"
      ],
      "updated": "2024-06-20T10:12:47.969618989-04:00",
      "url": "https://globalcatalog.cloud.ibm.com/api/v1/1112d6a9-71d6-4968-956b-eb3edbf0225b?languages=en-US%2Cen%3Bq%3D0.9",
      "visibility": {
        "restrictions": "public"
      }
    }
  ]
}
```
{: codeblock}

## Determining valid plans for a given region
{: #valid-plans-region}

In the following example, you'll see how to find valid plans for a specific region. to do this you'll make an API call to retrieve the list of valid plans for an offering in a specified region and then interpret the API response to understand the available plans. For more information, see the API documentation: [Get the pricing deployments for a plan](/apidocs/resource-catalog/global-catalog#get-pricing-deployments).

```sh
curl --request GET
--url 'https://globalcatalog.cloud.ibm.com/api/v1/{id}/pricing/deployment'
--header 'accept: application/json'
```
{: codeblock}
{: curl}

In that example, enter the plan ID that you found using the previous step in the place of `ID`.

```sh
curl --request GET
--url 'https://globalcatalog.cloud.ibm.com/api/v1/f165dd34-3a40-423b-9d95-e90a23f724dd/pricing/deployment'
--header 'accept: application/json'
```
{: codeblock}
{: curl}

The following is an example response that only lists the first metric:

```
{
  "offset": 0,
  "limit": 50,
  "count": 2,
  "resource_count": 2,
  "resources": [
    {
      "deployment_id": "1e4e33e4-cfa6-4f12-9016-be594a6d5f87:global",
      "deployment_location": "global",
      "deployment_region": "global",
      "origin": "pricing_catalog",
      "type": "paygo",
      "url": "https://globalcatalog.cloud.ibm.com/api/v1/1e4e33e4-cfa6-4f12-9016-be594a6d5f87:global/pricing",
      "i18n": {},
      "starting_price": {},
      "effective_from": "2024-07-01T00:00:00Z",
      "effective_until": "9999-12-31T00:00:00Z",
      "metrics": [
        {
          "part_ref": "",
          "metric_id": "COSARCVRSTR",
          "tier_model": "Simple Tier",
          "resource_display_name": "Archive restore",
          "charge_unit_display_name": "GIGABYTE",
          "charge_unit_name": "ARCHIVE_RESTORE",
          "charge_unit": "GIGABYTE",
          "charge_unit_quantity": 1,
          "amounts": [
            {
              "country": "USA",
              "currency": "USD",
              "prices": [
                {
                  "quantity_tier": 999999999,
                  "price": 0.02299
                }
              ]
            }
          ],
          "usage_cap_qty": 0,
          "display_cap": 0,
          "effective_from": "2024-07-01T00:00:00Z",
          "effective_until": "9999-12-31T00:00:00Z"
        }
      ]
    }
  ]
}
```
{: codeblock}

The resources object in the response is a list of deployments or locations where the plan is available. In this case, the plan is available globally. There are other situations the deployment is specific to a region such as `us-south`, `us-east`, etc.

For the case where the plan deployment is global, the pricing for a specific region can be queried by using the following API:

```sh
curl --request GET
--url 'https://globalcatalog.cloud.ibm.com/api/v1/{id}:global/pricing?deployment_region={ region_id}'
--header 'accept: application/json'
```
{: codeblock}
{: curl}

Use the plan ID that you found in the previous step:

```sh
curl --request GET
--url 'https://globalcatalog.cloud.ibm.com/api/v1/f165dd34-3a40-423b-9d95-e90a23f724dd:global/pricing?deployment_region={ region_id}'
--header 'accept: application/json'
```
{: codeblock}
{: curl}

An example of a plan that is deployed globally and has region specific pricing is the Cloud Object Storage Standard Plan. The plan Id is `744bfc56-d12c-4866-88d5-dac9139e0e5d`. This plan has specific region for `eu-de`. This `region_id` and must match with one of the values of `deployment_region` in the `deployment_locations` array in the previous response.

There's also global plans with global pricing that don't use the `deployment_regions` override variable.
{: note}

The following is an example using the API endpoint with `eu-de` `deployment_region`.

`https://globalcatalog.cloud.ibm.com/api/v1/744bfc56-d12c-4866-88d5-dac9139e0e5d:global/pricing?deployment_region=eu-de`

This is the example response:

```
{
  "deployment_id": "744bfc56-d12c-4866-88d5-dac9139e0e5d:global",
  "deployment_location": "global",
  "deployment_region": "eu-de",
  "origin": "pricing_catalog",
  "type": "paygo",
  "url": "https://globalcatalog.test.cloud.ibm.com/api/v1/744bfc56-d12c-4866-88d5-dac9139e0e5d:global/pricing?deployment_region=eu-de",
  "i18n": {},
  "starting_price": {},
  "effective_from": "2024-09-01T00:00:00Z",
  "effective_until": "9999-12-31T00:00:00Z",
  "metrics": [
    {
      "part_ref": "",
      "metric_id": "COSVLTBCALL",
      "tier_model": "Granular Tier",
      "resource_display_name": "Vault Class B calls",
      "charge_unit_display_name": "API_CALLS",
      "charge_unit_name": "VAULT_CLASS_B_CALLS",
      "charge_unit": "API_CALLS",
      "charge_unit_quantity": 10000,
      "amounts": [
        {
          "country": "USA",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 1,
              "price": 0.01045
            }
          ]
        }
      ],
      "usage_cap_qty": 0,
      "display_cap": 0,
      "effective_from": "2024-09-01T00:00:00Z",
      "effective_until": "9999-12-31T00:00:00Z",
      "additional_properties": {}
    }
  ]
}
```
{: codeblock}

For the case where the plan deployment is not global, the pricing for a specific deployment location can be queried using the following API:

```sh
curl --request GET
--url 'https://globalcatalog.cloud.ibm.com/api/v1/{id}/pricing'
--header 'accept: application/json'
```
{: codeblock}
{: curl}

Use the plan ID from the previous step:

```sh
curl --request GET
--url 'https://globalcatalog.cloud.ibm.com/api/v1/f165dd34-3a40-423b-9d95-e90a23f724dd/pricing'
--header 'accept: application/json'
```
{: codeblock}
{: curl}

The `{id}` is the ID of the `deployment_id` of the deployment. You can locate the deployment location and the associated `deployment_id` by using the previously discussed API.

Let’s illustrate this scenario by using plan ID: `databases-for-postgresql-standard`. A plan in the Service Databases for PostgreSQL, service id: `databases-for-postgresql`.

One of the deployment locations of this plan is available in `au-syd` and the `deployment_id` for this location is `databases-for-postgresql-standard:au-syd`.

The API call would be this: `https://globalcatalog.cloud.ibm.com/api/v1/databases-for-postgresql-standard:au-syd`.

The following is a response for the API call:

```
{
  "deployment_id": "databases-for-postgresql-standard:au-syd",
  "deployment_location": "au-syd",
  "deployment_region": "au-syd",
  "origin": "pricing_catalog",
  "type": "paygo",
  "url": "https://globalcatalog.cloud.ibm.com/api/v1/databases-for-postgresql-standard:au-syd/pricing",
  "i18n": {},
  "starting_price": {},
  "effective_from": "2024-09-01T00:00:00Z",
  "effective_until": "9999-12-31T00:00:00Z",
  "metrics": [
    {
      "part_ref": "",
      "metric_id": "databases-for-postgresql-cpu",
      "tier_model": "Linear Tier",
      "resource_display_name": "Databases for PostgreSQL CPU",
      "charge_unit_display_name": "CPU",
      "charge_unit_name": "VIRTUAL_PROCESSOR_CORES",
      "charge_unit": "Virtual Processor Core-Hour",
      "charge_unit_quantity": 1,
      "amounts": [
        {
          "country": "USA",
          "currency": "USD",
          "prices": [
            {
              "quantity_tier": 1,
              "price": 32.342
            }
          ]
        }
      ],
      "usage_cap_qty": 0,
      "display_cap": 0,
      "effective_from": "2024-09-01T00:00:00Z",
      "effective_until": "9999-12-31T00:00:00Z"
    }
  ]
}
```
{: codeblock}

## Identifying valid metrics for a given plan or region
{: #valid-metrics}

The following information is to help you identify valid metrics for a specific plan and region. Metrics are specifications of resources or operations that determine usage for pricing. You make an API call to list valid metrics for a given plan in a specified region and then parse trhough the response to get details about the metrics.

The following example shows an API call for the Power Systems Virtual Server Group service. As we found before, the ID is `f165dd34-3a40-423b-9d95-e90a23f724dd`.

```sh
curl --request GET
--url 'https://globalcatalog.cloud.ibm.com/api/v1/f165dd34-3a40-423b-9d95-e90a23f724dd/pricing/deployment'
--header 'accept: application/json'
```
{: codeblock}
{: curl}

The following is the example response:

```
{
  "offset": 0,
  "limit": 1,
  "count": 21,
  "resource_count": 1,
  "resources": [
    {
      "deployment_id": "f165dd34-3a40-423b-9d95-e90a23f724dd:che0142579",
      "deployment_location": "che01",
      "deployment_region": "che01",
      "origin": "pricing_catalog",
      "type": "Paid",
      "i18n": {},
      "starting_price": {},
      "effective_from": "2024-07-01T00:00:00Z",
      "effective_until": "9999-09-30T00:00:00Z",
      "metrics": [
        {
          "part_ref": "",
          "metric_id": "tier3-storage",
          "tier_model": "Linear Tier",
          "resource_display_name": "HDD Storage Gigabyte-Hours",
          "charge_unit_display_name": "HDD Storage Gigabyte-Hour",
          "charge_unit_name": "TIER_THREE_STORAGE_GIGABYTE_HOURS",
          "charge_unit": "HDD Storage Gigabyte-Hour",
          "charge_unit_quantity": 1,
          "amounts": [
            {
              "country": "USA",
              "currency": "USD",
              "prices": [
                {
                  "quantity_tier": 1,
                  "price": 0.000171798
                }
              ]
            }
          ],
          "usage_cap_qty": 0,
          "display_cap": 0,
          "effective_from": "2024-07-01T00:00:00Z",
          "effective_until": "9999-12-31T00:00:00Z"
        }
      ]
    }
  ]
}
```

Inspect the resources array for deployments. Each deployment has the `deployment_location` field which refers to a specific location or region where a plan is available.

The following table shows the response body fields and their descriptions. For more information, see the [Global Catalog API documentation](/apidocs/resource-catalog/global-catalog).

| JSON field                 | Description |
|----------------------------|-------------|
| `deployment_id`            | The deployment object ID this pricing is from. |
| `deployment_location`      | The deployment location this pricing is from. Such as `che01`. |
| `deployment_region`        | This is the region where the deployment plan is to retrieve plan pricing for a global deployment. For this example it is `che01`.  |
| `origin`                   | Where the pricing data comes from. For this example, it's `pricing_catalog` and is designated by the Pricing Source in the Global Catalog UI. |
| `type`                     | Type of plan. Valid values are `free`, `trial`, `paygo`, `paid`, `bluemix-subscription`, and `ibm-subscription`. For more information, see [Account types](/docs/account?topic=account-accounts). |
| `url`                      | The url for the artifact. This is the url that you can use to get pricing. |
| `starting_price`           | Plan-specific starting price information. |
| `effective_from`           | The start date for the available pricing. |
| `effective_until`          | The end date for the available pricing. |
| `metrics`                  | Specifications of resources or operations that determine usage for pricing. |
| `part_ref`                 | The IBM assigned part reference number for the metric. |
| `metric_id`                | The metric ID or part number. |
| `tier_model`               | The tier pricing model [^tabletext]. Possible values are `Simple Tier`, `Graduated Tier`, `Linear Tier`, or `Block (Step) Tier`. For this example it's `Linear Tier`. For more information, see [How you're charged](/docs/billing-usage?topic=billing-usage-charges#charges-services). |
| `resource_display_name`    | Display name of the resource. This is how the metric appears in the catalog. |
| `charge_unit_display_name` | Display name of the charge unit. Unit friendly display name for the `charge_unit`. |
| `charge_unit_name`         | An assigned name for the charge unit. This is the ID that is used to measure usages for the metric. |
| `charge_unit`              | This is the chargable unit. For this example, it's `HDD Storage Gigabyte-Hour`. |
| `charge_unit_quantity`     | The chargable unit quantity. In the example response, the charge unit is 1, which means you are charged for each gigabyte used. |
| `amounts`                  | The pricing per metric by country and currency. |
| `country`                  | Country for which this object's price is applicable. |
| `currency`                 | Currency for the prices. |
| `quantity_tier`            | Level of usage for that price in that tier. |
| `price`                    | Price per unit for this tier. |
{: caption="Table 1. Example response JSON fields" caption-side="bottom"}

[^tabletext]: For tiered pricing, you pay based on your runtime and service consumption. However, tiered charges add more pricing levels, often offering discounted rates on products for higher consumption tiers. Tiered pricing is offered in simple, graduated, linear, or block.

### Interpreting pricing API results
{: #graduated_tier}

In the following table, we're showing an example of what the linear tier pricing could be. For linear tier, the total amount is the result of multiplication of the unit price per resource and usage quantity.

The following table illustrates how much you pay with a plan that is based on a graduated tier pricing model:

|Quantity of Items | Charge Calculation          | Total Price |
|------------------|-----------------------------|-------------|
| 500              | 500 × 0.000171798  = .0859  | $.0859 USD  |
| 2000             | 2000 x 0.000171798 = .344   | $.344 USD   |
| 10000            | 10000 x 0.000171798 = 1.72  | $1.72 USD   |
{: caption="Table 2. Charge calculation by using the graduated tier pricing model" caption-side="top"}
