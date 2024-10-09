---

copyright:
  years: 2015, 2024
lastupdated: "2024-09-03"

keywords: estimate cost, cost example, billing example, payment example, calculating app price, Code Engine

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}


# Scenario: Estimating costs of a {{site.data.keyword.codeengineshort}} app with a {{site.data.keyword.cloudant_short_notm}} Database and Observability tools
{: #sample}

Assume that you are planning to deploy a web application on {{site.data.keyword.codeenginefull}} along with several {{site.data.keyword.Bluemix}} services including a database, logging, and monitoring. This example demonstrates how to estimate the cost of your application.
{: shortdesc}

With {{site.data.keyword.codeenginefull}}, you pay for only the memory and CPU needed to run your application and any incoming HTTP calls. This includes [scaling to 0](/docs/codeengine?topic=codeengine-app-scale#app-scale-boundaries) if your application doesn't receive any traffic for a [specified period](/docs/codeengine?topic=codeengine-app-scale#app-scale-timeconcurrency). For this example, let's assume that a production application receives a constant flow of traffic. The app has the following specifications:

- This application requires 1 vCPU and 4 GB of memory to run.
- Over its first 30 days, this application expects to handle 5 million HTTP requests.
- A {{site.data.keyword.cloudant_short_notm}} database on the standard plan is required to support the application's data storage needs:
   - 150 GB of data of stored storage.
   - Performance requirements include 1,000 lookups per second, 500 writes per second, and 50 queries per second.
- For log storage and search, the application uses a {{site.data.keyword.logs_full_notm}} Standard plan:
   - It requires fast search capabilities for at least 7 days of data.
   - Log retention is set to 3 months in {{site.data.keyword.cloud_notm}}.
   - It is estimated that on average there are 1,000 logging alerts per month, which is sent through {{site.data.keyword.en_full_notm}} by {{site.data.keyword.logs_full_notm}}. The alerts are sent to a webhook destination such as [Microsoft™ Teams](/docs/event-notifications?topic=event-notifications-en-destinations-msteams), [Slack™](/docs/event-notifications?topic=event-notifications-en-destinations-slack), or [PagerDuty™](/docs/event-notifications?topic=event-notifications-en-destinations-pagerduty)
- The application required Monitoring (Mon) for performance metrics:
   - Only platform metrics from {{site.data.keyword.codeengineshort}} and {{site.data.keyword.cloudant_short_notm}} are needed.

This scenario uses several of these services together to create a robust, scalable, and observable application environment. {{site.data.keyword.codeengineshort}} provides a flexible, serverless platform for your application, while {{site.data.keyword.cloudant_short_notm}} offers a reliable and scalable database solution. The addition of {{site.data.keyword.logs_full_notm}} and {{site.data.keyword.mon_full_notm}} helps ensure comprehensive observability, so you can you to monitor performance, troubleshoot issues, and optimize your application efficiently. This integrated approach enables developers to focus on building and improving their applications while relying on {{site.data.keyword.Bluemix}}'s managed services for infrastructure and operational concerns.

An estimate of the total monthly cost to run the application infrastructure can be created with the help of the [{{site.data.keyword.Bluemix}} cost estimator](/docs/billing-usage?topic=billing-usage-cost). Rather than using the {{site.data.keyword.Bluemix}} cost estimator this scenario walks through these calculations manually to help understand how the steps of determine reasonable inputs into the calculations and dealing with free-tier usage.

The prices that are used in this example are in US currency and might not reflect current prices and don't include any discounts or promo codes. For the most up-to-date prices, see [{{site.data.keyword.codeengineshort}} pricing](/codeengine/overview#pricing), [{{site.data.keyword.cloudant_short_notm}} pricing](/docs/Cloudant?topic=Cloudant-pricing), [{{site.data.keyword.logs_full_notm}} pricing](/docs/cloud-logs?topic=cloud-logs-service_plans), [{{site.data.keyword.mon_full_notm}} pricing](/docs/monitoring?topic=monitoring-pricing_plans), or [][{{site.data.keyword.en_full_notm}} pricing](https://cloud.ibm.com/docs/event-notifications?topic=event-notifications-en-new-pricing).
{: important}

## Cost Summary
{: #cost-summary}

The following table provides an example of the estimated cost for running an application in {{site.data.keyword.codeengineshort}} that uses {{site.data.keyword.cloudant_short_notm}} Standard plan as a data store, along with {{site.data.keyword.logs_full_notm}} and {{site.data.keyword.mon_full_notm}}. {{site.data.keyword.cloud_notm}} is also required to query log data older than 7 days and {{site.data.keyword.en_full_notm}} is used by {{site.data.keyword.logs_full_notm}} for sending alerts. The scenario assumes the following usage quantities and rates:


| Description | Quantity | Rate | Cost |
|----------------------------------|----------|-------------------|------|
| {{site.data.keyword.codeengineshort}} - vCPU seconds | 2,492,000 | $0.00003431 | $85.50 |
| {{site.data.keyword.codeengineshort}} - GB seconds | 10,168,000 | $0.00000356 | $36.20 |
| {{site.data.keyword.codeengineshort}} - Requests | 4,900,000 | $0.538 per million | $2.64 |
|  |  | **Subtotal** | **$124.34** |
|  |  |  |  |
| {{site.data.keyword.cloudant_short_notm}} - GB | 130 | $1.00 per GB | $130.00 |
| {{site.data.keyword.cloudant_short_notm}} - Lookups/second | 10 | $0.25 per 100 Lookups/second | $2.50 |
| {{site.data.keyword.cloudant_short_notm}} - Writes/second | 10 | $0.50 per 50 Write/second | $5.00 |
| {{site.data.keyword.cloudant_short_notm}} - Queries/second | 10 | $5.00 per 5 Query/second | $50.00 |
|  |  | **Subtotal** | **$187.50** |
|  |  |  |  |
| {{site.data.keyword.logs_full_notm}} - 7 days | 5 GB | $1.20 per GB | $6.00 |
|  |  | **Subtotal** | **$6.00** |
|  |  |  |  |
| {{site.data.keyword.mon_full_notm}} - Time-series Metrics | 110 | $0.08 per metric | $8.80 |
|  |  | **Subtotal** | **$8.80** |
|  |  |  |  |
| {{site.data.keyword.cloud_notm}} - Storage capacity | 15 GB | $0.0230 per GB/month | $0.36 |
| {{site.data.keyword.cloud_notm}} - Public outbound bandwidth | 15 GB | $0.0000 per GB (within allowance) | $0.00 |
| {{site.data.keyword.cloud_notm}} - Class A requests | 15,000 | $0.0000 per 1,000 (within allowance) | $0.00 |
| {{site.data.keyword.cloud_notm}} - Class B requests | 150,000 | $0.0000 per 10,000 (within allowance) | $0.00 |
|  |  | **Subtotal** | **$0.36** |
|  |  |  |  |
| {{site.data.keyword.en_full_notm}} - Ingested Events | 1,000 | $1.08 USD/Million events | $0.00108 |
| {{site.data.keyword.en_full_notm}} - Outbound Digital Message HTTP | 1,000 | $1.08 USD/Million Events | $0.00108 |
|  |  | **Subtotal** | **$0.00216** |
|  |  |  |  |
|  |  | **Total** | **$327.00** |
{: caption="Estimated costs for a {{site.data.keyword.codeengineshort}} application with {{site.data.keyword.cloudant_short_notm}} Standard plan, {{site.data.keyword.logs_full_notm}}, and {{site.data.keyword.mon_full_notm}}" caption-side="bottom"}

## Calculation details
{: #calculation-details}

To understand the total cost of the application, let's break down the calculations for each service. These details help you see how costs accumulate across different components of the architecture.
We'll examine the costs for {{site.data.keyword.codeengineshort}}, {{site.data.keyword.cloudant_short_notm}}, {{site.data.keyword.logs_full_notm}}, {{site.data.keyword.en_full_notm}}, {{site.data.keyword.mon_full_notm}}, and more {{site.data.keyword.cloud_notm}} storage. Remember, your actual costs might vary based on specific usage and configuration.

### {{site.data.keyword.codeengineshort}} Calculation details
{: #codeengine-cost-details}

With {{site.data.keyword.codeengineshort}} you are charged for the amount of vCPU, memory, and HTTP requests. The vCPU and memory is based on your chosen cpu and memory profile and the number of application instances. Keep in mind that your application might not use of all of the CPU and memory available, so it's important to choose the most appropriate [CPU and memory profile](/docs/codeengine?topic=codeengine-mem-cpu-combo#supported-combo) and [determining the right concurrency settings](/docs/codeengine?topic=codeengine-app-scale#app-determine-concurrency) for your application to run cost efficiently. For more details on {{site.data.keyword.codeengineshort}} Pricing see the [{{site.data.keyword.codeengineshort}} documentations](/docs/codeengine?topic=codeengine-pricing#app-pricing)

The following calculations include the {{site.data.keyword.codeengineshort}} no-cost tier allocations which include:
{: #code-engine-free-tier}

* 100,000 vCPU seconds per month
* 200,000 GB seconds of memory per month
* 100,000 HTTP requests per month

#### vCPU
{: #vCPU}

```text
1 Application Instance * 1 vCPU * 24 hours * 30 days * 3600 seconds = 2,592,000 vCPU seconds
Free tier: 100,000 vCPU seconds
Billable: 2,592,000 - 100,000 = 2,492,000 vCPU seconds
2,492,000 * $0.00003431 = $85.50
```

#### Memory
{: #Memory}

```text
1 Application Instance * 4 GB * 24 hours * 30 days * 3600 seconds = 10,368,000 GB seconds
Free tier: 200,000 GB seconds
Billable: 10,368,000 - 200,000 = 10,168,000 GB seconds
10,168,000 * $0.00000356 = $36.20
```


#### HTTP Requests
{: #HTTP-Requests}

```text
5,000,000 requests total
Free tier: 100,000 requests
Billable: 5,000,000 - 100,000 = 4,900,000 requests
4,900,000 * ($0.538 / 1,000,000) = $2.64
```

### {{site.data.keyword.cloudant_short_notm}} Calculation details
{: #cloudant-cost-details}

{{site.data.keyword.cloudant_short_notm}} pricing is based on the provisioned throughput capacity that you set for your instance, and the amount of data storage.

In our scenario, we're using 150 GB of storage, but with 20 GB of free data storage, we pay for the extra 130 GB. The throughput capacity is based on the required lookups, writes, and queries in their respective increments.
For more detailed information about {{site.data.keyword.cloudant_short_notm}} pricing, see [{{site.data.keyword.cloudant_short_notm}} Pricing](/docs/Cloudant?topic=Cloudant-pricing).
{: #cloudant-pricing-details}

#### Standard plan - Data
{: #cloudant-standard-plan-data}

```text
150 GB total, 20 GB free, 130 GB charged
130 GB * $1.00 per GB = $130.00
```

#### Standard plan - Lookups
{: #cloudant-standard-plan-lookups}

```text
1,000 Lookups/second / 100 Lookups/second = 10 units
10 * $0.25 per 100 Lookups/second = $2.50
```

#### Standard plan - Writes
{: #cloudant-standard-plan-writes}

```text
500 Writes/second / 50 Writes/second = 10 units
10 * $0.50 per 50 Writes/second = $5.00
```

#### Standard plan - Queries
{: #cloudant-standard-plan-writes}

```text
50 Queries/second / 5 Queries/second = 10 units
10 * $5.00 per 5 Queries/second = $50.00
```

### {{site.data.keyword.logs_full_notm}} Calculation details
{: #cloud-logs-cost-details}

{{site.data.keyword.logs_full_notm}} supports [tiering of your log data](/docs/cloud-logs?topic=cloud-logs-tco-optimizer) to help optimize your logging costs while still being able to search and analyze application log data. In this scenario, log data is stored in the initial default of 7 day retention in Priority Insights. After 7 days, the log data will still be queryable from {{site.data.keyword.cloud_notm}} at the {{site.data.keyword.cloud_notm}} rates. It is assumed that logs are retained for 3 months in {{site.data.keyword.cloud_notm}}.

#### Priority insights - 7 days Calculation details
{: #logs-priority-insights}

Estimated Monthly log volume: 1 KB per request * 5,000,000 requests/month * 1 month = 5 GB

```text
5 GB * $1.20 per GB = $6.00
```

### {{site.data.keyword.cloud_notm}} Calculation details
{: #cloud-calc-details}

There are various pricing plans for {{site.data.keyword.cloud_notm}} depending on the desired [storage class](/docs/cloud-object-storage?topic=cloud-object-storage-billing#billing-storage-classes). This scenario uses the `standard` storage class, which is meant for active workloads, since {{site.data.keyword.logs_full_notm}} needs to query the data. The `standard` storage class bills based on the amount of data that is stored along with the number of inbound and outbound requests. Alternatively, the [one rate plan](/docs/cloud-object-storage?topic=cloud-object-storage-onerate), which includes allowances for inbound and outbound requests, might be a good option if you expect that logs older than 7 days are queried frequently. See [{{site.data.keyword.cloud_notm}} Pricing](/objectstorage/create#pricing) for more details on the different options and rates.

#### Standard plan - Storage
{: #cos-free-tier}

The Standard plan includes a no-cost tier, which is based on the amount of data that you store. It is expected that 15 GB of data is stored based on the following calculation.

```text
3 months of logs: 1 KB per request * 5,000,000 requests/month * 3 months = 15 GB
```

```text
Storage capacity Costs:
15 GB * $0.0230 per GB/month = $0.36

Public outbound bandwidth Costs:
Allowance: 100% of storage in GB = 15 GB
Actual usage: 15 GB
15 GB ≤ 15 GB allowance, so no additional charge
```


#### Standard plan - Class A requests (writes)
{: #cos-writes}

```text
Allowance: 100 x storage in GB = 100 x 15 = 1,500 requests
Actual usage: Assuming file writes every 10 min, there would be 43,800 minutes/month / 10 minutes = 4,380
4,380 > 1,500 allowance, but charge applies per 1,000 requests
Billable requests: 4,380 - 1,500 = 2,880
2,880 * ($0.0052 / 1,000) = $0.014976 (rounded to $0.01 due to small amount)
```

#### Standard plan - Class B requests (reads)
{: #cos-reads}

```text
Allowance: 1,000 x storage in GB = 1,000 x 15 = 15,000 requests
Actual usage: Let's assume we read 3 files for every file written in a month, 4,380 * 3 = 13,140
13,140 < 15,000 allowance, but charge applies per 10,000 requests

Billable requests: Below allowance, so there is no charge
```

```text
Total {{site.data.keyword.cos_full_notm}} cost: $0.36 + $0.00 + $0.01 + $0.00 = $0.37
```

### {{site.data.keyword.mon_full_notm}} Calculation details
{: #cloud-monitoring-pricing-details}

Monitoring of {{site.data.keyword.codeengineshort}} and {{site.data.keyword.cloudant_short_notm}} is enabled by using platform metrics. Platform metrics are metrics that are generated by {{site.data.keyword.Bluemix}} services for your service instances. These metrics are treated as a time-series, which is a series of data-points that are ordered by time that contains various metadata or labels. These metrics are billed by using a [tiered pricing model](/docs/monitoring?topic=monitoring-pricing_plans#graduated_tier) that depends on the quantity of time-series metrics being sent in a given time period. See the {{site.data.keyword.mon_full_notm}} docs for an [example of platform metric billing](/docs/monitoring?topic=monitoring-pricing_plans#billing_example).

```text
time-series metrics: $0.08 USD per metric
```

In this scenario, assume 110 time-series metrics (50 for {{site.data.keyword.codeengineshort}} and 60 for {{site.data.keyword.cloudant_short_notm}}).

#### Time-series Metrics
{: #sysdig-time-series-metrics}

[{{site.data.keyword.codeengineshort}}](/docs/codeengine?topic=codeengine-monitor#metrics-by-plan) and [{{site.data.keyword.cloudant_short_notm}}](/docs/Cloudant?topic=Cloudant-monitor-ibm-cloud-pm#metrics_dictionary-pm) provide various platform metrics to monitor your applications. The number of [time-series depends on the cardinality](https://docs.sysdig.com/en/docs/sysdig-monitor/using-monitor/metrics/using-labels/#cardinality){: external}, or number of unique time series associated with a given metric. In this scenario, assume 60 time-series for {{site.data.keyword.codeengineshort}} and 50 time-series for {{site.data.keyword.cloudant_short_notm}}.

```text
{{site.data.keyword.codeengineshort}}: 60 time-series/month
{{site.data.keyword.cloudant_short_notm}}: 50 time-series/month
Total: 110 time-series/month * 730 hours/month =
110 * $0.08 per metric = $8.80
```

### {{site.data.keyword.en_full_notm}} Calculation details
{: #event-notifications-pricing-details}

{{site.data.keyword.logs_full_notm}} alerts are triggered through the {{site.data.keyword.en_full_notm}} service. See [enabling {{site.data.keyword.en_full_notm}} for {{site.data.keyword.logs_full_notm}}](/docs/cloud-logs?topic=cloud-logs-event-notifications-events&interface=ui#event-notifications-enable) to set this up. {{site.data.keyword.en_full_notm}} bills based on the quantity of incoming events and outbound destinations. Various [destinations are supported](/docs/event-notifications?topic=event-notifications-supported-destinations) each at their own rate. In this scenario only the HTTP destination is needed.

The number of alerts that might generate from {{site.data.keyword.logs_full_notm}} might vary by month but this scenario assumes 1,000 alerts.

#### Inbound Events
{: #en-inbound-events}

```text
Ingested Events: $1.08 USD/Million events
1,000 Events * $0.00000108 USD/Event = $0.00108
```

#### Outbound Events
{: #en-outbound-events}

```text
Outbound Digital Message HTTP: $1.08 USD/Million events
1,000 Events * $0.00000108 USD/Event = $0.00108
```

```text
Total Cost: $0.00108 + $0.00108 = $0.00216
```

## Conclusion
{: #conclusion}

This pricing scenario provides an estimate of the costs that are associated with running a {{site.data.keyword.codeengineshort}} application that uses {{site.data.keyword.cloudant_short_notm}}, {{site.data.keyword.logs_full_notm}}, and {{site.data.keyword.mon_full_notm}} provided by {{site.data.keyword.Bluemix}}. The total estimated cost for this scenario is $327.00 USD per month. However, actual costs might vary based on your specific usage patterns, data volumes, and configuration choices.

To get a more accurate estimate tailored to your specific needs, you can use the [{{site.data.keyword.Bluemix}} cost estimator](/docs/billing-usage?topic=billing-usage-cost). This tool allows you to input your expected usage for various services and provides a customized cost estimate based on current pricing.

By carefully estimating your costs and using the available tools, you can make informed decisions about your cloud resource usage and optimize your spending on the {{site.data.keyword.Bluemix}} platform.
