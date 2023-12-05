---
copyright:
  years: 2022, 2023
lastupdated: "2023-12-05"


keywords: carbon calculator, cloud carbon calculator, emission calculator, carbon footprint, sustainability, FAQs

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Working with {{site.data.keyword.Bluemix_notm}}'s carbon calculator
{: #what-is-cloud-calc}

Output that is provided by the carbon calculator is provided “as-is” for informational purposes only, and is based on cloud services information that are provisioned by client in client’s {{site.data.keyword.cloud_notm}} account. Output is provided in a format according to GHG protocol standards. The data sources and tools used to calculate client's emissions are subject to change by IBM without notice. Client is responsible for confirming accuracy of any calculator output for purposes of client’s compliance with any applicable regulatory obligations or for any other purpose.
{: important}

{{site.data.keyword.cloud_notm}}'s carbon calculator displays the carbon emissions for an account by monitoring your electricity consumption for services, resources, and the location and efficiency of your data centers. Tracking your carbon emissions is important so that you can know how much carbon emissions your account is associated with, and it helps you manage and mitigate your carbon footprint over time.

Emissions data is currently tracked for a subset of services, but more services are under consideration to be added. Emission data is currently available for the following services:

* {{site.data.keyword.appconfig_short}}
* Application Load Balancer
* {{site.data.keyword.bm_is_short}}
* {{site.data.keyword.baremetal_short}} for Classic
* {{site.data.keyword.blockstorageshort}}
* {{site.data.keyword.block_storage_is_short}}
* Cloud HSM
* Cloud Object Storage
* {{site.data.keyword.dns_short}}
* {{site.data.keyword.databases-for-elasticsearch}}
* {{site.data.keyword.databases-for-enterprisedb}}
* {{site.data.keyword.databases-for-etcd}}
* {{site.data.keyword.databases-for-mongodb}}
* {{site.data.keyword.databases-for-mysql}}
* {{site.data.keyword.databases-for-postgresql}}
* {{site.data.keyword.databases-for-redis}}
* {{site.data.keyword.en_short}}
* {{site.data.keyword.messagehub}}
* {{site.data.keyword.filestorage_short}}
* {{site.data.keyword.filestorage_vpc_short}}
* {{site.data.keyword.fsa10_full}}
* {{site.data.keyword.keymanagementserviceshort}}
* {{site.data.keyword.containershort_notm}}
* {{site.data.keyword.loadbalancer_short}} for Classic
* Load Balancer for VPC
* {{site.data.keyword.messages-for-rabbitmq}}
* Network Load Balancer
* SAP on Classic Infrastructure
* SAP on VMware
* {{site.data.keyword.secrets-manager_short}}
* VMware Solutions
* {{site.data.keyword.vpn_vpc_short}}
* {{site.data.keyword.virtualmachinesshort}} for Classic
* Virtual Server for VPC


Because emissions are reported after the close of each billing cycle, data for newly added services and current quarter results take about two months to populate.
{: note}

The carbon calculator provides a wide range of features to track your carbon emissions:

* View total emissions by service, resource group, and location.
* Filter emissions data by time period, service, or location.
* Best practices for cloud sustainability.
* Export data as a CSV file for additional analyses

All service workloads across all sites are metered for electricity consumption or estimations based on hardware profiles. Service usage is also tracked by account, location, and over time. Data is then processed to produce a standards-based carbon emission estimate for each account per service, per location, and resource group.


## Before you begin
{: #carbon-calc-prereq}

Account owners, account administrators, and users with a viewer role or higher on the billing service can view and export emissions data for the entire account. An account or billing administrator role is required to grant other users access to the Billing service. For more information about assigning access, see [Assigning access to account management services](/docs/account?topic=account-account-services&interface=api#billing-acct-mgmt-api).

<!--To view emissions data, you must be assigned the viewer or higher role on the billing service. Your account must be open for a minimum of 31 days. and the average monthly usage over a span of three months must be higher than $250 USD. If you have a free account or your average usage is less than $250 USD, {{site.data.keyword.cloud_notm}} might require two or more cloud services in the same location to calculate and show emissions data.-->

## IBM Cloud and sustainability
{: #cc-sustainability}

As organizations and users work together to achieve better outcomes for their business and for the environment, digital technologies are a growing source of carbon emissions. There are four areas that are the main source for carbon emissions: data centers, big data analytics, security, and internet usage. For more information about sustainability, see [IT sustainability beyond the data center](https://www.ibm.com/thought-leadership/institute-business-value/report/it-sustainability){: external}.

One use case strategy for sustainability involves ESG reporting, which uses environmental, social, and governance reporting to integrate data silos. For more information, explore [IBM Envizi](https://www.ibm.com/products/envizi){: external}.

## IBM Cloud Carbon Calculator methodology
{: #carbon-methodology}

{{site.data.keyword.cloud_notm}} plays a critical role for achieving {{site.data.keyword.IBM_notm}}’s energy conservation, renewable electricity procurement, and greenhouse gas (GHG) emissions reduction targets. {{site.data.keyword.cloud_notm}} is improving the estimation approach by introducing the carbon calculator, which gives you a detailed view of your cloud electricity consumption and associated GHG emissions.

{{site.data.keyword.cloud_notm}}'s carbon calculator uses data from electricity consumption, server resource utilization measurements, server and process life-cycle events, and service usage data. Based on the data, it estimates the electricity consumption and carbon emission from each account and service offering, according to the location, time period, and resource groups.

{{site.data.keyword.cloud_notm}} has a resilient global network of locations to host data center workloads and provides three tiers of regions: multizone regions, single-campus multizone regions, and data centers.

The calculation method depends on the gross electricity consumption and carbon emissions factor per location. It allocates a portion of the electricity consumption to each one of the services in a location based on the physical hosts that are being used. Then, it splits the electricity consumption per service, per location, across the tenants that are using the service based on their respective usage metrics.

The method uses the service units of individual {{site.data.keyword.cloud_notm}} offerings to allocate electricity consumption of shared resources to a service's individual resources. The per-account electricity consumption is multiplied by the location’s Power Usage Effectiveness (PUE) and carbon emission factor to yield the accounts carbon footprint.

The goal of the calculation method is to associate electricity consumption and carbon footprint allocation for the following:

* Per client account
* Per client account and cloud service used
* Per client account, cloud service, and location where the service is running
* Per client account and Resource Group

For more in depth explanation about carbon calculators methodology and calculations, see [Energy and carbon quantification methodology](https://cloud.ibm.com/media/docs/downloads/billing-usage/carbon-calc-method.pdf){: external}.

## Tracking your emissions with Carbon Calculator
{: #tracking-emissions-widget}

Emissions from key greenhouse gases are measured in metric tons of carbon dioxide-equivalent (kgCO~2~e). You can view your account's emissions data in the {{site.data.keyword.cloud_notm}} console. Go to **Manage** > **Billing and Usage** > **Carbon Calculator** to view the following widgets:

<!--If you have an enterprise account, you can view emission data for your enterprise, account groups, and child accounts by logging in to your enterprise's parent account.
{: note}-->

* Total emissions: The total emissions are calculated by comparing the energy-related usage with data center energy sources. You can download the total emissions data in CSV format.

* Emissions by location: The energy consumption is calculated by using usage units such as CPU. Two or more resources are required to display the location data. The size represents how much energy is generated and the color represents the carbon intensity that is the emission rate for grams of carbon dioxide-equivalent emissions that are released per unit of energy produced.

* Emissions by service: The carbon emissions are broken down by service.

* Emissions by resource group: The carbon emissions are broken down by group. Most services are displayed by resource group. However, Cloud Foundry is displayed by organization, and Classic Infrastructure is displayed in a dedicated group. The emissions are displayed only if a group contains those services.

You must be assigned the viewer or higher role on the billing service to view and export the emissions data for the entire account. An account or billing administrator role is required to grant other users access to the Billing service. For more information about assigning access, see [Assigning access to account management services](/docs/account?topic=account-account-services&interface=api#billing-acct-mgmt-api).
{: note}
