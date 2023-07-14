---

copyright:
  years: 2023
lastupdated: "2023-07-12"

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

You might not be able to view your accounts emissions data because you don't have the right access or the service doesn't have enough data. For access, account owners, account administrators, and users with a viewer role or higher on the billing service can view and export emissions data for the entire account. Supported services must have at least 30 days of data to be viewed on the carbon calculator.

<!--If you have the right access and still can't view data, there's some minimum requirements that your account needs. To view emissions data your account must be open for a minimum of 31 days and monthly usage must be higher than $250 USD. If you have a free account or your usage is less than $250 USD, {{site.data.keyword.cloud_notm}} might require a minimum number of service types to calculate and show emissions data.-->

If you're still having issues viewing data, [create a support case](/unifiedsupport/cases/form) in the {{site.data.keyword.cloud_notm}} Support Center.

## How do you calculate the emissions?
{: #calculate-emissions}
{: faq}

The total emissions are calculated by comparing the energy-related usage with data center energy sources. Emissions from key greenhouse gases are measured in metric tons of carbon dioxide-equivalent (kgCO~2~e). You can download the total emissions data in CSV format. View the total emissions widget on the [Carbon Calculator](/billing/carbon-calculator) page in the console.


## Can I view emissions for all services on my account?
{: #service-emissions}
{: faq}

Carbon Calculator has emission data for the following services:

* Bare Metal Servers for Classic
* Bare Metal Servers for VPC
* Cloud HSM
* Cloud Object Storage
* FortiGate Security Appliance 10Gbps
* Kubernetes Service
* Load Balancers for Classic
* Virtual Server for Classic
* Virtual Server for VPC
<!--* Block Storage for Classic - released planned for 7/17-->
<!--* Block Storage for VPC - released planned for 7/17-->
<!--* DNS Services - release planned for 7/17-->
<!--* File Storage for Classic - released planned for 7/17-->
<!--* File Storage for VPC - released planned for 7/17-->
<!--* Load Balancer for VPC (Application) - release planned for 7/17-->
<!--* Load Balancer for VPC (Network) - release planned for 7/17-->
<!--* VPN for VPC - released planned for 7/17-->

More services are under consideration to be added to the carbon calculator. After a service is added, it takes 30 days to collect and show data.
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

## Can I view emission data for enterprise accounts?
{: #enterprise-data}
{: faq}

Yes. You can view emission data for your enterprise, account groups, and child accounts by logging into your enterprise's parent account and navigating from the {{site.data.keyword.cloud_notm}} console and go to Go to **Manage** > **Billing and Usage** > **Carbon Calculator**.
