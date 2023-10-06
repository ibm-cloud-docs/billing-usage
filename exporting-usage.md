---

copyright:
  years: 2023
lastupdated: "2023-10-06"

keywords: apptio, cost benefit analysis

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

<!--staging only for now - Kent Hall-->
# Exporting your usage data to a third party provider
{: #exporting-your-usage}

You can export your account's usage data for visibility, optimization, governance and more across cloud environments. For example, if you are an account administrator and want to learn more about your account's usage and get cost optimization analysis, you can integrate your account with Apptio or to gain insights about your accounts usage.
{: shortdesc}

When you set up your account to export usage report to a (COS) bucket you are enabling your account to continually export that data. To export data on a one time basis, see [Exporting your usage details to a CSV file](/docs/billing-usage?topic=billing-usage-viewingusage&interface=ui#export-csv).

To enable your account to share usage data, you need to grant permissions to the Billing service to access usage details and export it to a Cloud Object Storage (COS) bucket. Because the report includes usage data for the entire account, child account usage and information about services and instances, the service ID used by the Billing service needs administrator access to export usage details. After this setup is complete, a CSV formatted cost and usage report is automatically exported to your COS bucket on a daily basis.


## Enabling your account to export usage data
{: #enable-export-usage}

Before you can enable your account to share usage data, you need to have Administrator or editor role on the Billing account management service. For more information, see [IAM access](/docs/account?topic=account-userroles).

To enable your account to share usage data, use the following steps:

1. From the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Billing and usage**, and select **Settings**.
1. Click **Connect**.
1. Select a Cloud Object Storage instance and Bucket. By selecting these, you are choosing which bucket will store your usage reports.
   1. Optional: If you don't want to select an existing instance, you can click **Select an instance** > **Create new**.
   1. Optional: You can select a bucket or create a new bucket by clicking **Create new bucket** in the Bucket dropdown. For more information about buckets, see [Getting started with IBM Cloud Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage). After you create your bucket
1. For service to service authorizations, click **Authorize**. For the required access, select **Object Writer** and **Content Reader**. Click **Review** and then **Assign**.
1. Click **Connect** after you review your folder details.

<!--terraform steps won't release for Oct 2 GA
## Enabling your account to export usage data by using Terraform
{: #attach-terraform}
{: terraform}

Before you can attach enable your account to export usage data by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

To enable your account to export usage data, you need to authorize a policy between two instances and provision `billing_report_snaptshot` for a resource instance. Use the following steps to attach tags to a resource by using Terraform:

1. The following example creates an authorization policy between two specific instances.

   ```terraform
   resource "ibm_iam_authorization_policy" "policy" {
   source_service_name         = "billing"
   target_service_name         = "cloud-object-storage"
   target_resource_instance_id = var.cos_instance_id
   roles                       = ["Object Writer", "Content Reader"]
   }
   ```
   {: codeblock}

1. The following example provisions `billing_report_snaptshot` for a resource instance.

   ```terraform
   resource "ibm_billing_report_snapshot" "billing_report_snapshot_instance" {
   account_id = var.billing_report_snapshot_account_id
   interval = var.billing_report_snapshot_interval
   versioning = var.billing_report_snapshot_versioning
   report_types = var.billing_report_snapshot_report_types
   cos_reports_folder = var.billing_report_snapshot_cos_reports_folder
   cos_bucket = var.billing_report_snapshot_cos_bucket
   cos_location = var.billing_report_snapshot_cos_location
   depends_on = [ ibm_iam_authorization_policy.policy ]
   }
   ```
   {: codeblock}

1. After you finish building your configuration file, initialize the Terraform CLI. For more information, see [Initializing Working Directories](https://www.terraform.io/cli/init){: external}.

   ```terraform
   terraform init
   ```
   {: pre}

1. Provision the resources from the `main.tf` file. For more information, see [Provisioning Infrastructure with Terraform](https://www.terraform.io/cli/run){: external}.

   1. Run `terraform plan` to generate a Terraform execution plan to preview the proposed actions.

      ```terraform
      terraform plan
      ```
      {: pre}

   1. Run `terraform apply` to create the resources that are defined in the plan.

      ```terraform
      terraform apply
      ```
      {: pre}
-->

### Bucket requirements
{: #enable-export-usage-bucket-requirements}

The bucket that you use to store your results does not require any particular settings or naming format. All the traffic between Billing service and Cloud Object Storage is done over a private network. The retrieval of data for display purposes in the console does not cost you anything. However, if you choose to download the data directly from Cloud Object Storage after it is stored, you do incur a data transfer cost. See [Cloud Object Storage pricing](https://cloud.ibm.com/docs/cloud-object-storage/iam?topic=cloud-object-storage-billing) for more information.

## Disconnecting your account from sharing usage
{: #disconnect-exporting-your-usage}

If you've set up your account to share usage data to a third party provider, you can disconnect your chosen bucket so that you are no longer sharing data.

To disconnect, use the following steps:

1. From the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Billing and usage**, and select **Settings**.
1. Click **Disconnect**.
1. Enter the name of your bucket.
1. Click **Disconnect**.


## Know how your usage data is stored and used
{: #storing-usage-data}


Your data shared by using billing report snapshots and by going through the steps to enable your account to export usage data, you are setting up the snapshots.

Snapshots of the billing reports are stored based on the configuration setup. Depending on the configuration, older snapshots are either deleted or retained. Each snapshot would have a manifest file describing the details of the snapshot such as the files included as part of the snapshot. The manifest of the latest snapshot for that billing month would be stored at each billing month folder as well.


The following is an example of the folder structure of the snapshots in the COS bucket.

```sh
<cos_reports_folder>/
<cos_reports_folder>/<billing-month>/
<cos_reports_folder>/<billing-month>/manifest.json
<cos_reports_folder>/<billing-month>/<snaphot-id>
<cos_reports_folder>/<billing-month>/<snaphot-id>/manifest.json
<cos_reports_folder>/<billing-month>/<snaphot-id>/*.gz
```
{: codeblock}

cos_reports_folder
:   The billing reports root folder customer has configured as part of the biling-reports-snapshots setup.
:   Defaults to IBMCloud-Billing-Reports

billing-month
:   The billing month for corresponding to the snapshot.
:   Format is `YYYY-MM`. For example, `2023-03`.

snapshot-id
:   Id of the snapshot.
:   Alphanumberic value. For example, `1678234269105`.

manifest.json
:   Metadata file describing the details of the snapshot, such as the customer account id, csv files corresponding to the snapshot, report types etc
:   The manifest file at the billing-month contains the latest snapshot taken

*.gz
:   List of files mentioned in the manifest.json

For more information about the usage snapshot API, see [Setup the snapshot configuration](/apidocs/metering-reporting#create-reports-snapshot-config){: external}.

### Understanding CSV table headings and JSON report fields for account summary
{: #export-csv-api-table-account-summary-csv}

The following table shows the correlation between the heading titles in your CSV report and JSON report fields. For more information about JSON report fields, see [Usage Reports: Get account summary](/apidocs/metering-reporting#get-account-summary){: external}. Each row of the **Account Resource Usage** section represents the aggregated usage of a service plan metric for all the resource instances in the account.

| CSV Header       | Description                                      |
|---------------------|--------------------------------------------------|
| Account Owner ID    | ID of the account                    |
| Account Name        | Name of the account                  |
| Billing Month       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Currency Rate       | Currency Exchange Rate with USD as the base     |
| Created Time        | Timestamp at which the CSV report was generated|
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-summary"}
{: #account-owner-id}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|-------------------------------|-------------|
| Account ID          | `account_id`                  | ID of the account |
| Month               | `month`                       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Country Code        | `billing_country_code`        | Country the requested account is mapped to |
| Currency Code       | `billing_currency_code`       | The currency in which the account is billed |
| Billable Cost       | `resources.billable_cost`     | The billable charges for all cloud resources used in the account |
| Non Billable Cost  | `resources.non_billable_cost` | Non-billable charges for all cloud resources used in the account |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for account usage summary" caption-side="bottom"}
{: tab-group="account-summary"}
{: #account-id}
{: tab-title="Account Usage Summary"}

| CSV Header       | JSON Report Fields                                          | Description |
|---------------------|-------------------------------------------------------------|-------------|
| Subscription ID | `subscription.subscriptions.subscription_id`                | The ID of the subscription |
| CA                  | `subscription.subscriptions.charge_agreement_number`        | The charge agreement number of the subscription |
| Type                | `subscription.subscriptions.type`                           | Type of subscription |
| Subscription Amount | `subscription.subscriptions.subscription_amount`            | The credits available in the subscription for the month |
| Start               | `subscription.subscriptions.start` or \n `subscription.subscriptions.terms.start`| Pay-As-You-Go accounts: the date from which the subscription was active \n Subscription accounts: The start date of the term |
| End                 | `subscription.subscriptions.end` or \n `subscription.subscriptions.terms.end`           | Pay-As-You-Go accounts: unavailable \n Subscription accounts: The end date of the term |
| Credits Total       | `subscription.subscriptions.credits_total` or \n `subscription.subscriptions.terms.credits.total`             | Pay-As-You-Go accounts: The total credits available in the  subscription \n Subscription accounts: The total credits available for the term  |
| Credits Starting    | `subscription.subscriptions.terms.credits.starting_balance` | The unused credits in the term at the beginning of the month |
| Credits Used        | `subscription.subscriptions.terms.credits.used`             | The credits used in this month |
| Credits Balance     | `subscription.subscriptions.terms.credits.balance`          | The remaining credits in this term |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for subscriptions" caption-side="bottom"}
{: tab-group="account-summary"}
{: #subscription-id}
{: tab-title="Subscriptions"}

| CSV Header       | JSON Report Fields                     | Description |
|---------------------|-----------------------------------|-------------|
| Offer ID            | `offers.offer_id`                 | The ID of the offer |
| Credits Total       | `offers.credits_total`            | The total credits before applying the offer |
| Offer Template      | `offers.offer_template`           | The template with which the offer was generated |
| Valid From          | `offers.valid_from`               | The date from which the offer is valid |
| Expire Date         | `offers.expires_on`               | The date until the offer is valid |
| Recurring           | `offers.is_recurring`             | Indicates if a cost is recurring |
| Starting Balance    | `offers.credits.starting_balance` | The available credits in the offer at the beginning of the month |
| Used                | `offers.credits.used`             | The credits used in this month |
| Balance             | `offers.credits.balance`          | The remaining credits in the offer |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for offers" caption-side="bottom"}
{: tab-group="account-summary"}
{: #offer-id}
{: tab-title="Offers"}

| CSV Header       | JSON Report Fields | Description |
|---------------------|--------------------|-------------|
| Support Cost        | `support.cost`     | The monthly support cost |
| Support Type        | `support.type` \n (`STANDARD` > `Advanced` and \n `PREMIUM` > `Premium`) | The type of support  |
| Support Overage     | `support.overage`  | Additional support cost for the month |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for support summary" caption-side="bottom"}
{: tab-group="account-summary"}
{: #support-cost}
{: tab-title="Support Summary"}

| CSV Header  | JSON Report Fields                 | Description |
|----------------|------------------------------------|-------------|
| Service Name   | `resources.resource_name`          | The name of the resource |
| Service ID     | `resources.resource_id`            | The ID of the resource |
| Currency       | `currency_code`                    | The currency for the cost fields in the resources, plans, and metrics |
| Billable       | `resources.billable`               | Indicates if the plan charges are billed to the customer |
| Plan Name      | `resources.plan_name`              | Name of the service plan |
| Plan ID        | `resources.plan_id`                | ID of the service plan |
| Pricing Region | `reports.resources.plans.pricing_region` | Pricing region for the plan |
| Metric         | `resources.usage.metric`           | The ID of the metric |
| Unit           | `resources.usage.unit`             | The unit that qualifies the quantity |
| Quantity       | `resources.usage.quantity`         | The aggregated value for the metric |
| Cost           | `resources.usage.cost`             | The cost incurred by the metric |
| Original Cost  | `resources.usage.rated_cost`       | Pre-discounted cost incurred by the metric |
| Pending        | `resources.pending`            | Pending charge from classic infrastructure |
| Discount (%)   | `resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID    | `resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
| Non Chargeable  | `resources.plans.usage.non_chargeable` |  When set to `true`, the cost is for informational purpose and is not included while calculating the plan charges. |
| Classic Infrastructure Product ID | `resources.plans.usage.additional_properties.classic_infrastructure_product_id`| Product ID of classic infrastructure resource |
| Classic Infrastructure Package ID | `resources.plans.usage.additional_properties.classic_infrastructure_package_id` | Package ID of classic infrastructure resource |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for account resource usage" caption-side="bottom"}
{: tab-group="account-summary"}
{: #service-name}
{: tab-title="Account Resource Usage"}



### Understanding CSV table headings and API parameters for instances
{: #table-account-summary-csv}

The following table shows the correlation between the heading titles in your CSV report and API parameters. For more information about JSON report fields, see [Usage Reports: Get resource instance usage in an account](/apidocs/metering-reporting#get-resource-usage-account). Each row of the **Account Instance Usage** section represents an instance usage of a specific metric in a service plan.

Regular account CSV reports are not real time and can be incomplete. Complete CSV reports are generated for previous months that have already been invoiced. In case of potentially inconsistent data in the CSV reports, it's advised to regenerate the CSV after couple of hours. For more accurate and real time usages, it's always recommended to use the JSON APIs.
{: note}

| CSV Header    | Description                                     |
|------------------|-------------------------------------------------|
| Account Owner ID | ID of the account                    |
| Account Name     | Name of the account                  |
| Billing Month    | The month in which usages were incurred. Represented in `yyyy-mm` format     |
| Currency Rate    | Currency Exchange Rate with USD as the base     |
| Created Time     | Timestamp at which the CSV report was generated |
{: class="simple-tab-table"}
{: caption="Table 2. Account instance CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-instance"}
{: #account-owner-id-instance}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|------------------------------------|-------------|
| Service Name        | `resources.resource_name`          | The name of the resource |
| Service ID          | `resources.resource_id`            | The ID of the resource |
| Instance Name       | `resources.resource_instance_name` | The name of the resource instance |
| Instance ID         | `resources.resource_instance_id`   | The ID of the resource instance |
| Plan Name           | `resources.plan_name`              | The name of the plan where the instance was provisioned and rated |
| Plan ID             | `resources.plan_id`                | The ID of the plan where the instance was provisioned and rated |
| Region              | `resources.region`                 | The region where instance was provisioned |
| Consumer ID         | `resources.consumer_id`            | The ID of the consumer |
| Resource Group Name | `resources.resource_group_name`    | The name of the resource group |
| Resource Group ID   | `resources.resource_group_id`      | The ID of the resource group |
| CF Org              | `resources.organization_name`      | The name of the CF organization |
| Org ID              | `resources.organization_id`        | The ID of the CF organization |
| CF Space            | `resources.space_name`             | The name of the CF space |
| Space ID            | `resources.space_id`               | The ID of the CF space|
| Currency            | `resources.currency_code`          | The currency for the cost fields in the resources, plans, and metrics |
| Billable            | `resources.billable`               | Validates if a cost is charged to the account |
| Usage Metric        | `resources.usage.metric`           | ID of the metric |
| Usage Unit          | `resources.usage.unit`             | Unit that qualifies the quantity |
| Usage Quantity      | `resources.usage.quantity`         | Aggregated value for the metric |
| Usage Cost          | `resources.usage.cost`             | Cost incurred by the metric |
| Original Cost       | `resources.usage.rated_cost`       | The starting cost of a resource within your account |
| Pending             | `resources.pending`            | 	Pending charge from classic infrastructure |
| Discount (%)        | `resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID         | `resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
| Non Chargeable  | `resources.usage.non_chargeable` |  When set to `true`, the cost is for informational purpose and is not included while calculating the plan charges. |
| Classic Infrastructure Product ID | `resources.usage.additional_properties.classic_infrastructure_product_id`  | Product ID of classic infrastructure resource |
| Classic Infrastructure Package ID |`resources.usage.additional_properties.classic_infrastructure_package_id` | Package ID of classic infrastructure resource |
| Other Tags          | `resources.tags`                   | Tags that are not of `key:value` format |
{: class="simple-tab-table"}
{: caption="Table 2. Account instance CSV header titles and JSON report fields for account instance usage" caption-side="bottom"}
{: tab-group="account-instance"}
{: #service-name-instance}
{: tab-title="Account Instance Usage"}

For tags that are of `key:value` format, a new column is added for each and every unique `key`, with the `key` as the column name and the `value` as the column value for the corresponding instance usage row. For example, if there are two instances, `i1` and `i2`, with tag `env:prod` on `i1` and tags `env:test` and `team:backend` on `i2`, there would be two additional columns named `env` and `team`. And only the `i1` row will have value `prod` under the `env` column. The `i2` row will have values `test` and `backend` under the `env` and `team` columns. The following table shows the example layout.

| Instance ID | Other tags | `env`  | `team`    |
|-------------|------------|--------|-----------|
| `i1`        |            | `prod` |           |
| `i2`        |            | `test` | `backend` |
{: caption="Table 3. Example of tag layout in the CSV report" caption-side="bottom"}


### Understanding CSV table headings and JSON report fields for enterprise account summary
{: #enterprise-usage-table-account-summary-csv}

The following table shows the correlation between the heading titles in your CSV report and JSON report fields. The usage in the **Enterprise Resource Usage** section is aggregated by each metric of a service plan.

| CSV Header      | Description        |
|--------------------|--------------------|
| Entity ID          | ID of the requested entity (`enterprise_id`/`account_group_id`/`account_id`) |
| Entity Type        | Type of the requested entity (enterprise/account_group/account) |
| Billing Month      | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Currency Rate      | Currency Exchange Rate with USD as the base |
| Created Time       | Timestamp at which the CSV report was generated |
{: class="simple-tab-table"}
{: caption="Table 1.  Enterprise usage report CSV contents for entity metadata" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #entity-metadata}
{: tab-title="Entity Metadata"}

| CSV Header      | Description |
|--------------------|-------------|
| Entity ID          | ID of the hierarchy entity |
| Entity Type        | Type of the hierarchy entity |
| Entity Name        | Name of the hierarchy entity |
| Parent Entity ID   | ID of the parent of this hierarchy entity |
| Parent Entity Name | Name of the parent of the current hierarchy entity |
| Parent Entity Type | Type of the parent of the current hierarchy entity |
| Entity CreatedOn   | Timestamp at which the hierarchy entity was created |
{: class="simple-tab-table"}
{: caption="Table 1.  Enterprise usage report CSV contents for entity hierarchy" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #entity-hierarchy}
{: tab-title="Entity Hierarchy"}

| CSV Header Header          | JSON Report Fields        | Description        |
|------------------------|---------------------------|--------------------|
| Billing Unit ID        | `resources.id`         | The ID of the DEFAULT billing unit of the requested entity, which is a globally unique identifier (GUID) |
| Billing Unit Name      | `resources.name`       | The name of the billing unit |
| Billing Unit CreatedOn | `resources.created_at` | The creation date of the billing unit |
{: class="simple-tab-table"}
{: caption="Table 1. Enterprise usage report CSV contents for billing units" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #billing-unit-id-enterprise}
{: tab-title="Billing Units"}

| CSV Header Header     | JSON Report Fields                        | Description        |
|-------------------|-------------------------------------------|--------------------|
| Credit Pool Type  | `resources.type`                          | The type of credit, either `PLATFORM` or `SUPPORT` |
| Currency Code     | `resources.currency_code`                 | The currency code of the associated billing unit |
| Billing Option ID | `resources.term_credits.billing_option_id`| The ID of the billing option from which the subscription term is derived |
| Category          | `resources.term_credits.category`         | The category of the credit pool. \n For platform credit the valid values are `PLATFORM`, `OFFER`, or `SERVICE` \n For support credit the valid value is `SUPPORT` |
| Start Date        | `resources.term_credits.start_date`       | The start date of the term in ISO format |
| End Date          | `resources.term_credits.end_date`         | The end date of the term in ISO format  |
| Total Credits     | `resources.term_credits.total_credits`    | The total credit available in this term |
| Starting Balance  | `resources.term_credits.starting_balance` | The balance of available credit at the start of the current month |
| Used Credits      | `resources.term_credits.used_credits`     | The amount of credit used during the current month |
| Current Balance   | `resources.term_credits.current_balance`  | The balance of remaining credit in the subscription term |
{: class="simple-tab-table"}
{: caption="Table 1. Enterprise usage report CSV contents for credit pools" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #credit-pool-type-enterprise}
{: tab-title="Credit Pools"}

| CSV Header Header     | JSON Report Fields       | Description        |
|-------------------|--------------------------|--------------------|
| Credit Pool Type  | `resources.type`         | The type of credit, either `PLATFORM` or `SUPPORT` |
| Currency Code     | `resources.currency_code`| The currency code of the associated billing unit |
| Overage           | `resources.overage.cost` | The number of credits that are used as overage |
{: class="simple-tab-table"}
{: caption="Table 1. Enterprise usage report CSV contents for overages" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #overages-enterprise}
{: tab-title="Overages"}

| CSV Header Header      | JSON Report Fields  | Description        |
|--------------------|---------------------|--------------------|
| Entity ID          | `reports.entity_id`         | The ID of the entity |
| Entity Type        | `reports.entity_type`       | The type of the entity  \n Possible values: `enterprise` , `account-group`, or `account` |
| Entity Name        | `reports.entity_name`       | A user-defined name for the entity, such as the enterprise name or account group name |
| Billing Unit ID    | `reports.billing_unit_id`   | The ID of the billing unit  |
| Billing Unit Name  | `reports.billing_unit_name` | The name of the billing unit |
| Country Code       | `reports.country_code`      | The country code of the billing unit |
| Currency Code      | `reports.currency_code`     | The currency code of the billing unit |
| Billable Cost      | `reports.billable_cost`     | Billable charges that are aggregated from all entities in the report |
| Non Billable Cost  | `reports.non_billable_cost` | Non-billable charges that are aggregated from all entities in the report |
{: class="simple-tab-table"}
{: caption="Table 1.  Enterprise usage report CSV contents for enterprise usage summary" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #entity-resource-usage1}
{: tab-title="Enterprise Usage Summary"}

| CSV Header Header    | JSON Report Fields                       | Description        |
|------------------|------------------------------------------|--------------------|
| Entity ID        | `reports.entity_id`                      | The ID of the entity |
| Entity Type      | `reports.entity_type`                    | The type of the entity. \n Possible values: `enterprise`, `account-group`, or `account` |
| Parent Entity ID | `reports.parent_entity_id`               | The ID of the parent of the requested entity |
| Billing Unit ID  | `reports.billing_unit_id`                | The ID of the billing unit  |
| Currency Code    | `reports.currency_code`                  | The currency code of the billing unit |
| Service Name     | `reports.resources.resource_name`        | The name of the resource |
| Service ID       | `reports.resources.resource_id`          | The ID of the resource |
| Billable         | `reports.resources.plans.billable`       | Whether the plan charges are billed to the customer |
| Plan Name        | `reports.resources.plan_name`            | The name of the plan |
| Plan ID          | `reports.resources.plan_id`              | The ID of the plan |
| Pricing Region   | `reports.resources.plans.pricing_region` | The pricing region for the plan |
| Metric           | `reports.resources.plans.usage.metric`   | The name of the metric |
| Unit             | `reports.resources.plans.usage.unit`     | A unit to qualify the quantity |
| Quantity         | `reports.resources.plans.usage.quantity` | The aggregated value for the metric |
| Cost             | `reports.resources.plans.usage.cost`     | The cost that was incurred by the metric |
| Pending          | `reports.resources.plans.pending`        | Pending charge from classic infrastructure |
{: class="simple-tab-table"}
{: caption="Table 1. Enterprise usage report CSV contents for enterprise resource usage" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #entity-resource-usage2}
{: tab-title="Enterprise Resource Usage"}

The following are the JSON report section APIs for the different CVS headings:

* Billing Units: [Enterprise Billing Units: List billing units](/apidocs/enterprise-apis/billing-unit#list-billing-units){: external}
* Credit Pools and Overages: [Enterprise Billing Units: Get credit pools](/apidocs/enterprise-apis/billing-unit#get-credit-pools){: external}
* Enterprise Usage Summary and Enterprise Resource Usage: [Enterprise Usage Reports API: Get usage reports for enterprise entities](/apidocs/enterprise-apis/resource-usage-reports#get-resource-usage-report-csv){: external}

<!--
When `recurse=true`, the usage in the **Enterprise Resource Usage** section is aggregated by each metric of a service plan and it's broken down by child accounts. Each row represents the total usage of a service plan metric in some child account. When `recurse=false`, the usage is aggregated by each metric of a service plan and each row represents the total usage of a service plan metric of all the sub-accounts or child-accounts in the requested entity hierarchy. In the Hierarchy section, `recurse=true` shows all the child entities of the requested entity, and for `recurse=false`, it shows only the direct children of the requested entity.
{: note} -->
