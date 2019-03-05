---



copyright:

  years: 2017, 2018, 2019
lastupdated: "2019-01-09"

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

与管理计费和使用情况相关的一般问题可能包括访问您的帐单信息需要权限。在许多情况下，您可以通过以下几个简单的步骤来解决此问题。
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
