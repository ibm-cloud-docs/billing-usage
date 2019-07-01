---

copyright:
  years: 2019
lastupdated: "2019-06-18"

keywords: best practice billing, best practice usage, automate billing, track costs

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 청구 및 사용량에 대한 우수 사례
{: #best-practices}

우수 사례에 따라 {{site.data.keyword.Bluemix}}에서 비용을 추적하고 청구를 자동화하십시오.
{:shortdesc}


## 태그를 추가하여 연관된 리소스에 대한 비용 추적
{:#track-billing-tags}

관련 리소스에 대한 비용을 구성, 추적 및 관리할 리소스에 태그를 추가하십시오. 어떤 리소스가 특정 프로젝트에 연관되어 있는지 식별하기 위해 일치 태그 지정 스키마를 사용하는 경우, 내보낸 사용량 보고서 내의 비용을 분석할 때 해당 태그 기준으로 그룹화하고 필터링할 수 있습니다.

1. 일치 태그 지정 스키마를 사용하여 리소스에 태그를 지정하십시오. 예를 들어, 비용 센터, 데이터 센터, 프로젝트 또는 팀을 차별화하기 위한 태그를 작성할 수 있습니다. 태그를 추가하려면 메뉴 아이콘 ![메뉴 아이콘](../icons/icon_hamburger.svg) > **리소스 목록**을 클릭하십시오. 태그 열에서 태그를 지정할 각 리소스에 대해 **태그 추가**를 클릭하십시오.

   키:값 쌍에 태그를 추가하여 사용량 보고서 내의 키를 기반으로 하여 사용자 정의 열을 추가하십시오. 리소스를 구성하는 데 사용하는 카테고리를 기반으로 하여 키를 작성하십시오. 예를 들어, `costcenter:`를 사용하여 비용 센터를 그룹화하거나 `project:` 사용하여 프로젝트를 그룹화하십시오. {: tip}

   예를 들어, 단일 계정에 프로젝트 ABC 및 프로젝트 XYZ라는 두 개의 프로젝트에 대한 리소스가 있을 수 있습니다. 프로젝트 ABC에는 {{site.data.keyword.containershort_notm}} 클러스터, 몇 가지 Cloud Foundry 앱 배치 및 {{site.data.keyword.cloudant_short_notm}} 데이터베이스가 있습니다. 이러한 모든 자원에 `project:abc` 태그를 추가하여 프로젝트 ABC에 대한 해당 리소스를 `project:xyz`라는 태그가 지정된 프로젝트 XYZ의 유사한 리소스와 구별할 수 있습니다.

   태그 추가 및 사용에 대한 자세한 정보는 [태그에 대한 작업](/docs/resources?topic=resources-tag)을 참조하십시오.

1. 인스턴스에 대한 사용량 보고서를 내보내는 방법으로 태그가 지정된 리소스에 대한 비용을 추적하십시오. 보고서를 내보내려면 **관리 > 청구 및 사용량**으로 이동하여 **사용량**을 선택하십시오. 그런 다음 **CSV 내보내기 > 인스턴스**를 클릭하십시오.

   인스턴스 CSV 파일에서 태그 열을 사용하여 계정 내의 리소스 분석에 도움을 받을 수 있습니다. 각 인스턴스의 프로젝트 태그에 따라 CSV 데이터를 정렬하여 개별 프로젝트의 비용을 더 잘 분석할 수 있습니다. 키:값 쌍을 사용하여 리소스에 태그를 지정한 경우, 키에 해당되는 사용량 보고서 내의 열을 볼 수도 있습니다. 예를 들어, `project:abc` 및 `project:xyz`라는 태그가 지정된 리소스는 프로젝트 열에 "abc" 및 "xyz"로 표시됩니다.

   자세한 정보는 [사용량 보기](/docs/billing-usage?topic=billing-usage-viewingusage)를 참조하십시오.

## CLI 또는 API를 사용하여 청구 및 사용량 관리 자동화
{: #billing-cli-apis}

리소스 사용량 및 연관된 임의의 비용을 검토하는 방법을 자동화하려면 [`ibmcloud billing`](/docs/cli?topic=cloud-cli-ibmcloud_billing) CLI 또는 [사용량 측정 ![외부 링크 아이콘](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/usage-metering){: new_window} 및 [사용량 보고서 ![외부 링크 아이콘](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/metering-reporting){: new_window} API를 사용하여 이 기능을 사용자 소유의 앱에 통합할 수 있습니다.

API 사용을 시작하려면 [{{site.data.keyword.Bluemix_notm}} 사용량 샘플 대시보드 ![외부 링크 아이콘](../icons/launch-glyph.svg)](https://github.com/IBM-Cloud/openwhisk-cloud-usage-sample){: new_window}를 설정하십시오. 샘플의 경우, {{site.data.keyword.openwhisk}}를 사용하여 API 주도적인 접근법을 구현하여 {{site.data.keyword.Bluemix_notm}} 사용량 및 청구 데이터를 얻고 시각화합니다.
{: tip}
