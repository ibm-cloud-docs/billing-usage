---

copyright:
  years: 2015, 2024
lastupdated: "2024-08-14"

keywords: estimate cost, cost example, billing example, payment example, calculating app price

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Scenario: Estimating costs of a {{site.data.keyword.codeengineshort}} App with a {{site.data.keyword.cloudant_short_notm}} Database and Observability Tools
{: #sample}

Assume that you deployed your web application on to {{site.data.keyword.codeenginefull}} that uses several services that are provided by {{site.data.keyword.Bluemix}} including a database, logging and monitoring. You can learn how the actual cost of your app is calculated in this example.
{: shortdesc}

With {{site.data.keyword.codeenginefull}} you pay for only memory and CPU needed to run your application, as well as any incoming HTTP calls. This includes [scaling to 0](/docs/codeengine?topic=codeengine-app-scale#app-scale-boundaries) if your application doesn't receive any traffic for a period of time. However, for this example let's assume a production application which is always running and the app has the following specifications:

* The application is configured with 1 vCPU and 4 GB of memory (default for apps and jobs).
* The application receives 5 million HTTP requests in 30 days.
* The application uses a {{site.data.keyword.cloudant_short_notm}} Standard plan with:
  * 150 GB of data storage (130 GB over the free 20 GB)
  * 1,000 lookups per second
  * 500 writes per second
  * 50 queries per second
* The application uses {{site.data.keyword.logs_full_notm}} Standard plan for log storage and search.
  * The application needs 7 days of fast search
  * logs are retained in for 3 months in {{site.data.keyword.cloud_notm}}
* The application uses {{site.data.keyword.mon_full_notm}} for performance metrics.
  * Only platform-metrics from {{site.data.keyword.codeengineshort}} and {{site.data.keyword.cloudant_short_notm}} are needed

{{site.data.keyword.codeengineshort}} includes a free tier, and {{site.data.keyword.cloudant_short_notm}} Standard plan includes 20GB of free storage so you can experiment before you commit.

The prices used in this example are in US currency and they may not reflect current prices or include any discounts or promo codes. For the most up-to-date prices, see [{{site.data.keyword.codeengineshort}} pricing](/codeengine/overview#pricing), [{{site.data.keyword.cloudant_short_notm}} pricing](/docs/Cloudant?topic=Cloudant-pricing), [{{site.data.keyword.logs_full_notm}} pricing](/docs/cloud-logs?topic=cloud-logs-service_plans), and [{{site.data.keyword.mon_full_notm}} pricing](/docs/monitoring?topic=monitoring-pricing_plans).
{: important}

## Pricing scenario
{: #pricing-scenario}

The following table provides an example of estimated pricing for running an application in {{site.data.keyword.codeengineshort}} that uses {{site.data.keyword.cloudant_short_notm}} Standard plan as a data store, along with {{site.data.keyword.logs_full_notm}} and {{site.data.keyword.mon_full_notm}}. {{site.data.keyword.cloud_notm}} is also required to query log data older than 7 days. The scenario assumes the following usage pattern:


| Description | Quantity | Rate | Cost |
|----------------------------------|----------|-------------------|------|
| {{site.data.keyword.codeengineshort}} - vCPU seconds | 2,492,000 | $0.00003431 | $85.50 |
| {{site.data.keyword.codeengineshort}} - GB seconds | 10,168,000 | $0.00000356 | $36.20 |
| {{site.data.keyword.codeengineshort}} - Requests | 4,900,000 | $0.538 per million | $2.64 |
|  |  | **SubTotal** | **$124.34** |
|  |  |  |  |
| {{site.data.keyword.cloudant_short_notm}} - GB | 130 | $1.00 per GB | $130.00 |
| {{site.data.keyword.cloudant_short_notm}} - Lookups/second | 10 | $0.25 per 100 Lookups/second | $2.50 |
| {{site.data.keyword.cloudant_short_notm}} - Writes/second | 10 | $0.50 per 50 Write/second | $5.00 |
| {{site.data.keyword.cloudant_short_notm}} - Queries/second | 10 | $5.00 per 5 Query/second | $50.00 |
|  |  | **SubTotal** | **$187.50** |
|  |  |  |  |
| {{site.data.keyword.logs_full_notm}} - 7 days | 5 GB | $1.20 per GB | $6.00 |
|  |  | **SubTotal** | **$6.00** |
|  |  |  |  |
| {{site.data.keyword.mon_full_notm}} - Time-series Metrics | 110 | $0.08 per metric | $8.80 |
|  |  | **SubTotal** | **$8.80** |
|  |  |  |  |
| {{site.data.keyword.cloud_notm}} - Storage capacity | 15 GB | $0.0230 per GB/month | $0.36 |
| {{site.data.keyword.cloud_notm}} - Public outbound bandwidth | 15 GB | $0.0000 per GB (within allowance) | $0.00 |
| {{site.data.keyword.cloud_notm}} - Class A requests | 15,000 | $0.0000 per 1,000 (within allowance) | $0.00 |
| {{site.data.keyword.cloud_notm}} - Class B requests | 150,000 | $0.0000 per 10,000 (within allowance) | $0.00 |
|  |  | **SubTotal** | **$0.36** |
|  |  |  |  |
|  |  | **Total** | **$327.00** |
{: caption="Table 1. Estimated costs for a {{site.data.keyword.codeengineshort}} application with {{site.data.keyword.cloudant_short_notm}} Standard plan, {{site.data.keyword.logs_full_notm}}, and {{site.data.keyword.mon_full_notm}}" caption-side="bottom"}

## Calculation details
{: #calculation-details}

## {{site.data.keyword.codeengineshort}} Calculation details
{: #codeengine-cost-details}

The following calculations include the{{site.data.keyword.codeengineshort}} free tier allocations which includes:
{: #code-engine-free-tier}

* 100,000 vCPU seconds per month
* 200,000 GB seconds of memory per month
* 100,000 HTTP requests per month

**vCPU:**

```
1 vCPU * 24 hours * 30 days * 3600 seconds = 2,592,000 vCPU seconds
Free tier: 100,000 vCPU seconds
Billable: 2,592,000 - 100,000 = 2,492,000 vCPU seconds
2,492,000 * $0.00003431 = $85.50
```

**Memory:**

```
4 GB * 24 hours * 30 days * 3600 seconds = 10,368,000 GB seconds
Free tier: 200,000 GB seconds
Billable: 10,368,000 - 200,000 = 10,168,000 GB seconds
10,168,000 * $0.00000356 = $36.20
```

**HTTP Requests:**

```
5,000,000 requests total
Free tier: 100,000 requests
Billable: 5,000,000 - 100,000 = 4,900,000 requests
4,900,000 * ($0.538 / 1,000,000) = $2.64
```

## {{site.data.keyword.cloudant_short_notm}} Calculation details
{: #cloudant-cost-details}

In our scenario, we're using 150 GB of storage but with 20 GB of free data storage, we pay for the extra 130 GB. The lookups, writes, and queries are charged based on the provisioned capacity in their respective increments.
For more detailed information about {{site.data.keyword.cloudant_short_notm}} pricing, see {{site.data.keyword.cloudant_short_notm}} Pricing.
{: #cloudant-pricing-details}

**Standard plan - Data:**

```
150 GB total, 20 GB free, 130 GB charged
130 GB * $1.00 per GB = $130.00
```

**Standard plan - Lookups:**

```
1,000 Lookups/second / 100 Lookups/second = 10 units
10 * $0.25 per 100 Lookups/second = $2.50
```

**Standard plan - Writes:**

```
500 Writes/second / 50 Writes/second = 10 units
10 * $0.50 per 50 Writes/second = $5.00
```

**Standard plan - Queries:**

```
50 Queries/second / 5 Queries/second = 10 units
10 * $5.00 per 5 Queries/second = $50.00
```

## {{site.data.keyword.logs_full_notm}} Calculation details
{: #cloud-logs-cost-details}

{{site.data.keyword.logs_full_notm}} supports [tiering of your log data](/docs/cloud-logs?topic=cloud-logs-tco-optimizer) to help optimize your logging costs while still being able to search and analyze applications log data. In this scenario, log data will be stored in the initial default of 7-day retention in Priority Insights. After 7-days the log data will still be queryable from {{site.data.keyword.cloud_notm}} at the {{site.data.keyword.cloud_notm}} rates. It is assumed that logs are retained for 3 months in {{site.data.keyword.cloud_notm}}.

Estimated Monthly log volume: 1 KB per request * 5,000,000 requests/month * 1 months = 5 GB

**Standard plan - Priority insights - 7 days:**

```
5 GB * $1.20 per GB = $6.00
```

## {{site.data.keyword.cloud_notm}} Calculation details


**Standard plan (us-south):**

3 months of logs: 1 KB per request * 5,000,000 requests/month * 3 months = 15 GB

Storage capacity:
15 GB * $0.0230 per GB/month = $0.36

Public outbound bandwidth:
Allowance: 100% of storage in GB = 15 GB
Actual usage: 15 GB
15 GB ≤ 15 GB allowance, so no additional charge

**Class A requests (write operations):**

Allowance: 100 x storage in GB = 100 x 15 = 1500 requests
Actual usage: Assuming file writes every 10 min there would be 43800 minutes/month / 10 minutes = 4380
4,380 > 1500 allowance, but charge applies per 1,000 requests
Billable requests: 4,380 - 1,500 = 2880
2880 * ($0.0052 / 1,000) = $0.014976 (rounded to $0.01 due to small amount)

**Class B requests (read operations):**

Allowance: 1000 x storage in GB = 1000 x 15 = 15,000 requests
Actual usage: Let's assume, we read 3 files for every file written in a month, 4,380 * 3 = 13140
13,140 < 15,000 allowance, but charge applies per 10,000 requests
Billable requests: Below allowance so there is no charge

Total {{site.data.keyword.cos_full_notm}} cost: $0.36 + $0.00 + $0.01 + $0.00 = $0.37

## {{site.data.keyword.mon_full_notm}} Calculation details
{: #cloud-monitoring-pricing-details}

Monitoring of {{site.data.keyword.codeengineshort}} and {{site.data.keyword.cloudant_short_notm}} is enabled using platform metrics. Platform metrics {{site.data.keyword.mon_full_notm}} are charged using the tiered pricing based on the number of time-series hours metrics.
There can view more [monitoring billing examples](/docs/monitoring?topic=monitoring-pricing_plans#billing_example) in the 
See  /docs/monitoring?topic=monitoring-pricing_plans#pricing_example3
For platform metrics {{site.data.keyword.mon_full_notm}} charges based on the number of time-series metrics:

```
time-series metrics: $0.08 USD per metric
```
In our scenario, we're assuming that there are 110 time-series metrics (50 for {{site.data.keyword.codeengineshort}} and 60 for {{site.data.keyword.cloudant_short_notm}}).

**Time-series Metrics:**

[{{site.data.keyword.codeengineshort}}](/docs/codeengine?topic=codeengine-monitor#metrics-by-plan) and [{{site.data.keyword.cloudant_short_notm}}](https://cloud.ibm.com/docs/Cloudant?topic=Cloudant-monitor-ibm-cloud-pm#metrics_dictionary-pm) provides a variety of platform metrics to monitor your applications. The number of [time-series depends on the cardinality](https://docs.sysdig.com/en/docs/sysdig-monitor/using-monitor/metrics/using-labels/#cardinality){: external}, or number of unique time series associated with a given metric. In our scenario we are assuming 60 time-series for code engine and 50 time-series for cloudant.

```
{{site.data.keyword.codeengineshort}}: 60 time-series/month
{{site.data.keyword.cloudant_short_notm}}: 50 time-series/month
Total: 110 time-series/month * 730 hours/month = 
110 * $0.08 per metric = $8.80
```

## Conclusion
{: #conclusion}

This pricing scenario provides an estimate of the costs associated with running a {{site.data.keyword.codeengineshort}} application that utilizes {{site.data.keyword.cloudant_short_notm}}, {{site.data.keyword.logs_full_notm}}, and {{site.data.keyword.mon_full_notm}} provided by {{site.data.keyword.Bluemix}}. The total estimated cost for this scenario is $327.00 USD per month. However, it's important to note that actual costs may vary based on your specific usage patterns, data volumes, and configuration choices.

To get a more accurate estimate tailored to your specific needs, you can use the [IBM Cloud cost estimator](/docs/billing-usage?topic=billing-usage-cost). This tool allows you to input your expected usage for various services and provides a customized cost estimate based on current pricing.

By carefully estimating your costs and utilizing the available tools, you can make informed decisions about your cloud resource usage and optimize your spending on the {{site.data.keyword.Bluemix}} platform.