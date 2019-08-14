---

copyright:
  years: 2019
lastupdated: "2019-07-26"

keywords: enterprise usage, view enterprise costs, account group usage, account usage, cost recovery, chargeback, support cost

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:external: target="_blank" .external}
{:note: .note}


# 查看企业中的使用情况
{: #enterprise-usage}

您可以通过查看 {{site.data.keyword.Bluemix}} 企业中帐户的使用情况，跟踪这些帐户中的资源和支持成本。可以查看其使用情况的帐户和帐户组取决于分配给您的访问权。
{: shortdesc}

通过 {{site.data.keyword.Bluemix_notm}} 企业，您能够集中管理多个 {{site.data.keyword.Bluemix_notm}} 帐户。作为企业用户，您可以关注企业中任何帐户的资源使用情况以及关联成本。请参阅[什么是企业？](/docs/account?topic=account-enterprise)。


## 查看企业使用情况所必需的访问权
{: #enterprise-usage-access}

在企业中，对使用情况信息的访问权由企业服务进行控制。要使用户能够查看使用情况信息，必须邀请用户加入企业帐户，并使其具有对企业服务的使用情况报告查看者、编辑者或管理员角色。使用情况报告查看者角色仅提供查看使用情况报告的访问权，而编辑者和管理员角色还支持其他企业管理操作。为了与安全性最佳实践保持一致，请为用户分配完成其任务所需的最少数量的访问权。有关更多信息，请参阅[企业操作和角色](/docs/iam?topic=iam-account-services#enterprise-account-management)。

您可以授予用户粒度访问权，以便他们可以查看特定帐户或帐户组的使用情况。例如，假设企业有针对每个部门的帐户组，每个部门有针对每个团队的帐户组。您可以限定访问权的作用域，以便每个企业用户只能查看履行其工作角色所需的信息。
   * 财务管理人员需要查看整个企业的使用情况，以便能够跟踪和回收每个部门的成本，但他们不需要创建帐户或帐户组。因此，为财务管理人员分配对企业的使用情况报告查看者角色。
   * 每个部门负责人需要查看其部门的使用情况，还需要为其团队创建和管理帐户和帐户组。因此，为每个部门负责人分配对其部门的帐户组的编辑者角色。
   * 每个团队负责人需要查看其团队的使用情况，但您希望他们向团队添加新帐户时获得部门批准。因此，为每个团队负责人分配对其团队的帐户组的使用情况报告查看者角色。他们可以查看帐户组中所有帐户的使用情况，但不能查看部门中其他团队的帐户组的使用情况。

有关分配企业访问权的详细步骤，请参阅[分配企业访问权](/docs/iam?topic=iam-assign-access-enterprise)。

## 查看企业使用情况
{: #enterprise-usage-console}

1. 登录到企业帐户。
1. 转至**管理 > 计费和使用情况**，然后选择**使用情况**。

   “使用情况”页面显示企业中所有资源使用量的成本（按帐户和帐户组细分）。您还可以查看整个企业的支持信用值使用情况以及产生的任何超额费。

   当前结算周期不包含经典基础架构服务的使用情况信息。但是，先前的结算周期包含这些信息，您可以通过从**时间范围**菜单中选择较早的月份进行查看。有关更多信息，请参阅[查看经典基础架构资源的使用情况](/docs/billing-usage?topic=billing-usage-infra-usage)。
1. 要查看帐户组中的使用情况，请单击表或**企业级别**菜单中的帐户组名称。与企业级别类似，使用情况也是按帐户和帐户组细分的。

   如果帐户组不包含任何帐户，那么该帐户组不会显示在“使用情况”页面上。

1. 要按资源查看使用情况，请通过单击表中的帐户组或从**企业级别**菜单中选择帐户来转至帐户级别。这将显示在相应时间范围内使用的每种类型资源的成本。

   在企业帐户中，无法查看资源套餐或实例的使用情况数据，因为这需要相应帐户中的访问权。如果您是该帐户中的用户，请切换到该帐户以查看这些数据。您需要具有对该帐户中资源和服务的计费访问权，如[查看使用情况](/docs/billing-usage?topic=billing-usage-viewingusage)中所述。

企业帐户中仅显示企业中各帐户所产生的使用情况数据。要在将帐户添加到企业之前查看其使用情况，请登录到该帐户并选择相关时间范围。
{: note}

### 使用 CLI 查看企业使用情况
{: #enterprise-usage-cli}

您可以获取企业、帐户组或特定帐户的使用情况报告。

1. 登录并选择企业帐户。

   ```
ibmcloud login
```
   {:codeblock}

1. 如果要查看特定帐户组或帐户的使用情况，请通过运行 **`ibmcloud enterprise`** 命令来查找相应名称或标识。

   例如，以下命令显示企业中的所有帐户组。

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}

1. 通过运行 **`ibmcloud billing`** 命令来查看使用情况，如以下示例所示。

   * 查看当月整个企业的使用情况。

      ```
      ibmcloud billing enterprise-usage
      ```
      {: codeblock}

   * 查看 2019 年 7 月`开发`帐户组的使用情况。

      ```
      ibmcloud billing enterprise-usage --account-group Development --month 2019-07
      ```
      {:codeblock}

   * 查看企业正下方的帐户组和帐户的使用情况。

      ```
      ibmcloud billing enterprise-usage --children
      ```
      {:codeblock}

   缺省情况下，命令按以下格式输出当月使用情况报告。大部分成本都列为可计费成本。非可计费成本仅在极少数情况下列出，例如向企业添加试用帐户的月份。

   ```
   Name             Type            Billable Cost   Non-billable Cost   Currency   Month   
Example Corp     account         123.45          0                   USD        2019-07   
Development      account_group   234.56          0                   USD        2019-07   
Marketing        account_group   345.67          0                   USD        2019-07   
Sales            account_group   456.78          0                   USD        2019-07
   ```

   可以通过指定 `--output JSON` 选项以 JSON 格式输出报告。
   {: tip}

### 使用 API 查看企业使用情况
{: #enterprise-usage-api}

您可以通过调用[企业使用情况报告 API (Beta)](https://{DomainName}/apidocs/enterprise-apis/resource-usage-reports){: external}，从企业及其帐户中获取使用情况报告。可以将 API 中的查询基于企业、帐户组或帐户，并指定是查看实体还是其子代。企业使用情况报告 API 是 Beta 发行版。

以下示例显示了可用于获取不同使用情况报告的查询。调用 API 时，请将标识变量和 IAM 令牌替换为企业中的值。

查看当月整个企业的使用情况。

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

查看 2019 年 7 月帐户组的使用情况。

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?account_group_id=$ACCOUNT_GROUP_ID&month=2019-07" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

查看企业正下方的帐户组和帐户的使用情况。

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID&children=true" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}


## 回收企业使用成本
{: #enterprise-cost-recovery}

企业将其所有帐户和帐户组的计费合并到单个发票，从而简化了计费管理。您可以通过向关联的部门或团队收取每个帐户组或帐户的使用成本，回收企业中的资源使用成本。

要查看企业层次结构和任何使用情况，您需要具有对整个企业的企业服务的编辑者或管理员角色的访问策略。以下步骤以 {{site.data.keyword.Bluemix_notm}} 控制台为例，但您还可以使用 CLI 或 API 来执行这些步骤。

1. 通过在企业帐户中转至**管理 > 使用情况**来查找每个部门的使用成本。在**时间范围**菜单中，选择上个月以查看最新发票中包含的使用情况。

  帐户组的成本会以表形式列出。这些成本包括所有费用，但在您的计费区域中收取的任何税款除外。如果要进一步细分使用成本，请单击帐户组名称来查看其中包含的帐户和帐户组。

1. 识别公司中对应于帐户组的部门。

   如果分配给帐户组的联系人与您要向其回收成本的部门相关联，那么可通过查找该联系人来查找这些信息。转至**管理 > 企业**，然后选择**帐户**。每个帐户组的联系人会以表形式列出。

   但是，计费做法因公司而异。例如，帐户组联系人可能是与您要收费的部门无关的技术联系人。请始终根据公司的会计流程来验证部门是否正确。

   如果公司使用计费代码来向部门回收成本，请将计费代码添加到帐户组名称，以轻松识别该代码。例如，`销售 - A2B3`。
   {: tip}

1. 将每个帐户组的使用成本与识别到的部门进行匹配，然后遵循公司的流程来提交费用。
