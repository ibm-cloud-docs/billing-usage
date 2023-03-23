---

copyright:
  years: 2015, 2023
lastupdated: "2023-03-23"

keywords: payment, charges, pricing plan, service cost, cost, pricing tier, pricing model, pricing

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# How you're charged
{: #charges}

{{site.data.keyword.cloud}} charges vary depending on the resources that are used by a particular service, runtime, container, or support option. The resources can be the number of API calls, the number of instances, memory, or storage. In addition, tiered pricing is offered in simple, graduated, or block.
{: shortdesc}

{{site.data.keyword.Bluemix_notm}} provides detailed [cost estimators](/docs/billing-usage?topic=billing-usage-cost) to help you plan for charges.
{: tip}

After you build your resources, you can check the actual cost. In the {{site.data.keyword.cloud}} console, go to **Manage > Billing and usage**, and select **Usage**. With an {{site.data.keyword.Bluemix_notm}} billable account, you're charged for the compute, containers, and services that your organization used. You might be invited by other {{site.data.keyword.Bluemix_notm}} users to participate in organizations under a different account. The usage of the apps or services that you use in the organizations that you're invited to are charged to the account that contains those organizations. You can see more information about a specific charge from each resource details page.

Different types of charges apply depending on the features of {{site.data.keyword.Bluemix_notm}} that you're using. The following table provides a high-level overview:

| Type of Charge | Description      | Resource Type            | Example                  |
|----------------|------------------|--------------------------|--------------------------|
| Fixed          | Fixed-rate pricing is based on an agreed upon monthly charge. If you buy an additional bare metal server, virtual server, or storage resource after the start of the monthly billing period, the cost of the resource for the first month is prorated based on the number of days remaining in the billing period. The prorated cost is billed in a separate invoice.  | Services  | For Bare Metal Servers, there are fixed plans to choose from, and those plans are charged at a fixed monthly rate.|
| Metered        | Usage is a unit-based pricing model in which you pay for what you consume. In this case, the number of GB hours that are consumed for runtimes and the number of IP addresses and storage that is consumed for containers.  | Services, Compute, and Containers | For {{site.data.keyword.mobilepushshort}}, any usage that is consumed over the free monthly allowance of 100,000 digital messages per month, will be charged.  |
| Tiered         | In this pricing model, you get a volumed-based discount according to your actual usage. Tiered pricing is typically used for charge metrics that are expected to have high quantities per month, such as API calls. Services might offer simple, graduated, or block tier pricing plans. | Services | For {{site.data.keyword.apiconnect_short}}, one of the tiered plans charges $10,000 for the first 25 million monthly API calls and $40.00 USD per 100,000 API calls per month thereafter.|
| Reserved       | Reserved pricing is based on a long-term commitment for a service, so you can get a discounted price. With a reserved plan, you get a dedicated service instance that is easy to set up, deploy, and deliver in the public {{site.data.keyword.Bluemix_notm}} environment. | Services | Db2 on Cloud has reserved plans.|
{: caption="Table 1. Charges based on features" caption-side="top"}

## Understanding monthly and hourly tags
{: #monthly-hourly-tags}

On the usage dashboard, your products and resources can be labeled with `Monthly`, `Hourly`, or a combination of both tags to signify how often charges are updated.

The `Monthly` tag signifies that resources within your account have a fixed cost. These charge show up immediately after purchase and are prorated in proportion to how many days are left in the month. The fixed costs is then shown at the first of every month.

The `Hourly` tag signifies that resources within your account have variable costs that can change throughout the day. These resources are updated every day.

## Lite plans
{: #liteplans}

Lite plans are structured as a free quota. You can work on your projects worry free, without the risk of generating an accidental bill. The quota might operate for a specific time period, for example a month, or on a one-off usage basis. The following list provides some examples of Lite plan quotas:

   * Maximum number of registered devices
   * Maximum number of application bindings
   * Encrypted data storage limit, for example 1 GB
   * Provisioned throughput capacity

You can easily find services for Lite plans in the catalog. By default, all services with a Lite plan are displayed with a **Lite** tag ![Lite tag](../icons/Lite.svg "Lite"). Select a service to view the quota details for the associated Lite plan.


## Charges for compute resources
{: #compute}

You're charged for the time that your apps run and the memory that's used in *GB-hours*. GB-hours is the calculation of the number of application instances that are multiplied by the memory per instance and by the hours that the instances run. You can customize the number of instances and the amount of memory per instance based on your needs. You can also add memory or instances to scale for more users. To get the amount charged, take your application instances that are multiplied by memory per instance and by hours running.

For example, consider a runtime that costs $0.07 per GB-hour in two 512-MB instances, running for 30 days (720 hours). These resources would cost $50.4 USD, with the following calculations:


```
2 instances x 0.5 GB x 720 hours = 720 GB-hours.
720 GB-hours x $0.07 per GB-hour = $50.4
```

## Charges for services
{: #charges-services}

Many services include monthly free allowances. Usage of services that aren't included as part of the free allowance is charged in one of the following ways:

Fixed charges
:   You select a plan and pay on a flat rate basis. For example, the Bare Metal Servers are charged at a flat-rate.

Metered charges
:   You pay based on your runtime and service consumption. For example, with the Push service, any usage over the free monthly allowance is charged.

Reserved charges
:   As the account owner of a Pay As You Go account or a Subscription account, you can reserve a service instance, with a long-term commitment, for a discounted price. For example, you can reserve the standard large Db2 on Cloud offering for 12 months.
:   Some {{site.data.keyword.Bluemix_notm}} services offer reserved plans. You can request a reserved plan from the {{site.data.keyword.Bluemix_notm}} catalog by clicking the tile of the service. Then, select the service plan that best meets your needs. If a reserved plan is available, click **Request**, and follow the prompts to send your request. You receive an email that contains the price information of the reserved plan. An {{site.data.keyword.Bluemix_notm}} sales representative also contacts you soon to complete the purchase.

Tiered charges
:   Similar to metered charges, you pay based on your runtime and service consumption. However, tiered charges add more pricing tiers, often offering discounted charges in tiers with larger consumption. Tiered pricing is offered in simple, graduated, or block.

### Simple tier
{: #simple_tier}

In the simple tier model, the unit price is determined by the tier that the quantity of your usage falls into. The total price is your quantity that is multiplied by the unit price in that tier, for example:

| Quantity of Items   | Unit Price for All Items |
|---------------------|--------------------------|
| Tier 1: 1 - 1000    | $1 USD                   |
| Tier 2: 1001 - 2000 | $0.90 USD                |
| Tier 3: 2001 - 3000 | $0.75 USD                |
| Tier 4: 3001 - 4000 | $0.60 USD                |
| Tier 5: &gt; 4000   | $0.40 USD                |
{: caption="Table 2. Simple tier pricing table" caption-side="top"}

The following table illustrates how much you pay with a plan that is based on a simple tier pricing model:

| Quantity of Items | Charge Calculation | Total Price |
|-------------------|--------------------|-------------|
| 500               | 500 × 1 = 500      | $500 USD    |
| 1500              | 1500 × 0.90 = 1350 | $1350 USD   |
| 2500              | 2500 × 0.75 = 1875 | $1875 USD   |
| ...               | ...                | ...         |
| 5200              | 5200 × 0.40 = 2080 | $2080 USD   |
{: caption="Table 3. Charge calculation by using the simple tier pricing model" caption-side="top"}

### Graduated tier
{: #graduated_tier}

In the graduated tier model, the unit price per tier decreases as your level of usage increases. The total price is the cumulative charges for each level of usage, consisting of your quantity multiplied by the unit price at that tier, for example:

| Quantity of Items   |	Unit Price for Items in the Tier|
|---------------------|---------------------------------|
| Tier 1: 1 - 1000    |	$1 USD                          |
| Tier 2: 1001 - 2000 |	$0.90 USD                       |
| Tier 3: 2001 - 3000 |	$0.75 USD                       |
| Tier 4: 3001 - 4000 |	$0.60 USD                       |
| Tier 5: &gt; 4000   |	$0.40 USD                       |
{: caption="Table 4. Graduated tier pricing table" caption-side="top"}

The following table illustrates how much you pay with a plan that is based on a graduated tier pricing model:

|Quantity of Items | Charge Calculation                                                               | Total Price |
|------------------|----------------------------------------------------------------------------------|-------------|
| 500              | 500 × 1 (unit price for Tier 1) = 500                                            |	$500 USD    |
| 1500             | (1000 × 1 (unit price for Tier 1)) + (500 × 0.90 (unit price for Tier 2)) = 1450 |	$1450 USD   |
| 2500             | (1000 × 1 (unit price for Tier 1)) + (1000 × 0.90 (unit price for Tier 2)) + (500 × 0.75 (unit price for Tier 3)) = 2275 | $2275 USD |
| ...              | ...                                                                              | ...         |
| 5200             | (1000 × 1 (unit price for Tier 1)) + (1000 × 0.90 (unit price for Tier 2)) + (1000 × 0.75 (unit price for Tier 3)) + (1000 × 0.60 (unit price for Tier 4)) + (1200 × 0.40 (unit price for Tier 5)) = 3730 | $3730 USD |
{: caption="Table 5. Charge calculation by using the graduated tier pricing model" caption-side="top"}

### Block tier
{: #block_tier}

In the block tier model, the price is a set charge for the quantity you use within a usage level. The total price is the charge for your level of usage regardless of your actual usage. Each successive tier provides a lower price to quantity ratio. For example:

|Quantity of Items    |	Total Price for All Items |
|---------------------|---------------------------|
| Tier 1: &lt;= 1000  |	$1000 USD                 |
| Tier 2: &lt;= 2000  |	$1900 USD                 |
| Tier 3: &lt;= 3000  |	$2800 USD                 |
| Tier 4: &lt;= 4000  |	$3500 USD                 |
| Tier 5: &lt;= 10000 |	$5000 USD                 |
{: caption="Table 6. Block tier pricing table" caption-side="top"}

The following table illustrates how much you pay with a plan that is based on a block tier pricing model:

|Quantity of Items | Charge Calculation                                                      | Total Price|
|------------------|-------------------------------------------------------------------------|------------|
| 500              | The number of items falls into Tier 1, so the total price is $1000 USD. | $1000 USD  |
| 1500             | The number of items falls into Tier 2, so the total price is $1900 USD. | $1900 USD  |
| ...              | ...                                                                     | ...        |
| 5200             | The number of items falls into Tier 5, so the total price is $5000 USD. | $5000 USD  |
{: caption="Table 7. Charge calculation by using the block tier pricing model" caption-side="top"}
