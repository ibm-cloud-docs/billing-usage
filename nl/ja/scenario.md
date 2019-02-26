---

copyright:

  years: 2015, 2018
lastupdated: "2018-11-15"

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
* 1 カ月当たり 150 GB の {{site.data.keyword.cloudant_short_notm}} データベース、1,000 件のルックアップ、500 件の書き込み、および 50 件の照会。
* 20 GB のインバウンドまたはアウトバウンドのネットワーク・トラフィック


## {{site.data.keyword.Bluemix_notm}} リソースの価格
{: #sample_resources}

例を単純にするため、以下の表の価格が月などの時間フレーム内または時間フレーム間で変動しないと仮定します。 この例の価格設定はすべてアメリカ合衆国の通貨です。

| サービス                           |	フィーチャー                                                            |	価格             |
|-----------------------------------|---------------------------------------------------------------------|-------------------|
| {{site.data.keyword.runtime_nodejs_short}}                   |	1 月あたり 375 GB 時間無料 (すべてのランタイム間で共有)            |	$0.07 (米ドル)/GB 時間 |
| {{site.data.keyword.autoscaling}} |	{{site.data.keyword.autoscaling}} サービスの無料サービス・プラン |	無料              |
| {{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}} - ライト | 20 GB の無料データ・ストレージを含む</br>プロビジョンされたスループット容量を以下の単位でスケール:</br>1 秒当たり 100 件のルックアップ</br>1 秒当たり 50 件の書き込み</br>1 秒当たり 5 件の照会 | $1.00 USD/GB のデータ・ストレージ</br>$0.25 USD/1 秒当たりのルックアップ</br>$0.50 USD/1 秒当たりの書き込み</br>$5.00 USD/1 秒当たりの照会 |
{:caption="表 1. リソースの価格設定" caption-side="top"}


## アプリ価格の計算
{: #calc-app-price}

アプリの価格は、次の方法で計算することができます。

<dl>
<dt>4 個の 256 MB Node.js ランタイム・インスタンス</dt>
<dd>{{site.data.keyword.Bluemix_notm}} は、
GB 時間ごとにランタイムに課金します。 1 月あたりに使用される GB 数は、<code>4 x 256 = 1024 MB つまり 1 GB /月</code>です。 <code>1 カ月を 24 x 30 = 720 時間</code> と仮定すると、アプリケーションは <code>1 x 720 = 720 GB 時間</code>に対して課金されます。
<p>
すべての {{site.data.keyword.Bluemix_notm}} ランタイムにわたって共有される 1 月あたりの無料枠に、375 GB 時間が含まれます。 そのため、ランタイムの総額は、<code>$0.07 x (720-375) = $24.15</code> となります。</p></dd>

<dt>2 個の {{site.data.keyword.autoscaling}} ポリシー (プロセッサーとメモリー)</dt>
<dd>{{site.data.keyword.autoscaling}} ポリシーは無料です。</dd>

<dt>1 月あたり 150 GB の {{site.data.keyword.cloudant_short_notm}}</dt>
<dd>{{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}} のサービス料金は、データ・ストレージと、1 秒あたりのルックアップ、書き込み、および照会によって示されるプロビジョニングされたスループット容量によって、そのデータにアクセスする機能に基づきます。
<p>
GB 数を合計して、20 GB の無料許容量を減算します。 1 月あたり 130 GB が課金されます。 ストレージの総額には、次のものが含まれています。</p>
<pre class="codeblock">
<codeblock>
    130 x 1 = $130
    (1,000 / 100) x 0.25 = $2.50
    (500 / 50) x 0.50 = $5.00
    (50 / 5) x 5.00 = $50.00
</codeblock>
</pre>
<p>
総額は、130 + 2.50 + 5.00 + 50.00 = $187.50 です。</p></dd>

<dt>20 GB のインバウンドまたはアウトバウンドのネットワーク・トラフィック</dt>
<dd>インバウンドおよびアウトバウンドのネットワーク・トラフィックは無料です。</dd>

</dl>

すべてのアイテムが加算される場合、アプリケーションの総額は $211.65 となります。
