---

copyright:

  years: 2015, 2018
lastupdated: "2018-11-15"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# 情境：預估範例 Node 應用程式的成本
{: #sample}

假設您的 Node.js Web 應用程式具有擴充功能，而且該應用程式使用 {{site.data.keyword.Bluemix}} 所提供的數個服務。您可以在此範例中瞭解如何計算應用程式的實際成本。Web 應用程式使用下列 {{site.data.keyword.Bluemix_notm}} 服務及項目：

* 四個 256 MB Node.js 運行環境實例
* 兩個 {{site.data.keyword.autoscaling}} 原則：處理器及記憶體
* 每月 150 GB 的 {{site.data.keyword.cloudant_short_notm}} 資料庫、1,000 次查閱、500 次寫入，及 50 次查詢。
* 20 GB 的入埠或出埠網路資料流量


## {{site.data.keyword.Bluemix_notm}} 資源的價格
{: #sample_resources}

為了讓範例保持簡單，我們假設下表中的價格不會在時間範圍（例如，一個月）內或之間波動。此範例中的所有定價都以美金計價。

|服務|	特性|	價格|
|-----------------------------------|---------------------------------------------------------------------|-------------------|
| {{site.data.keyword.runtime_nodejs_short}}                   |	每個月有 375 GB-小時免費（跨所有運行環境共用）|	美金 0.07 元/GB-小時|
| {{site.data.keyword.autoscaling}} |	{{site.data.keyword.autoscaling}} 服務的免費服務方案|	免費|
| {{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}} - Lite |包含 20 GB 的免費資料儲存空間</br>擴充佈建的傳輸量，使用增量為：</br>每秒 100 次查閱</br>每秒 50 次寫入</br>每秒 5 次查詢|美金 1.00 元/GB 的資料儲存空間</br>美金 0.25 元/每秒查閱</br>美金 0.50 元/每秒寫入</br>美金 5.00 元/每秒查詢|
{:caption="表 1. 資源的定價" caption-side="top"}


## 計算應用程式價格
{: #calc-app-price}

應用程式的價格可以使用下列方式進行計算：

<dl>
<dt>四個 256 MB Node.js 運行環境實例</dt>
<dd>{{site.data.keyword.Bluemix_notm}} 是依 GB-小時來收取運行環境的費用。每個月所使用的 GB 數目為 <code>4 x 256 = 1024 MB 或 1 GB（每個月）</code>。假設<code>一個月有 24 x 30 = 720 小時</code>，則會依 <code>1 x 720 = 720 GB-小時</code>收取應用程式的費用。
<p>
每個月的免費額度包含 375 GB-小時（跨所有 {{site.data.keyword.Bluemix_notm}} 運行環境共用）。因此，運行環境的總成本是 <code>$0.07 x (720-375) = $24.15</code>。</p></dd>

<dt>兩個 {{site.data.keyword.autoscaling}} 原則（處理器及記憶體）</dt>
<dd>{{site.data.keyword.autoscaling}} 原則是免費的。</dd>

<dt>每月 150 GB 的 {{site.data.keyword.cloudant_short_notm}}</dt>
<dd>{{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}} 服務費用是根據資料儲存空間，以及能夠透過佈建傳輸量容量（以每秒查閱、寫入和查詢表示）存取該資料。
<p>
將 GB 數目加總，並扣除 20 GB 免費額度。每個月收取 130 GB 的費用。總儲存空間價格包含下列部分：</p>
<pre class="codeblock">
<codeblock>
    130 x 1 = $130
    (1,000 / 100) x 0.25 = $2.50
    (500 / 50) x 0.50 = $5.00
    (50 / 5) x 5.00 = $50.00
</codeblock>
</pre>
<p>
總價為 130 + 2.50 + 5.00 + 50.00 = $187.50。</p></dd>

<dt>20 GB 的入埠或出埠網路資料流量</dt>
<dd>入埠及出埠網路資料流量免費。</dd>

</dl>

所有項目相加之後，應用程式的總價是 $211.65。
