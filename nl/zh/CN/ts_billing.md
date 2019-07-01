---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-11"

keywords: troubleshoot billing, billing error, payment error, error message, feature code, subscription code

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# 有关管理计费和使用情况的故障诊断
{: #troubleshoot}

与管理 {{site.data.keyword.cloud}} 计费和使用情况相关的一般问题可能包括访问您的计费信息所需要的权限。在许多情况下，您可以通过以下几个简单的步骤来解决此问题。
{:shortdesc}


## 为什么无法访问计费信息？
{: #cannot-access-billing-info}
{: troubleshoot}

当您尝试访问计费信息（例如，付款和发票）时，收到一条消息，说明此功能不可用。
{: tsSymptoms}

收到此消息的原因是您无权查看该帐户的计费信息。您必须是帐户所有者或 Cloud Foundry 组织的记帐管理者，或者必须有一个 IAM 策略来分配对所有帐户管理服务的“管理员”角色。
{: tsCauses}

对于您拥有的任何帐户，您都可以查看其计费信息。记帐管理者能够查看 Cloud Foundry 组织的计费信息。而且，对于支持 IAM 的资源，您必须有一个 IAM 策略来分配对所有帐户管理服务的“管理员”角色。

通过完成以下步骤来检查您的访问权：

  1. 转至**管理 > 访问权 (IAM)**，然后选择**用户**。
  2. 在“用户”页面中，单击您的姓名。
  3. 单击**访问策略**以查看分配给您的 IAM 访问策略。
  4. 单击 **Cloud Foundry 访问权**，然后展开您的已分配组织所在的行，以查看您是否具有“帐户所有者”或“记帐管理者”角色。

有关 IAM 访问权的更多信息，请参阅 [Cloud IAM 角色](/docs/iam?topic=iam-userroles)。有关 Cloud Foundry 访问权的更多信息，请参阅 [Cloud Foundry 角色](/docs/iam?topic=iam-cfaccess)。
{: tsResolve}


## 为什么无法应用特征代码？
{: #cannot-apply-feature-code}
{: troubleshoot}

尝试应用特征代码时，您会看到一条错误，指出无法应用该代码。
{: tsSymptoms}

帐户不满足特征代码的需求，或者您在帐户中没有必需的访问级别。
{: tsCauses}

- 验证您是否具有正确的帐户类型。例如，某些用于教育促销的特征代码仅适用于轻量帐户。要查看帐户类型，请转至**管理 > 帐户**，然后选择**帐户设置**。有关详细信息，请参阅[应用特征代码](/docs/account?topic=account-codes)。
- 验证您是否有权应用特征代码。要应用任何特征代码，您必须拥有对所有帐户管理服务的编辑者角色或更高级别的角色。要查看或更改角色，请参阅[分配对帐户管理服务的访问权](/docs/iam?topic=iam-account-services)。
{: tsResolve}
