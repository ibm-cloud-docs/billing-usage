---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-15"

keywords: estimate cost, cost example, billing example, payment example

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# 시나리오: 예제 Node 앱의 비용 추정
{: #sample}

스케일링 기능이 있는 Node.js 웹 앱이 있으며 이 앱이 {{site.data.keyword.Bluemix}}에서 제공하는 여러 서비스를 사용한다고 가정하십시오. 이 예제를 통해 앱의 실제 비용이 어떻게 계산되는지 이해할 수 있습니다. 웹 앱이 사용하는 {{site.data.keyword.Bluemix_notm}} 서비스와 항목은 다음과 같습니다.

* 256MB Node.js 런타임 인스턴스 4개
* 2개의 {{site.data.keyword.autoscaling}} 정책, 프로세서 및 메모리
* 월별 150GB {{site.data.keyword.cloudant_short_notm}} 데이터베이스, 1,000개의 검색, 500개의 쓰기 및 50개의 조회.
* 20GB의 인바운드 또는 아웃바운드 네트워크 트래픽


## {{site.data.keyword.Bluemix_notm}} 리소스의 가격
{: #sample_resources}

예제를 단순화하기 위해 다음 표의 가격은 특정 시간 범위(예: 한 달) 내에서 또는 시간 범위 사이에서 변동되지 않는다고 가정하십시오. 이 예의 모든 가격은 미국 통화입니다.

|서비스                           |	기능                                                            |	가격             |
|-----------------------------------|---------------------------------------------------------------------|-------------------|
| {{site.data.keyword.runtime_nodejs_short}}                   |	매월 375GB-시간 무료(모든 런타임에서 공유됨)            |	$0.07 USD/GB-시간 |
| {{site.data.keyword.autoscaling}} |	{{site.data.keyword.autoscaling}} 서비스에 대한 무료 서비스 플랜 |	무료              |
| {{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}} - Lite | 20GB의 사용 가능한 데이터 스토리지 포함</br>프로비저닝된 처리량 용량을 다음과 같은 증분으로 스케일링합니다.</br>초당 100개의 검색</br>초당 50개의 쓰기</br>초당 5개의 조회 | $1.00USD/GB의 데이터 스토리지</br>$0.25USD/초당 검색</br>$0.50USD/초당 쓰기</br>$5.00USD/초당 조회 |
{:caption="표 1. 리소스 가격" caption-side="top"}


## 앱 가격 계산
{: #calc-app-price}

앱 가격은 다음과 같은 방법으로 계산될 수 있습니다.

<dl>
<dt>256MB Node.js 런타임 인스턴스 4개</dt>
<dd>{{site.data.keyword.Bluemix_notm}}에서는 런타임 비용을 GB-시간 단위로 청구합니다. 매월 사용량(GB)은 <code>월별 4 x 256 = 1024MB 또는 1GB</code>입니다. <code>한 달은 24 x 30 = 720시간</code>으로 가정하므로 애플리케이션의 비용이 <code>1 x 720 = 720GB-시간</code>으로 청구됩니다.
<p>
375GB-시간은 매달 무료 사용량에 포함되며, 모든 {{site.data.keyword.Bluemix_notm}} 런타임에서 공유됩니다. 런타임의 총 비용은 <code>$0.07 x (720-375) = $24.15</code>입니다.</p></dd>

<dt>2개의 {{site.data.keyword.autoscaling}} 정책(프로세서 및 메모리)</dt>
<dd>{{site.data.keyword.autoscaling}} 정책은 무료입니다.</dd>

<dt>매월 150GB {{site.data.keyword.cloudant_short_notm}}</dt>
<dd>{{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}} 서비스 비용은 초당 검색, 쓰기 및 조회로 표시되는 프로비저닝된 처리량 용량별로 해당 데이터에 액세스하는 기능 및 데이터 스토리지를 기반으로 청구됩니다.
<p>
GB 수를 더한 다음 20GB 무료 사용량을 빼십시오. 매달 130GB가 청구됩니다. 총 스토리지 가격에는 다음과 같은 파트가 포함됩니다.</p>
<pre class="codeblock">
<codeblock>
    130 x 1 = $130
    (1,000 / 100) x 0.25 = $2.50
    (500 / 50) x 0.50 = $5.00
    (50 / 5) x 5.00 = $50.00
</codeblock>
</pre>
<p>
총 가격은 130 + 2.50 + 5.00 + 50.00 = $187.50입니다.</p></dd>

<dt>20GB의 인바운드 또는 아웃바운드 네트워크 트래픽</dt>
<dd>인바운드 및 아웃바운드 네트워크 트래픽은 무료입니다.</dd>

</dl>

모든 항목을 더할 경우 총 애플리케이션 가격은 $211.65입니다.
