---

copyright:

  years: 2015, 2018
lastupdated: "2018-11-15"

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
* 每月 150 GB（针对 {{site.data.keyword.cloudant_short_notm}} 数据库，1,000 个查找、500 次写入和 50 个查询）。
* 20 GB 入站或出站网络流量


## {{site.data.keyword.Bluemix_notm}} 资源的价格
{: #sample_resources}

为了简化示例，假设下表中的价格在某个时间范围（例如，一个月）内不波动。此示例中的所有定价使用美元。

|服务|	功能|	价格|
|-----------------------------------|---------------------------------------------------------------------|-------------------|
| {{site.data.keyword.runtime_nodejs_short}}                   |	每月 375 GB-小时可用（在所有运行时共享）|	0.07 美元/GB-小时|
| {{site.data.keyword.autoscaling}} |	{{site.data.keyword.autoscaling}} 服务的免费服务套餐|	免费|
| {{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}} - 轻量|包含 20 GB 免费数据存储</br>按以下增量扩展供应的吞吐量容量：</br>每秒 100 个查找</br>每秒 50 次写入</br>每秒 5 个查询|1.00 美元/GB 数据存储</br>每秒 0.25 美元/查找</br>每秒 0.50 美元/写入</br>每秒 5.00 美元/查询|
{:caption="表 1. 资源的定价" caption-side="top"}


## 计算应用程序价格
{: #calc-app-price}

可以使用以下方式来计算应用程序的价格：

<dl>
<dt>四个 256 MB Node.js 运行时实例</dt>
<dd>{{site.data.keyword.Bluemix_notm}} 对运行时按 GB-小时收费。每月使用的 GB 数是 <code>4 x 256 = 1024 MB 或 1 GB/月</code>。假设<code>一个月有 24 x 30 = 720 小时</code>，那么应用程序按 <code>1 x 720 = 720 GB-小时</code>收费。<p>
375 GB-小时包括在每月免费限额中，该限额在所有 {{site.data.keyword.Bluemix_notm}} 运行时中共享。因此，运行时的总成本为 <code>0.07 美元 x (720-375) = 24.15 美元</code>。</p></dd>

<dt>两个 {{site.data.keyword.autoscaling}} 策略（处理器和内存）</dt>
<dd>{{site.data.keyword.autoscaling}} 策略免费。</dd>

<dt>每月 150 GB（针对 {{site.data.keyword.cloudant_short_notm}}）</dt>
<dd>{{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}} 服务费用基于数据存储和按每秒查找数、写入数和查询数表示的供应的吞吐量容量访问此数据的能力。
<p>
加总 GB 数并减去 20 GB 免费限额。每月对 130 GB 收费。存储价格总计包括以下部分：</p>
<pre class="codeblock">
<codeblock>
    130 x 1 = $130
    (1,000 / 100) x 0.25 = $2.50
    (500 / 50) x 0.50 = $5.00
    (50 / 5) x 5.00 = $50.00
</codeblock>
</pre>
<p>
总价格为 130 + 2.50 + 5.00 + 50.00 = 187.50 美元。</p></dd>

<dt>20 GB 入站或出站网络流量</dt>
<dd>入站和出站网络流量免费。</dd>

</dl>

加总所有项时，应用程序的总价格为 211.65 美元。
