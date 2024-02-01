---

copyright:
  years: 2023, 2024
lastupdated: "2024-02-01"

keywords: carbon calculator, cloud carbon calculator, emission calculator, carbon footprint, sustainability, FAQs

subcollection: billing-usage

content-type: faq

---

{{site.data.keyword.attribute-definition-list}}

# FAQs for IBM Cloud Carbon Calculator
{: #carboncalcfaqs}

## Why can't I see my emissions data?
{: #carboncalc-emissions}
{: faq}

You might not be able to view your accounts emissions data because you don't have the correct access or the service doesn't have enough data. For access, account owners, account administrators, and users with a viewer role or higher on the billing service can view and export emissions data for the entire account. Supported services must have at least 30 days of data to be viewed on the carbon calculator.

<!--If you have the correct access and still can't view data, there's some minimum requirements that your account needs. To view emissions data your account must be open for a minimum of 31 days and monthly usage must be higher than $250 USD. If you have a free account or your usage is less than $250 USD, {{site.data.keyword.cloud_notm}} might require a minimum number of service types to calculate and show emissions data.-->

If you're still having issues viewing data, [create a support case](/unifiedsupport/cases/form) in the {{site.data.keyword.cloud_notm}} Support Center.

## How do you calculate the emissions?
{: #calculate-emissions}
{: faq}

The total emissions are calculated by comparing the energy-related usage with data center energy sources. Emissions from key greenhouse gases are measured in metric tons of carbon dioxide-equivalent (kgCO~2~e). You can download the total emissions data in CSV format. View the total emissions widget on the [Carbon Calculator](/billing/carbon-calculator) page in the console.


## Can I view emissions for all services on my account?
{: #service-emissions}
{: faq}

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
* Db2 Warehouse                                                 <!--Db2 Warehouse-->
* {{site.data.keyword.dns_short}}                               <!--DNS Services-->
* {{site.data.keyword.en_short}}                                <!--Event Notifications-->
* {{site.data.keyword.messagehub}}                              <!--Event Streams-->
* {{site.data.keyword.filestorage_short}}                       <!--File Storage for Classic-->
* {{site.data.keyword.filestorage_vpc_short}}                   <!--File Storage for VPC-->
* {{site.data.keyword.fsa10_full}}                              <!--Fortigate Security Appliance 10 Gbps-->
* Gateway Appliance                                             <!--Gateway Appliance-->
* IBM Cloud Activity Tracker                                    <!--IBM Cloud Activity Tracker-->
* IBM Cloud Monitoring                                          <!--IBM Cloud Monitoring-->
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
* VMware Solutions                                              <!--VMware Solutions-->
* {{site.data.keyword.vpn_vpc_short}}                           <!--VPN for VPC-->
* {{site.data.keyword.virtualmachinesshort}} for Classic        <!--Virtual Servers for Classic-->
* Virtual Server for VPC                                        <!--Virtual Server for VPC-->

Because emissions are reported after the close of each billing cycle, data for newly added services and current quarter results take about two months to populate.
{: note}

## How do I use this data with Envizi or other third party ESG reporting tools?
{: #emission-tools}
{: faq}

IBM Envizi is a robust data management foundation that is designed to create a single, trusted data source for all your ESG reporting and opportunity identification. Use ESG reporting to meet compliance and reporting requirements. For more information, see [IBM Envizi ESG Suite](https://www.ibm.com/products/envizi){: external}.

Envizi integration currently requires creation of a custom connector. Reach out to your {{site.data.keyword.cloud_notm}} representative for more information.

## How do I submit feedback on Carbon Calculator?
{: #cc-feedback}
{: faq}

Talk to your CSM or create case on support center. When you open a support casae, choose billing and usage topics and subtopics, but specify carbon calculator in case description.

<!--## Why can’t I see my data from previous years?
{: #available-data}
{: faq}

Carbon Calculator data is currently available from 2022.-->

## How do I view the carbon intensity of my data center?
{: #carbon-intensity}
{: faq}

In the carbon calculator, on the locations widget, you can hover over the location of their data center to see carbon intensity.

<!--
## Can I view emission data for enterprise accounts?
{: #enterprise-data}
{: faq}

Yes. You can view emission data for your enterprise, account groups, and child accounts by logging into your enterprise's parent account and navigating from the {{site.data.keyword.cloud_notm}} console and go to Go to **Manage** > **Billing and Usage** > **Carbon Calculator**.-->
