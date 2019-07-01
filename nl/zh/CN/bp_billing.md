---

copyright:
  years: 2019
lastupdated: "2019-06-18"

keywords: best practice billing, best practice usage, automate billing, track costs

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 计费和使用情况最佳做法
{: #best-practices}

关注我们在 {{site.data.keyword.Bluemix}} 中跟踪成本和自动计费的最佳做法。
{:shortdesc}


## 通过添加标记跟踪相关资源的成本
{:#track-billing-tags}

将标记添加到资源以组织、跟踪和管理相关资源的成本。当您使用一致的标记模式来识别哪些资源与特定项目相关时，您可以在导出的使用报告中分析成本时按标记分组和过滤。

1. 使用一致的标记模式（例如创建标记以区分成本中心、数据中心、项目或团队）来标记资源。要添加标记，请单击“菜单”图标 ![“菜单”图标](../icons/icon_hamburger.svg) > **资源列表**。在“标记”列中，为要进行标记的每个资源单击**添加标记**。

   使用“键:值”对添加标记，以根据使用情况报告中的键添加定制列。根据用于组织资源的类别创建键，例如使用 `costcenter:` 以按成本中心分组，或使用 `project:` 以按项目分组。
   {: tip}

   例如，您可能具有用于单个帐户中的两个项目（项目 ABC 和项目 XYZ）的资源。项目 ABC 具有一个 {{site.data.keyword.containershort_notm}} 集群、一些 Cloud Foundry 应用程序部署和一个 {{site.data.keyword.cloudant_short_notm}} 数据库。您可以将 `project:abc` 标记添加到所有这些资源，以将项目 ABC 的这些资源与项目 XYZ 中标记为 `project:xyz` 的类似资源区分开来。

   有关添加和使用标记的更多信息，请参阅[使用标记](/docs/resources?topic=resources-tag)。

1. 通过导出实例的使用情况报告来跟踪已标记资源的成本。要导出报告，请转至**管理 > 计费和使用情况**，并选择**使用情况**。然后，单击**导出 CSV > 实例**。

   使用实例 CSV 文件中的“标记”列来帮助分析帐户中的资源。您可以根据每个实例上的项目标记对 CSV 数据分类，以便您可以更好地分析单个项目的成本。如果您使用“键:值”对标记了资源，那么您还将在使用情况报告中看到与键对应的列。例如，标记为 `project:abc` 的资源和标记为 `project:xyz` 的资源在“项目”列中分别显示为“abc”和“xyz”。

   有关更多信息，请参阅[查看使用情况](/docs/billing-usage?topic=billing-usage-viewingusage)。

## 使用 CLI 或 API 进行自动记帐和使用情况管理
{: #billing-cli-apis}

如果您想要自动化资源使用情况和任何相关成本的查阅方式，可以使用 [`ibmcloud billing`](/docs/cli?topic=cloud-cli-ibmcloud_billing) CLI 或[使用情况计量 ![外部链接图标](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/usage-metering){: new_window} 和[使用情况报告 ![外部链接图标](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/metering-reporting){: new_window} API 来将此功能集成到您自己的应用程序中。

要开始使用这些 API，请设置 [{{site.data.keyword.Bluemix_notm}} 使用情况样本仪表板 ![外部链接图标](../icons/launch-glyph.svg)](https://github.com/IBM-Cloud/openwhisk-cloud-usage-sample){: new_window}。使用 {{site.data.keyword.openwhisk}}，样本实现了 API 驱动的方法来获取和可视化 {{site.data.keyword.Bluemix_notm}} 使用情况和计费数据。
{: tip}
