---



copyright:

  years: 2015, 2018
lastupdated: "2018-04-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 연결된 계정에 대한 통합된 청구
{: #unifybillaccounts}

{{site.data.keyword.Bluemix_notm}}와 Softlayer 계정을 연결한 경우 단일 {{site.data.keyword.Bluemix_notm}} 송장을 수신합니다. 기존 {{site.data.keyword.Bluemix_notm}} 계정을 보유하고 있는 경우, {{site.data.keyword.Bluemix_notm}}를 통한 인프라 리소스의 청구는 계정이 연결된 이후 시작되는 새 청구 주기에 적용됩니다.
{: shortdesc}

{{site.data.keyword.Bluemix_notm}}의 모든 연결된 계정은 종량과금제 또는 구독 계정이어야 합니다.
{: tip}

## 계정 연결 시 {{site.data.keyword.Bluemix_notm}} 사용에 대한 청구
{: #linkedbilling}

{{site.data.keyword.Bluemix_notm}} 및 SoftLayer 청구 계정을 연결한 후, 다음 청구 주기는 단일 {{site.data.keyword.Bluemix_notm}} 청구로 부과됩니다.

{{site.data.keyword.Bluemix_notm}} 사용 주기가 달력 월 기반이므로, 사용자 계정은 비용 계약에 대해 설정된 청구일에 매월 청구됩니다. SoftLayer에서 사용 주기는 SoftLayer가 시작된 시점에서 시작됩니다. 따라서 사용자에게는 매월 SoftLayer 계정에 서명한 날과 동일한 날에 청구됩니다.

{{site.data.keyword.Bluemix_notm}} 사용량이 계속해서 당월 주기에 대해 측정되며 사용자는 {{site.data.keyword.Bluemix_notm}} 송장에서 해당 사용량에 대해 청구됩니다. 다음 달 초에 시작하여, {{site.data.keyword.Bluemix_notm}} 및 SoftLayer 비용은 {{site.data.keyword.Bluemix_notm}} 송장에서 통합됩니다.

예를 들어, 2017년 4월 16일에 계정을 연결한 경우에는 4월 사용량에 대해 {{site.data.keyword.Bluemix_notm}} 송장을 받습니다. 연결된 계정에 따라 SoftLayer 사용량에 대해 별도로 청구될 수 있습니다. 그런 다음 5월 중에 결합된 사용량이 {{site.data.keyword.Bluemix_notm}} 계정을 통해 청구됩니다.

![IBM Cloud 및 SoftLayer 계정 연결 요약](images/IBMCloudSoftLayerBill.svg)

청구서가 연결된 후에 {{site.data.keyword.Bluemix_notm}} 송장은 사용한 각 리소스마다 서로 다른 비용을 나열합니다.

## API 기반 {{site.data.keyword.Bluemix_notm}} 서비스
{: #api-based-services}

다음 목록에는 애플리케이션 코드와 함께 실행되도록 설정할 수 있는 서비스가 포함되어 있습니다. 이러한 서비스의 모든 플랜을 연결 계정에 사용할 수 있는 것은 아닙니다. 종량과금제 및 구독 계정에 사용되는 플랜만 연결된 계정에서 사용할 수 있습니다. 그러나 별도로 청구되는 별도의 {{site.data.keyword.Bluemix_notm}} 계정이 있으면 이러한 서비스에 대해 어떤 플랜이라도 사용할 수 있습니다.

* {{site.data.keyword.alertnotificationshort}}
* {{site.data.keyword.sparks}}
* {{site.data.keyword.appseccloudshort}}
* {{site.data.keyword.blockchain}}
* {{site.data.keyword.cloudant}}
* {{site.data.keyword.iotmapinsights_short}}
* {{site.data.keyword.dashdbshort}}
* {{site.data.keyword.weather_short}}
* {{site.data.keyword.iotdriverinsights_short}}
* {{site.data.keyword.geospatialshort_Geospatial}}
* {{site.data.keyword.iotelectronics}}
* {{site.data.keyword.languagetranslationshort}}
* {{site.data.keyword.messagehub}}
* {{site.data.keyword.nlclassifiershort}}
* {{site.data.keyword.objectstorageshort}}
* {{site.data.keyword.personalityinsightsshort}}
* {{site.data.keyword.servicediscoveryshort}}
* {{site.data.keyword.speechtotextshort}}
* {{site.data.keyword.sqldb}}
* {{site.data.keyword.streaminganalyticsshort}}
* {{site.data.keyword.texttospeechshort}}
* {{site.data.keyword.toneanalyzershort}}
* {{site.data.keyword.visualrecognitionshort}}
* {{site.data.keyword.workloadscheduler}}
