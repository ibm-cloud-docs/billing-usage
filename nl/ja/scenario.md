---

copyright:

  years: 2015, 2018
lastupdated: "2018-04-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# シナリオ: Node アプリの例のコスト見積もり
{: #sample}

スケーリング機能を持つ Node.js Web アプリを使用しており、そのアプリは {{site.data.keyword.Bluemix}} が提供する複数のサービスを使用していると仮定します。 この例で、ご使用のアプリの実際のコストがどのように計算されるかを学習することができます。 この Web アプリは、以下の {{site.data.keyword.Bluemix_notm}}
サービスとアイテムを使用します。

* 4 個の 256 MB Node.js ランタイム・インスタンス
* 2 個の {{site.data.keyword.autoscaling}} ポリシー、およびプロセッサーとメモリー
* 1 月あたり 2 GB の {{site.data.keyword.datacshort}}
* 1 月あたり 150 GB の NoSQL データベース、100,000 回の高負荷 API 呼び出し、および 500,000 回の軽負荷 API 呼び出し
* 20 GB のインバウンドまたはアウトバウンドのネットワーク・トラフィック

## {{site.data.keyword.Bluemix_notm}} リソースの価格
{: #sample_resources}

例を単純にするため、以下の表の価格が月などの時間フレーム内または時間フレーム間で変動しないと仮定します。 この例の価格設定はすべてアメリカ合衆国の通貨です。

|サービス |	フィーチャー |	価格 |
|--------|-----------|--------|
|SDK for Node.js |	1 月あたり 375 GB 時間無料 (すべてのランタイム間で共有) |	$0.07 (米ドル)/GB 時間|
|{{site.data.keyword.autoscaling}} |	{{site.data.keyword.autoscaling}} サービスの無料サービス・プラン |	無料|
|{{site.data.keyword.datacshort}} - スターター |	1 GB のキャッシュ・スペースおよびレプリカ |	$55.00 (米ドル)/インスタンス |
|{{site.data.keyword.datacshort}} - 標準 |	5 GB のキャッシュ・スペースおよびレプリカ |	$155.00 (米ドル)/インスタンス |
|{{site.data.keyword.datacshort}} - プレミアム |	25 GB のキャッシュ・スペースおよびレプリカ |	$505.00 (米ドル)/インスタンス|
|IBM Cloudant® NoSQL DB for {{site.data.keyword.Bluemix_notm}} |	2 GB の無料データ・ストレージ<br/>1 月あたり 50,000 回の無料軽負荷 API 呼び出し<br/>1 月あたり 10,000 回の無料高負荷 API 呼び出し | $1.00 (米ドル)/GB<br/>$0.03 (米ドル)/軽負荷 API 呼び出し 1000 回<br/>$0.15 (米ドル)/高負荷 API 呼び出し 1000 回 |
{:caption="表 1. リソースの価格設定" caption-side="top"}

## アプリ価格の計算

アプリの価格は、次の方法で計算することができます。

<dl>
<dt>4 個の 256 MB Node.js ランタイム・インスタンス</dt>
<dd>{{site.data.keyword.Bluemix_notm}} は、
GB 時間ごとにランタイムに課金します。 1 月あたりに使用される GB 数は、<code>4 x 256 = 1024 MB つまり 1 GB /月</code>です。 <code>1 カ月を 24 x 30 = 720 時間</code> と仮定すると、アプリケーションは <code>1 x 720 = 720 GB 時間</code>に対して課金されます。
<p>
すべての {{site.data.keyword.Bluemix_notm}} ランタイムにわたって共有される 1 月あたりの無料枠に、375 GB 時間が含まれます。 そのため、ランタイムの総額は、<code>$0.07 x (720-375) = $24.15</code> となります。</p></dd>

<dt>2 個の {{site.data.keyword.autoscaling}} ポリシー (プロセッサーとメモリー)</dt>
<dd>{{site.data.keyword.autoscaling}} ポリシーは無料です。</dd>

<dt>1 月あたり 2 GB の {{site.data.keyword.datacshort}}</dt>
<dd>{{site.data.keyword.datacshort}} サービスが提供する 50 MB プランは無料です。 ただし、無料のプランでは、1 カ月当たり 2 GB と予測される使用量をカバーできません。 {{site.data.keyword.datacshort}} の 3 つの有料プランでは、使用したスペースの量にかかわらず、特定のスペース量に対する一定の料金がかかります。 そのため、予測される使用量を満たす最小限のプランである 5 GB の標準プランを選択することにします。 総額は 1 月あたり $155 になります。</dd>

<dt>1 月あたり 150 GB の NoSQL データベース</dt>
<dd>Cloudant NoSQL DB for {{site.data.keyword.Bluemix_notm}} のサービス料金は、データ・ストレージおよび各 API メソッドでそのデータにアクセスする機能に基づきます。 <strong>PUT</strong> コマンドおよび
<strong>POST</strong> コマンドは高負荷 API 呼び出しとみなされますが、
<strong>GET</strong> コマンドは軽負荷 API 呼び出しとみなされます。
<p>
GB 数を合計して、2 GB の無料枠を減算します。 1 月あたり 148 GB が課金されます。 軽負荷 API 呼び出し 50,000 回の無料枠と、高負荷 API 呼び出し 10,000 回の無料枠を減算します。 ストレージの総額には、次のものが含まれています。</p>
<pre class="codeblock">
<codeblock>
    148 x 1 = $148
    (450,000 / 1000) x 0.03 = $13.5
    (90,000 / 1000) x 0.15 = $13.5
</codeblock>
</pre>
<p>
総額は、148 + 13.5 + 13.5 = $175 です。</p></dd>

<dt>20 GB のインバウンドまたはアウトバウンドのネットワーク・トラフィック</dt>
<dd>インバウンドおよびアウトバウンドのネットワーク・トラフィックは無料です。</dd>

</dl>

すべてのアイテムが加算される場合、アプリケーションの総額は $354.15 となります。
