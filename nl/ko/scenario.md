---

copyright:

  years: 2015, 2018
lastupdated: "2017-10-09"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# 시나리오: 예제 Node 앱의 비용 추정
{: #sample}

확장 기능이 있는 Node.js 웹 앱이 있으며 이 앱이 {{site.data.keyword.Bluemix}}에서 제공하는 여러 서비스를 사용한다고 가정하십시오. 이 예제를 통해 앱의 실제 비용이 어떻게 계산되는지 이해할 수 있습니다. 웹 앱이 사용하는 {{site.data.keyword.Bluemix_notm}} 서비스와 항목은 다음과 같습니다.

* 256MB Node.js 런타임 인스턴스 4개
* 2개의 {{site.data.keyword.autoscaling}} 정책, 프로세서 및 메모리
* 매월 2GB의 {{site.data.keyword.datacshort}}
* 매월 150GB의 NoSQL 데이터베이스, Heavy API 호출 100,000개 및 Light API 호출 500,000개
* 20GB의 인바운드 또는 아웃바운드 네트워크 트래픽

## {{site.data.keyword.Bluemix_notm}} 리소스의 가격
{: #sample_resources}

예를 단순화하기 위해 다음 표의 가격은 특정 시간 범위(예: 한 달) 내에서 또는 시간 범위 간에 변동되지 않는다고 가정합니다. 이 예의 모든 가격은 미국 통화입니다.

|서비스 |	기능 |	가격 |
|--------|-----------|--------|
|SDK for Node.js |	매월 375GB-시간 무료(모든 런타임에서 공유됨) |	$0.07 USD/GB-시간|
|{{site.data.keyword.autoscaling}} |	{{site.data.keyword.autoscaling}} 서비스에 대한 무료 서비스 플랜 |	무료|
|{{site.data.keyword.datacshort}} - 스타터 |	1GB의 캐시 공간 및 복제본 |	$55.00 USD/인스턴스 |
|{{site.data.keyword.datacshort}} - 표준 |	5GB의 캐시 공간 및 복제본 |	$155.00 USD/인스턴스 |
|{{site.data.keyword.datacshort}} - 프리미엄 |	25GB의 캐시 공간 및 복제본 |	$505.00 USD/인스턴스|
|IBM Cloudant® NoSQL DB for {{site.data.keyword.Bluemix_notm}} |	2GB의 사용 가능한 데이터 스토리지<br/>매월 50,000개의 Light API 호출 무료<br/>매월 10,000개의 Heavy API 호출 무료 | $1.00 USD/GB<br/>$0.03 USD/1000개의 Light API 호출<br/>$0.15 USD/1000개의 Heavy API 호출 |
{:caption="표 1. 리소스 가격 책정" caption-side="top"}

## 앱 가격 계산

앱 가격은 다음과 같은 방법으로 계산될 수 있습니다.

<dl>
<dt>256MB Node.js 런타임 인스턴스 4개</dt>
<dd>{{site.data.keyword.Bluemix_notm}}에서는 런타임 비용을 GB-시간 단위로 청구합니다. 매월 사용량(GB)은 <code>월별 4 x 256 = 1024MB 또는 1GB</code>입니다. <code>한 달은 24 x 30 = 720시간</code>으로 가정하므로 애플리케이션의 비용이 <code>1 x 720 = 720GB-시간</code>으로 청구됩니다.
<p>
375GB-시간은 매달 무료 사용량에 포함되며, 모든 {{site.data.keyword.Bluemix_notm}} 런타임에서 공유됩니다. 런타임의 총 비용은 <code>$0.07 x (720-375) = $24.15</code>입니다.</p></dd>

<dt>2개의 {{site.data.keyword.autoscaling}} 정책(프로세서 및 메모리)</dt>
<dd>{{site.data.keyword.autoscaling}} 정책은 무료입니다.</dd>

<dt>매월 2GB의 {{site.data.keyword.datacshort}}</dt>
<dd>{{site.data.keyword.datacshort}} 서비스에서 50MB 플랜을 무료로 제공합니다. 그러나 무료 사용제로는 매달 2GB의 예상 사용량을 충당할 수 없습니다. {{site.data.keyword.datacshort}}에 대한 3개의 유료 사용제를 사용할 경우 실제로 사용하는 공간의 양에 관계없이 특정 공간량에 대해 정해진 비용이 듭니다. 따라서 예상 사용량을 충족하는 최소 플랜을 선택할 수 있는데, 이것이 표준 플랜(5GB)입니다. 총 비용은 매달 $155입니다.</dd>

<dt>매월 150GB의 NoSQL 데이터베이스</dt>
<dd>Cloudant NoSQL DB for {{site.data.keyword.Bluemix_notm}} 서비스 비용은 데이터 스토리지 및 여러 API 메소드로 데이터에 액세스할 수 있는지에 따라 달라집니다. <strong>PUT</strong> 및 <strong>POST</strong> 명령은 Heavy API 호출로 간주되지만, <strong>GET</strong> 명령은 Light API 호출로 간주됩니다.
<p>
GB 수를 더한 다음 2GB 무료 사용량을 빼십시오. 매달 148GB가 청구됩니다. Light API 호출의 경우 무료 사용량인 50,000을 빼고, Heavy API 호출의 경우 10,000을 빼십시오. 총 스토리지 가격에는 다음과 같은 파트가 포함됩니다.</p>
<pre class="codeblock">
<codeblock>
    148 x 1 = $148
    (450,000 / 1000) x 0.03 = $13.5
    (90,000 / 1000) x 0.15 = $13.5
</codeblock>
</pre>
<p>
총 가격은 148 + 13.5 + 13.5 = $175입니다.</p></dd>

<dt>20GB의 인바운드 또는 아웃바운드 네트워크 트래픽</dt>
<dd>인바운드 및 아웃바운드 네트워크 트래픽은 무료입니다.</dd>

</dl>

모든 항목을 더할 경우 총 애플리케이션 가격은 $354.15입니다.
