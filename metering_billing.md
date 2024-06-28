---

copyright:
  years: 2017, 2024

lastupdated: "2024-02-26"

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:note: .note}
{:screen: .screen}

# Metering integration
{: #meteringintera}

**STAGING ONLY**

{{site.data.keyword.Bluemix}} supports multiple models for services that are provided by IBM to have their usage aggregated. Various metrics are measured on the provisioned instances and are submitted to the metering service. The rating service aggregates the submitted usage into different buckets (instance, resource group, and account), based on the model chosen by the service. The aggregation and rating models for all the metrics in a plan are contained in the metering and rating definition documents for the plan. The following expectations are for tracking and submitting usage:

*	Free and paid plans both require a usage submission. Usage submission can be waived for free plans with a special request and agreement from the appropriate {{site.data.keyword.Bluemix_notm}} team.
*	Monthly plans and metered plan models are supported.
*	Usage must be submitted in windows every 2 - 24 hours. Lite plans must submit every 15 minutes to 2 hours.
*	The service must attempt failure responses again. {{site.data.keyword.Bluemix_notm}} doesn't provide a retry function for failed submissions. For more information, see the status codes and actions table in [{{site.data.keyword.Bluemix_notm}} Usage Metering](https://cloud.ibm.com/apidocs/usage-metering).
*	Usage records for the current month must be submitted, at the latest, by the 2nd of the following month.
*	{{site.data.keyword.Bluemix_notm}} is configured for a monthly billing cycle and time is represented in Coordinated Universal Time.
* Do not assume calculations for the monthly billing cycle before you submit the usage.

For information about pricing, see [How to calculate your costs](/docs/billing-usage?topic=billing-usage-cost).

## Configuration properties
{: #configur}

The following properties define how {{site.data.keyword.Bluemix}} meters and rates usage submissions for product plans:

Unit
:   Metrics to be metered, for example, ApiCall, Bytes, Hours, Instances, and Nodes.

Aggregation
:   How metered unit data is compiled, for example INSTANCES_BY_MONTH, or ACTIVE_HOURS_BY_MONTH.

Metering model
:   How usage submission data is processed, as shown in the Metering model table.

Resource name
:   The name of the resource that is being measured, for example, Storage, Instance, Virtual Server, or Bytes transmitted.

Unit name
:   The descriptive name of the unit if the default name is not relevant for the product.


## Metering model types
{: #metermodel}

The following table shows the available metering models and a brief description of each type:

|  *Type* | *Description*  |
|-----|-----|
| **standard_add** | Add quantity from all submitted usage records for a month. |
| **standard_max**  | Max quantity from all submitted usage records for a month. |
| **standard_avg** | Average quantity from all submitted usage records for a month. |
| **dailyproration_max** | Calculated daily max. Sum up all the days for month. |
| **dailyproration_avg** | Calculated daily average. Sum up all the days for month. |
| **monthlyproration** | Calculated like the daily proration, but the price that is used is the plan price that is divided by the total number of days for the month (daily price). |
{: caption="Table 1. Metering model" caption-side="top"}

### Examples
The Quantity in Dashboard is before the next usage is submitted, but after the current usage is processed.

#### Standard Add
Add up usages for the entire month.

Formula: ADD(Usages)

| Time            | Usage Sent In | Calculation | Quantity in Dashboard |
|-----------------|:-------------:| ----------- |:---------------------:|
| Day 1 (morning) | 5             | 5           | 5                     |
| Day 1 (night)   | 5             | 5 + 5       | 10                    |
| Day 2 (morning) | 5             | 10 + 5      | 15                    |
| Day 3 (morning) | 5             | 15 + 5      | 20                    |
| Day 4 (night)   | 5             | 20 + 5      | 25                    |

#### Standard Average
Take the average of the usages for the entire month. Submitting a 0 usage counts toward the average.

Formula: AVG(Usages)

| Time            | Usage Sent In | Calculation             | Quantity in Dashboard |
|-----------------|:-------------:| ----------------------- |:---------------------:|
| Day 1 (morning) | 4             | 4 / 1                   | 4                     |
| Day 1 (night)   | 0             | (4 + 0) / 2             | 2                     |
| Day 2 (morning) | 5             | (4 + 0 + 5) / 3         | 3                     |
| Day 3 (morning) | 3             | (4 + 0 + 5 + 3) / 4     | 3                     |
| Day 4 (night)   | 3             | (4 + 0 + 5 + 3 + 3) / 5 | 3                     |

#### Standard Max
Take the max of the usages for the entire month.

Formula: MAX(Usages)

| Time            | Usage Sent In  | Calculation  | Quantity in Dashboard |
|-----------------|:--------------:| ------------ |:---------------------:|
| Day 1 (morning) | 5              | MAX(5)       | 5                     |
| Day 1 (night)   | 10             | MAX(5, 10)   | 10                    |
| Day 2 (morning) | 0              | MAX(10, 0)   | 10                    |
| Day 3 (morning) | 15             | MAX(10, 15)  | 15                    |
| Day 4 (night)   | 1              | MAX(15, 1)   | 15                    |

#### Dailyproration Average
Take the average usage for each day and average it for the month. The {{site.data.keyword.Bluemix_notm}} billing team adds up the average of each day and divides it by the number of days currently passed (in Coordinated Universal Time).

Formula: Summation(Daily Average) / Number of Days Passed in Billing Period

The quantity might change throughout the month, but the number that the BSS rates is the average usage per day.
{: note}

Given a 30-day month:

| Time               | Usage Sent In    | Daily Average | Calculation                            | Quantity in Dashboard*                           |
| ------------------ | :--------------: | ------------- | ------------------                     | :----------------------------------------------: |
| Day 1 (morning)    | 8                | 8 / 1         | 8 / 1                                  | 8                                                |
| Day 1 (night)      | 3                | (8 + 3) / 2   | 5.5 / 1                                | 5.5 (On Day 1 EOD)                               |
| Day 2 (morning)    | 2                | 2 / 1         | (5.5 + 2) / 2                          | 3.75                                             |
| Day 2 (night)      | 5                | (2 + 5) / 2   | (5.5 + 3.5) / 2                        | 4.5 (On Day 2 EOD)                               |
| Day 3 to Day 15    | 1                | 1 / 1         | (5.5 + 3.5 + (1 + 13) / 15            | 1.4666 (On Day 15 EOD)                          |
| Day 15 to Day 30   | 0                | 0 / 1         | (5.5 + 3.5 + (1 * 12) + (0 * 15) / 30 | 0.7333 (On Day 20 EOD)                          |

\* As seen on the same day as when the usage was submitted.

#### Dailyproration Max
Take the max usage per day and average it for the month. BSS adds up the max of each day and divides it by the number of days currently passed (in Coordinated Universal Time).

Formula: Summation(Daily Max) / Number of Days Passed in Billing Period

The quantity might change throughout the month, but the BSS rates the max usage per day.
{: note}

Given a 30-day month:

| Time             | Usage Sent In  | Daily Max | Calculation                    | Quantity in Dashboard* |
|------------------|:--------------:| --------- | ------------------------------ |:----------------------:|
| Day 1 (morning)  | 0              | MAX(0)    | 0 / 1                          | 0                      |
| Day 1 (night)    | 1              | MAX(0, 1) | 1 / 1                          | 1                      |
| Day 2 to Day 15  | 1              | MAX(1)    | (1 + 1 + ...) / day            | 1                      |
| Day 15 to Day 30 | 0              | MAX(0)    | (1 + (1 * 14) + 0 + ...) / day | < 1                    |

\* As seen on the same day as when the usage was submitted.

## Metering and rating scale examples

**Do we want these revealed to the customers?**

You can use the scaling configuration to compile the unit quantity differently from what is sent in usage submissions to what is displayed in the {{site.data.keyword.Bluemix_notm}} console under the **Usage Dashboard** section. You can also compile what is finally used for the rating and cost calculations.

The following examples demonstrate scenarios when these values need to be configured:

### You want more granularity than what users see
Some products want to send usages at a more granular level, but show customers a more readable number.

For example, a product might want to measure an instance's traffic in Bytes and want the aggregated values in Megabytes. You would add to the **metering** configuration a `scale` of 1024.

### You want more granularity than what your pricing configuration has
Some products price their metrics as (for example) $X / Gigabyte, but want to send in Megabytes. If your metric is priced at $1 / Gigabyte, but a user uses 0.5 Megabytes, they are charged $1 (since your pricing is per Gigabyte). If so, you would add to the **rating** configuration a `scale` of 1024 and set `clip` to `true`.

This holds true if your metric is also priced as $X per 100 API Calls (or some other pack size).

### Scaling at both Metering and Rating levels
You can add scaling to both metering and rating configurations.

If you want to send in Bytes, but want to show Megabytes to the customer, then you configure metering scale to 1024.
If your metric price is in Gigabytes, then you also configure rating scale to be 1024.
