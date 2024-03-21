---
copyright:
  years: 2022, 2024
lastupdated: "2024-03-21"


keywords: carbon calculator, cloud carbon calculator, emission calculator, carbon footprint, sustainability, FAQs

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Working with {{site.data.keyword.Bluemix_notm}}'s carbon calculator
{: #what-is-cloud-calc}

Output that is provided by the carbon calculator is provided “as-is” for informational purposes only, and is based on cloud services information that is provisioned by client in client’s {{site.data.keyword.cloud_notm}} account. Output is provided in a format according to GHG protocol standards. The data sources and tools that are used to calculate client's emissions are subject to change by IBM without notice. The client is responsible for confirming the accuracy of any calculator output for purposes of client’s compliance with any applicable regulatory obligations or for any other purpose.
{: important}

{{site.data.keyword.cloud_notm}}'s carbon calculator displays the carbon emissions for an account by monitoring your electricity consumption for services, resources, and the location and efficiency of your data centers. Tracking your carbon emissions is important so that you can know how much carbon emissions your account is associated with, and it helps you manage and mitigate your carbon footprint over time.

If service data is not displaying, it may be because emissions data is currently tracked for a subset of services, data for newly added services and current quarter results are not yet available because it can take roughly two months to populate, or some service instances might be running on [zero-emissions data centers](#zero-emission-data-centers).
{: note}

Emissions data is currently tracked for a subset of services, but more services are under consideration to be added. Emission data is currently available for the following services:

* {{site.data.keyword.iae_short}}                               <!--Analytics Engine-->
* {{site.data.keyword.appconfig_short}}                         <!--App Configuration-->
* Application Load Balancer                                     <!--Application Load Balancer-->
* {{site.data.keyword.bm_is_short}}                             <!--Bare Metal Servers for VPC-->
* {{site.data.keyword.baremetal_short}} for Classic             <!--Bare Metal Servers for Classic-->
* {{site.data.keyword.blockstorageshort}}                       <!--Block Storage for Classic-->
* {{site.data.keyword.block_storage_is_short}}                  <!--Block Storage for VPC-->
* Cloud HSM                                                     <!--Cloud HSM-->
* Cloud Object Storage                                          <!--Cloud Object Storage-->
* Cloudant                                                      <!--Cloudant-->
* {{site.data.keyword.registryshort}}                           <!--Container Registry-->
* {{site.data.keyword.contdelivery_short}}                      <!--Continuous Delivery-->
* Data Engine (previously SQL Query)                            <!--Data Engine-->
* {{site.data.keyword.databases-for-elasticsearch}}             <!--Databases for Elasticsearch-->
* {{site.data.keyword.databases-for-enterprisedb}}              <!--Databases for EnterpriseDB-->
* {{site.data.keyword.databases-for-etcd}}                      <!--Databases for etcd-->
* {{site.data.keyword.databases-for-mongodb}}                   <!--Databases for MongoDB-->
* {{site.data.keyword.databases-for-mysql}}                     <!--Databases for MySQL-->
* {{site.data.keyword.databases-for-postgresql}}                <!--Databases for PostgreSQL-->
* {{site.data.keyword.databases-for-redis}}                     <!--Databases for Redis-->
* {{site.data.keyword.datastageshort}}                          <!--DataStage-->
* Db2                                                           <!--Db2-->
* Db2 Warehouse                                                 <!--Db2 Warehouse-->
* Direct Link Connect                                           <!--Direct Link Connect-->
* Direct Link Dedicated                                         <!--Direct Link Dedicated-->
* {{site.data.keyword.dns_short}}                               <!--DNS Services-->
* {{site.data.keyword.en_short}}                                <!--Event Notifications-->
* {{site.data.keyword.messagehub}}                              <!--Event Streams-->
* {{site.data.keyword.filestorage_short}}                       <!--File Storage for Classic-->
* {{site.data.keyword.filestorage_vpc_short}}                   <!--File Storage for VPC-->
* {{site.data.keyword.fsa10_full}}                              <!--Fortigate Security Appliance 10 Gbps-->
* Gateway Appliance                                             <!--Gateway Appliance-->
* IBM Cloud Activity Tracker                                    <!--IBM Cloud Activity Tracker-->
* IBM Cloud Monitoring                                          <!--IBM Cloud Monitoring-->
* IBM Cloud Platform - Core Services [^tabletext1]              <!--IBM Cloud Platform - Core Services-->
* IBM Log Analysis                                              <!--IBM Log Analysis-->
* {{site.data.keyword.keymanagementserviceshort}}               <!--Key Protect-->
* {{site.data.keyword.containershort_notm}}                     <!--Kubernetes Service-->
* {{site.data.keyword.loadbalancer_short}} for Classic          <!--Load Balancer for Classic-->
* {{site.data.keyword.messages-for-rabbitmq}}                   <!--Messages for RabbitMQ-->
* MQ                                                            <!--MQ-->
* Network Load Balancer                                         <!--Network Load Balancer-->
* SAP on Classic Infrastructure                                 <!--SAP on Classic Infrastructure-->
* SAP on VMware                                                 <!--SAP on VMware-->
* {{site.data.keyword.satelliteshort}}                          <!--Satellite-->
* {{site.data.keyword.secrets-manager_short}}                   <!--Secrets Manager-->
* {{site.data.keyword.compliance_short}}                        <!--Security and Compliance Center-->
* Security and Compliance Center Workload Protection            <!--Security and Compliance Center Workload Protection-->
* {{site.data.keyword.tg_short}}                                <!--Transit Gateway-->
* VMware Solutions                                              <!--VMware Solutions-->
* {{site.data.keyword.vpn_vpc_short}}                           <!--VPN for VPC-->
* {{site.data.keyword.virtualmachinesshort}} for Classic        <!--Virtual Servers for Classic-->
* Virtual Server for VPC                                        <!--Virtual Server for VPC-->

[^tabletext1]: Contains multiple services that are not tracked individually but are combined into one service. IBM Cloud Platform includes the following: Command line interface, Billing and usage, Identity and access management, Global catalog, Global search & tagging, Console, Cloud shell, Projects, Paywall, Schematics, and Carbon calculator.


All service workloads across all sites are metered for electricity consumption or estimations based on hardware profiles. Service usage is also tracked by account, location, and over time. Data is then processed to produce a standards-based carbon emission estimate for each account per service, per location, and resource group. {{site.data.keyword.cloud_notm}} has a resilient global network of locations to host data center workloads and provides three tiers of regions: multizone regions, single-campus multizone regions, and data centers. For more information, see [IBM Cloud global data centers](https://www.ibm.com/cloud/data-centers){: external}.

The carbon calculator provides a wide range of features to track your carbon emissions:

* View total emissions by service, resource group, and location.
* View total emissions for an enterprise account.
* Filter emissions data by time period, service, or location.
* Best practices for cloud sustainability.
* Export data as a CSV file for additional analyses.
* View emissions data by using [the API](/apidocs/carbon-calculator).

## Before you begin
{: #carbon-calc-prereq}

Account owners, account administrators, and users with a viewer role or higher on the billing service can view and export emissions data for the entire account. An account or billing administrator role is required to grant other users access to the Billing service. For more information about assigning access, see [Assigning access to account management services](/docs/account?topic=account-account-services&interface=api#billing-acct-mgmt-api).

<!--To view emissions data, you must be assigned the viewer or higher role on the billing service. Your account must be open for a minimum of 31 days. and the average monthly usage over a span of three months must be higher than $250 USD. If you have a free account or your average usage is less than $250 USD, {{site.data.keyword.cloud_notm}} might require two or more cloud services in the same location to calculate and show emissions data.-->

## IBM Cloud and sustainability
{: #cc-sustainability}

As organizations and users work together to achieve better outcomes for their business and for the environment, digital technologies are a growing source of carbon emissions. There are four areas that are the main source for carbon emissions: data centers, big data analytics, security, and internet usage. For more information about sustainability, see [IT sustainability beyond the data center](https://www.ibm.com/thought-leadership/institute-business-value/report/it-sustainability){: external}.

One use case strategy for sustainability involves ESG reporting, which uses environmental, social, and governance reporting to integrate data silos. For more information, explore [IBM Envizi](https://www.ibm.com/products/envizi){: external}.

## IBM Cloud carbon calculator methodology
{: #carbon-methodology}

{{site.data.keyword.cloud_notm}} plays a critical role for achieving {{site.data.keyword.IBM_notm}}’s energy conservation, renewable electricity procurement, and greenhouse gas (GHG) emissions reduction targets. {{site.data.keyword.cloud_notm}} is improving the estimation approach by introducing the carbon calculator, which gives you a detailed view of your cloud electricity consumption and associated GHG emissions.

{{site.data.keyword.cloud_notm}}'s carbon calculator uses data from electricity consumption, server resource utilization measurements, server and process life-cycle events, and service usage data. Based on the data, it estimates the electricity consumption and carbon emission from each account and service offering, according to the location, time period, and resource groups.

{{site.data.keyword.cloud_notm}} has a resilient global network of locations to host data center workloads and provides three tiers of regions: multizone regions, single-campus multizone regions, and data centers.

The calculation method depends on the gross electricity consumption and carbon emissions factor per location. It allocates a portion of the electricity consumption to each one of the services in a location based on the physical hosts that are being used. Then, it splits the electricity consumption per service, per location, across the tenants that are using the service based on their respective usage metrics. For Classic Infrastructure services, energy consumption is calculated by using the average power consumption for the machine on which the server is running.

Due to the large number of flexible profiles associated with Bare Metal for Classic, profiles were onboarded in phases. Complete data is available from December 2023 on. Users requiring a complete emissions report for previous months can submit a support case requesting a manual calculation. When creating a support case, select the **Billing and usage** topic. For more information, see [Creating support cases](https://cloud.ibm.com/docs/get-support?topic=get-support-open-case).
{: note}

The method uses the service units of individual {{site.data.keyword.cloud_notm}} offerings to allocate electricity consumption of shared resources to a service's individual resources. The per-account electricity consumption is multiplied by the location’s Power Usage Effectiveness (PUE) and carbon emission factor to yield the accounts carbon footprint.

The goal of the calculation method is to associate electricity consumption and carbon footprint allocation for the following:

* Per client account
* Per client account and cloud service used
* Per client account, cloud service, and location where the service is running
* Per client account and Resource Group

For a more in depth explanation about carbon calculators methodology and calculations, see [Energy and carbon quantification methodology](https://cloud.ibm.com/media/docs/downloads/billing-usage/carbon-calc-method-v2.pdf){: external}.


## Tracking account emissions with carbon calculator
{: #tracking-emissions-account}

To view emissions data for your account, you must be assigned the viewer or higher role on the billing service to view and export the emissions data for the entire account. An account or billing administrator role is required to grant other users access to the Billing service. For more information about assigning access, see [Assigning access to account management services](/docs/account?topic=account-account-services&interface=api#billing-acct-mgmt-api).

Emissions from key greenhouse gases are measured in metric tons of carbon dioxide-equivalent (kgCO~2~e). You can view your account's emissions data in the {{site.data.keyword.cloud_notm}} console. Go to **Manage** > **Billing and Usage** > **Carbon Calculator** to view the following widgets:

* Total emissions: The total emissions are calculated by comparing the energy-related usage with data center energy sources. You can download the total emissions data in CSV format.

* Emissions by location: The energy consumption is calculated by using usage units such as CPU. Two or more resources are required to display the location data. The size represents how much energy is generated and the color represents the carbon intensity that is the emission rate for grams of carbon dioxide-equivalent emissions that are released per unit of energy produced.

* Emissions by service: The carbon emissions are broken down by service.

* Emissions by resource group: The carbon emissions are broken down by group. Most services are displayed by resource group. However, Classic Infrastructure is displayed in a dedicated group. The emissions are displayed only if a group contains those services.


## Tracking enterprise emissions with carbon calculator
{: #tracking-emissions-enterprise}
​
The enterprise level view of carbon calculator enables you to view and export emissions data for your entire enterprise account. You must be assigned the `Usage report viewer` role on the enterprise service in the enterprise parent account in order to view and export the emissions data at the enterprise level. For more information about assigning access, see [Assigning access to account management services](/docs/account?topic=account-account-services&interface=api#billing-acct-mgmt-api).

In the enterprise level view, you can filter your emissions data down to a specific account group or account by clicking that entity in the account hierarchy. The enterprise view provides two additional widgets:
​
* Emissions by account group: Carbon emissions broken down by account group. This displays if the entity being viewed contains account groups. Emissions listed under "Miscellaneous" do not belong to an account group.
​
* Emissions by account: Carbon emissions broken down by account. This will display if the entity being viewed contains only accounts.
​
Learn more about setting up and managing [Enterprise accounts](/docs/secure-enterprise?topic=secure-enterprise-what-is-enterprise).
​

## Working with the carbon calculator API
{: #tracking-emissions-api}
​
Users can pull emissions data or incorporate that data into their own applications and processes by leveraging the [Carbon Calculator API](/apidocs/carbon-calculator).

## Zero-emissions data centers
{: #zero-emission-data-centers}

The following table shows the locations that are considered to be zero-emissions data centers for 2024. Data centers are considered zero-emissions either because they are powered by renewable energy or because their greenhouse gas emissions have been offset with certificates. Additional data centers may be added periodically.

| Data Center | Location      |
|-------------|---------------|
| DAL02	      | Dallas        |
| DAL06       | Dallas        |
| DAL10	      | Dallas        |
| DAL12	      | Dallas        |
| DAL13	      | Dallas        |
| MON01       |	Montreal      |
| SAO01       |	Sao Paulo     |
| SAO04       | Sao Paulo     |
| SAO05       |	Sao Paulo     |
| WDC04       | Washington DC |
| WDC06       | Washington DC |
| WDC07       | Washington DC |
{: caption="Table 1. Carbon intensity of data centers in North and South America" caption-side="bottom"}
{: #americas}
{: tab-title="Americas"}
{: tab-group="carbon-intesity"}
{: class="simple-tab-table"}

| Data Center | Location      |
|-------------|---------------|
| AMS01	      | Amsterdam     |
| AMS03	      | Amsterdam     |
| FRA02	      | Frankfurt     |
| FRA04	      | Frankfurt     |
| FRA05	      | Frankfurt     |
| LON02	      | London        |
| LON04	      | London        |
| LON05	      | London        |
| LON06	      | London        |
| MAD02	      | Madrid        |
| MAD04       | Madrid        |
| MAD05       | Madrid        |
| MIL01       |	Milan         |
| PAR01       | Paris         |
| PAR04       | Paris         |
{: caption="Table 1. Carbon intensity of data centers in Europe" caption-side="bottom"}
{: #europe}
{: tab-title="Europe"}
{: tab-group="carbon-intesity"}
{: class="simple-tab-table"}

| Data Center | Location      |
|-------------|---------------|
| OSA22       |	Osaka	        |
{: caption="Table 1. Carbon intensity of data centers in Asia Pacific" caption-side="bottom"}
{: #asia-pacific}
{: tab-title="Asia Pacific"}
{: tab-group="carbon-intesity"}
{: class="simple-tab-table"}

Carbon intensity is the emission rate for grams of carbon dioxide-equivalent emissions that are released per unit of energy produced.
{: note}
