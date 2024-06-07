---

copyright:
  years: 2021, 2023
lastupdated: "2021-09-17"

keywords: enterprise usage, view enterprise costs, account hierarchy, report organization, enterprise report organization

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Enterprise usage report organization
{: #enterprise-report}

An enterprise account's usage charges come from the use of the resource instances that are created in the account. The resource instances belong to different plans, and the usage for those instances are aggregated towards their respective plans. The charges for all of the plans in an account are calculated every month and are billed to the billing unit of the account.

Reports for any entity in the hierarchy that is not an account (the enterprise or an account group) has the usage of all the accounts under that entity rolled up to the billing unit.


## Example Hierarchy
{: #enterprise-hierarchy-example}

The following example depicts a hierarchy of an enterprise called `Cloud-Provider`. The `Cloud-Provider` enterprise contains an `Administration` account and the `Platform-Services` and `Solutions` account groups. Each account is assigned to one of the following billing units: `Administration`, `Operations`, or `Support`.

Only a single billing unit per enterprise is currently supported.
{: note}

```
(E)Cloud-Provider {ID: enterprise-cloud-provider}
├── (A)Administration {ID: account-administration, BU: Administration}
├── (AG)Platform-Services {ID: group-platform-services}
│   └── (A)Platform-Services-Operations {ID: platform-services-operations, BU: Operations}
└── (AG)Solutions {ID: group-solutions}
    ├── (AG)AI-Services {ID: group-ai-services}
    │   ├── (A)AI-Services-Operations {ID: account-ai-services-operations, BU: Operations}
    │   └── (A)AI-Services-Support {ID: account-ai-services-support, BU: Support}
    └── (AG)Data-Services  {ID: group-data-services}
        ├── (A)Data-Services-Operations {ID: account-data-services-operations, BU: Operations}
        └── (A)Data-Services-Support {ID: account-data-services-support, BU: Support}

ID -> Unique identifier of the entity
E  -> Enterprise entity
AG -> Account group entity
A  -> Account entity
BU -> Billing unit
```

Given this structure, the `Cloud-Provider` enterprise has the following effective billing units:

* The `Cloud-Provider` enterprise has three effective billing units: `Administration`, `Operations`, and `Support`.
* The `Platform-Services` account group has one effective billing unit: `Operations`.
* The `Solutions`, `AI-Services`, and `Data-Services` account groups have two effective billing units: `Operations` and `Support`.

### Example queries and responses

Enterprise `Cloud-Provider` reports

Query: `https://enterprise.{DomainName}/v1/resource-usage-reports?enterprise_id=enterprise-cloud-provider&month=2019-06`

This query returns three reports:

* Usage aggregated towards (E)Cloud-Provider:(BU)Administration
* Usage aggregated towards (E)Cloud-Provider:(BU)Operations
* Usage aggregated towards (E)Cloud-Provider:(BU)Support

Enterprise `Cloud-Provider` children reports

Query: `https://enterprise.{DomainName}/v1/resource-usage-reports?enterprise_id=enterprise-cloud-provider&month=2019-06&children=true`

This query returns four reports:

* Usage aggregated towards (A)Administration:(BU)Administration
* Usage aggregated towards (AG)Platform-Services:(BU)Operations
* Usage aggregated towards (AG)Solutions:(BU)Operations
* Usage aggregated towards (AG)Solutions:(BU)Support

Account group `Solutions` reports

Query: `https://enterprise.{DomainName}/v1/resource-usage-reports?account_group_id=group-solutions&month=2019-06`

This query returns two reports:

* Usage aggregated towards (AG)Solutions:(BU)Operations
* Usage aggregated towards (AG)Solutions:(BU)Support

Account group `Solutions` children reports

Query: `https://enterprise.{DomainName}/v1/resource-usage-reports?account_group_id=group-solutions&month=2019-06&children=true`

This query returns four reports:

* Usage aggregated towards (AG)AI-Services:(BU)Operations
* Usage aggregated towards (AG)AI-Services:(BU)Support
* Usage aggregated towards (AG)Data-Services:(BU)Operations
* Usage aggregated towards (AG)Data-Services:(BU)Support

Account group `Data-Services` reports

Query: `https://enterprise.{DomainName}/v1/resource-usage-reports?account_group_id=group-data-services&month=2019-06`

This query returns two reports:

* Usage aggregated towards (AG)Data-Services:(BU)Operations
* Usage aggregated towards (AG)Data-Services:(BU)Support

Account group `Data-Services` children reports

Query: `https://enterprise.{DomainName}/v1/resource-usage-reports?account_group_id=group-data-services&month=2019-06&children=true`

This query returns two reports:

* Usage aggregated towards (A)Data-Services-Operations:(BU)Operations
* Usage aggregated towards (A)Data-Services-Support:(BU)Support

Account `Data-Services-Operations` report

Query: `https://enterprise.{DomainName}/v1/resource-usage-reports?account_id=account-data-services-operations&month=2019-06`

This query returns one report: Usage aggregated towards (A)Data-Services-Operations:(BU)Operations
