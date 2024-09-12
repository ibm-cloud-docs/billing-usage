---

copyright:
  years: 2024

lastupdated: "2024-09-11"

keywords:

subcollection: billing-usage

content-type: conref

---

{{site.data.keyword.attribute-definition-list}}

# Content references for billing-usage subcollection
{: #conref-billing}

Reuse sections within the billing-usage repo.
{: shortdesc}
{: #my-shortdesc-reuse}

H1's would never be able to be reused. Each Markdown file can only ever have one H1. However, any H2-H6 can be fully reused.


### Tracking usage for service-level commitments
{: #SLC-usage}

To view usage for an on-premises resource, like {{site.data.keyword.powerSys_notm}} Private Cloud, filter the **Pricing region** column to the {{site.data.keyword.satelliteshort}} location associated with your pod. Then, filter the **Service name** column to {{site.data.keyword.powerSys_notm}}.

Map commitment usage in your enterprise back to child accounts by completing the following steps:

1. Go to the **Entity ID** column and filter on an account ID.
1. Go to the **Service name** column and filter on the service that is associated with your commitment. The sum of the **Cost** column gives you this month's usage towards a service-level commitment in a specific account.
