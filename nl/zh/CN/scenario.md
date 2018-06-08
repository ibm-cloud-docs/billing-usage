---

copyright:

  years: 2015, 2018
lastupdated: "2018-04-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# 场景：估算示例节点应用程序的成本
{: #sample}

假定您的 Node.js Web 应用程序具有扩展能力，并且该应用程序使用 {{site.data.keyword.Bluemix}} 提供的多个服务。在此示例中，您可以了解如何计算应用程序的实际成本。Web 应用程序使用以下 {{site.data.keyword.Bluemix_notm}} 服务和项：

* 四个 256 MB Node.js 运行时实例
* 两个 {{site.data.keyword.autoscaling}} 策略、处理器和内存
* 每月 2 GB（针对 {{site.data.keyword.datacshort}}）
* NoSQL 数据库每月 150 GB、100,000 个频繁 API 调用和 500,000 个稀少 API 调用
* 20 GB 入站或出站网络流量

## {{site.data.keyword.Bluemix_notm}} 资源的价格
{: #sample_resources}

为了简化示例，假设下表中的价格在某个时间范围（例如，一个月）内不波动。此示例中的所有定价使用美元。

|服务|	功能|	价格|
|--------|-----------|--------|
|SDK for Node.js|	每月 375 GB-小时可用（在所有运行时共享）|	0.07 美元/GB-小时|
|{{site.data.keyword.autoscaling}} |	{{site.data.keyword.autoscaling}} 服务的免费服务套餐|	免费|
|{{site.data.keyword.datacshort}} - 入门模板|	1 GB 高速缓存空间和副本|	55.00 美元/实例|
|{{site.data.keyword.datacshort}} - 标准|	5 GB 高速缓存空间和副本|	155.00 美元/实例|
|{{site.data.keyword.datacshort}} - 高端|	25 GB 高速缓存空间和副本|	505.00 美元/实例|
|IBM Cloudant® NoSQL DB for {{site.data.keyword.Bluemix_notm}}|	2 GB 免费数据存储<br/>每月 50,000 个免费稀少 API 调用<br/>每月 10,000 个免费频繁 API 调用|1.00 美元/GB<br/>0.03 美元/1000 个稀少 API 调用<br/>0.15 美元/1000 个频繁 API 调用|
{:caption="表 1. 资源的定价" caption-side="top"}

## 计算应用程序价格

可以使用以下方式来计算应用程序的价格：

<dl>
<dt>四个 256 MB Node.js 运行时实例</dt>
<dd>{{site.data.keyword.Bluemix_notm}} 对运行时按 GB-小时收费。每月使用的 GB 数是 <code>4 x 256 = 1024 MB 或 1 GB/月</code>。假设<code>一个月有 24 x 30 = 720 小时</code>，那么应用程序按 <code>1 x 720 = 720 GB-小时</code>收费。<p>
375 GB-小时包括在每月免费限额中，该限额在所有 {{site.data.keyword.Bluemix_notm}} 运行时中共享。因此，运行时的总成本为 <code>0.07 美元 x (720-375) = 24.15 美元</code>。</p></dd>

<dt>两个 {{site.data.keyword.autoscaling}} 策略（处理器和内存）</dt>
<dd>{{site.data.keyword.autoscaling}} 策略免费。</dd>

<dt>每月 2 GB（针对 {{site.data.keyword.datacshort}}）</dt>
<dd>{{site.data.keyword.datacshort}} 服务提供的 50 MB 套餐免费。然而，免费套餐可能难以满足您每月计划使用的 2 GB。{{site.data.keyword.datacshort}} 的 3 个付费套餐都是以固定金额购买特定的空间量，而不管您实际使用的空间量是多少。因此，您希望选择符合您计划使用量（标准套餐为 5 GB）的最低限度套餐。每月总开销为 155 美元。</dd>

<dt>NoSQL 数据库每月 150 GB</dt>
<dd>Cloudant NoSQL DB for {{site.data.keyword.Bluemix_notm}} 服务费用基于数据存储和按不同 API 方法访问该数据的能力。<strong>PUT</strong> 和 <strong>POST</strong> 命令被视为频繁 API 调用，但 <strong>GET</strong> 命令被视为稀少 API 调用。<p>
加总 GB 数并减去 2 GB 免费限额。每月对 148 GB 收费。减去 50,000 稀少 API 调用和 10,000 频繁 API 调用的免费限额。存储价格总计包括以下部分：</p>
<pre class="codeblock">
<codeblock>
    148 x 1 = $148
    (450,000 / 1000) x 0.03 = $13.5
    (90,000 / 1000) x 0.15 = $13.5
</codeblock>
</pre>
<p>
总价格为 148 + 13.5 + 13.5 = 175 美元。</p></dd>

<dt>20 GB 入站或出站网络流量</dt>
<dd>入站和出站网络流量免费。</dd>

</dl>

加总所有项时，应用程序的总价格为 354.15 美元。
