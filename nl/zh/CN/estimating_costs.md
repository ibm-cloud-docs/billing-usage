---

copyright:

  years: 2015, 2018

lastupdated: "2018-04-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# 成本计算方法
{: #cost}

您可以使用不同方法来估算使用 {{site.data.keyword.Bluemix}} 平台即服务 (PaaS) 和基础架构即服务 (IaaS) 资源来构建和托管应用程序的成本。
{:shortdesc}

您可以使用以下方法来确定成本：
* 使用[定价计算器 ![外部链接图标](../icons/launch-glyph.svg)](https://console.bluemix.net/pricing/){: new_window} 来估算要使用的平台和基础架构资源的总成本。
* 使用 {{site.data.keyword.Bluemix_notm}} {{site.data.keyword.pricing_sheet}} 上的成本估算工具来查看基于应用程序大小的粗略成本估算。
* 使用“定价”页面上的成本计算器来查看基于您输入的运行时和服务使用量的准确应用程序价格。
* 手动计算成本。

## 使用定价计算器
{: #pricing-calculator}

在进行采购之前，您可以使用定价计算器来估算平台和许多基础架构资源的成本。定价计算器提供以下功能：
  * 成本估算，目前提供的估算以美元货币计。
  * 基础架构资源的估算，目前可用于**计算**和**容器**类别。
  * 资源的成本估算，目前不包含折扣。
  * 提供成本估算是用于规划用途。

1. 可以通过以下其中一种方式来访问定价计算器：
  * 在[“定价”页面 ![外部链接图标](../icons/launch-glyph.svg)](https://www.ibm.com/cloud/pricing){: new_window} 中，单击“探索我们的解决方案”部分中的**试用计算器**。
  * 如果您当前未登录到 {{site.data.keyword.Bluemix_notm}}，请单击 [{{site.data.keyword.Bluemix_notm}} 主页 ![外部链接图标](../icons/launch-glyph.svg)](https://console.bluemix.net/) 中的**定价**。
2. 从**基础架构**或**平台**列表中，选择要定价的资源的类别。这将显示所选类别中的资源，并且还可以搜索特定资源的类别。
3. 选择类别中的资源以查看其描述。某些资源具有多个选项。例如，如果选择**基础架构** > **计算** > **裸机服务器**，那么可以从服务器列表中进行选择。 
4. 选择要添加的资源数量。
5. 单击**添加到估算**。
6. 继续从**基础架构**和**平台**类别中添加资源，直到添加完要估算的内容为止。

**估算**面板会显示您添加的资源、每个资源的价格和总价格。 

如果要仅对平台资源定价，那么可以单击**切换到经典计算器**来查看以非美元货币计的估算。经典计算器不包含基础架构资源。
{: tip}

### 将经典计算器用于平台资源
{: #calculator}

要计算以非美元货币计的平台资源成本，可以使用经典计算器。经典计算器不包提供基础架构资源的定价估算。

1. 转至 {{site.data.keyword.Bluemix_notm}} {{site.data.keyword.pricing_sheet}}。
2. 选择“基础架构”中的其中一个选项以支持所有工作负载部分。

要使用该计算器，请输入所列资源的每月计划使用量；例如，实例数或推送通知数。计算器会针对您的输入立即显示价格。您还可以调整计算器，以显示每年成本，而不是每月成本。

## 手动计算成本
{: #manual}

您可能想要自己估算 {{site.data.keyword.Bluemix_notm}} 成本，以更好地了解 {{site.data.keyword.Bluemix_notm}} 成本的计算方式。您可以考虑运行时和它使用的服务的价格，计算使用 {{site.data.keyword.Bluemix_notm}} 构建和托管应用程序的总价格。由于运行时和服务的价格有时会更改，因此在计算总价格时必须参考 {{site.data.keyword.Bluemix_notm}}“价格表”上的最新信息。

## 支持的计费货币

下表列出了可用的不同计费货币。

|ISO 4217 代码| 货币|
|-------------|---------|
|AUD|	  澳元|
|BRL|	  巴西雷亚尔|
|CAD|	  加拿大元|
|CHF|	  瑞士法郎|
|DKK|	  丹麦克郎|
|EUR|	  欧元|
|GBP|	  英镑|
|INR|	  印度卢比|
|JPY|	  日元|
|KRW|	  韩元|
|NOK|	  挪威克朗|
|NZD|	  新西兰元|
|SEK|	  瑞典克朗|
|USD|    美元|
|ZAR|	  南非兰特|
{:caption="表 1. 支持的货币" caption-side="top"}

如果已链接您的 {{site.data.keyword.Bluemix_notm}} 和 SoftLayer 帐户，那么您收到的单个发票只使用美元 (USD)。
有关更多信息，请参阅[链接帐户的合并帐单](/docs/account/linking_accounts.html)。
{: tip}
