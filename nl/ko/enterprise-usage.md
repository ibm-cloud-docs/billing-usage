---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise usage, view enterprise costs, account group usage, account usage, cost recovery, chargeback, support cost

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:external: target="_blank" .external}
{:note: .note}


# 엔터프라이즈의 사용량 보기
{: #enterprise-usage}

{{site.data.keyword.Bluemix}} 엔터프라이즈에 있는 계정의 사용량을 보고 이들의 리소스 및 지원 비용을 추적할 수 있습니다. 사용량을 볼 수 있는 계정 및 계정 그룹은 지정된 액세스 권한에 따라 달라집니다.
{: shortdesc}

{{site.data.keyword.Bluemix_notm}} 엔터프라이즈는 여러 {{site.data.keyword.Bluemix_notm}} 계정을 중앙 집중식으로 관리할 수 있게 해 줍니다. 엔터프라이즈 사용자는 엔터프라이즈에 속한 계정의 리소스 사용량 및 연관 비용을 감시할 수 있습니다. 자세한 정보는 [엔터프라이즈의 개념](/docs/account?topic=account-enterprise)을 참조하십시오.

## 엔터프라이즈 사용량을 보는 데 필요한 액세스 권한
{: #enterprise-usage-access}

엔터프라이즈에서는 사용량 정보에 대한 액세스가 엔터프라이즈 서비스에 의해 제어됩니다. 사용자가 사용량 정보를 보려면 엔터프라이즈 계정에 초대된 후 엔터프라이즈 서비스에 대한 사용량 보고서 뷰어, 편집자 또는 관리자 역할을 보유해야 합니다. 사용량 보고서 뷰어 역할은 사용량 보고서 보기에 대한 액세스 권한만을 제공하지만, 편집자 및 관리자 역할은 추가 엔터프라이즈 관리 조치를 가능하게 합니다. 보안 우수 사례에 따라, 사용자가 자신의 태스크를 완료하는 데 필요한 액세스 권한만 지정하십시오. 자세한 정보는 [엔터프라이즈 조치 및 역할](/docs/iam?topic=iam-account-services#enterprise-account-management)을 참조하십시오. 

특정 계정 또는 계정 그룹의 사용량을 볼 수 있도록 사용자에게 세부 단위의 액세스 권한을 제공할 수 있습니다. 예를 들면, 어떤 엔터프라이즈에 각 부서에 대한 계정 그룹이 있고, 각 부서에 각 팀에 대한 계정 그룹이 있습니다. 사용자는 각 엔터프라이즈 사용자가 자신의 작업 역할을 수행하는 데 필요한 정보만 볼 수 있도록 액세스 권한의 범위를 지정할 수 있습니다. 
   * 재무 담당자는 각 부서의 비용을 추적하고 회수할 수 있도록 전체 엔터프라이즈의 사용량을 봐야 하지만, 계정 또는 계정 그룹을 작성할 필요는 없습니다. 이들에게는 엔터프라이즈에 대한 사용량 보고서 뷰어 역할을 지정하십시오. 
   * 각 부서 책임자는 해당 부서의 사용량을 봐야 하며, 동시에 해당 팀의 계정 및 계정 그룹을 작성하고 관리해야 합니다. 각 부서 책임자에게는 해당 부서의 계정 그룹에 대한 편집자 역할을 지정하십시오. 
   * 각 팀 책임자는 해당 팀의 사용량을 봐야 하지만, 여기서는 해당 팀에 새 계정을 추가하기 위해 부서 승인을 받도록 하려 합니다. 각 팀 책임자에게 해당 팀의 계정 그룹에 대한 사용량 보고서 뷰어 역할을 지정하십시오. 이들은 해당 계정 그룹에 속한 모든 계정의 사용량을 볼 수 있지만, 부서의 다른 팀에 속한 계정 그룹의 사용량은 볼 수 없습니다. 

엔터프라이즈 액세스 권한 지정의 자세한 단계는 [엔터프라이즈 액세스 권한 지정](/docs/iam?topic=iam-assign-access-enterprise)을 참조하십시오. 

## 엔터프라이즈 사용량 보기
{: #enterprise-usage-console}

1. 엔터프라이즈 계정에 로그인하십시오. 
1. **관리 > 청구 및 사용량**으로 이동하여 **사용량**을 선택하십시오.

   사용량 페이지는 엔터프라이즈의 모든 리소스 사용량에 대한 비용을 계정 및 계정 그룹으로 구분하여 표시합니다. 전체 엔터프라이즈의 지원 크레딧 사용량과 발생한 초과 비용 또한 볼 수 있습니다. 

   클래식 인프라 서비스의 사용량 정보는 현재 청구 기간에 대해 포함되지 않습니다. 그러나 이는 이전 청구 기간에 대해 포함되며, **시간 범위** 메뉴에서 이전 월을 선택하여 볼 수 있습니다. 자세한 정보는 [클래식 인프라 리소스의 사용량 보기](/docs/billing-usage?topic=billing-usage-infra-usage)를 참조하십시오. 
1. 계정 그룹의 사용량을 보려면 테이블 또는 **엔터프라이즈 레벨** 메뉴에서 계정 그룹 이름을 클릭하십시오. 엔터프라이즈 레벨과 마찬가지로, 사용량은 계정 및 계정 그룹으로 구분됩니다. 

   계정을 포함하지 않는 계정 그룹은 사용량 페이지에 표시되지 않습니다. 

1. 리소스별 사용량을 보려면 테이블에서 계정 그룹을 클릭하거나 **엔터프라이즈 레벨** 메뉴에서 계정을 선택하여 계정 레벨로 이동하십시오. 해당 시간 범위 동안 사용된 각 리소스 유형에 대한 비용이 표시됩니다. 

   엔터프라이즈 계정에서는 리소스 플랜 또는 인스턴스에 대한 사용량 데이터를 볼 수 없으며, 이를 위해서는 해당 계정 자체에 대한 액세스 권한이 필요합니다. 사용자가 해당 계정의 사용자인 경우에는 이 데이터를 보려면 해당 계정으로 전환하십시오. 이를 수행하려면 [사용량 보기](/docs/billing-usage?topic=billing-usage-viewingusage)에 설명되어 있는 바와 같이 해당 계정의 리소스 및 서비스에 대한 청구 액세스 권한이 필요합니다. 

엔터프라이즈 계정에서는 엔터프라이즈의 계정에 의해 발생한 사용량에 대한 데이터만 표시됩니다. 계정이 엔터프라이즈에 추가되기 전의 사용량을 보려면 해당 계정에 로그인하여 관련 시간 범위를 선택하십시오.
{: note}

### CLI를 사용한 엔터프라이즈 사용량 보기
{: #enterprise-usage-cli}

사용자는 엔터프라이즈, 계정 그룹, 또는 특정 계정의 사용량에 대한 보고서를 얻을 수 있습니다. 

1. 로그인하여 엔터프라이즈 계정을 선택하십시오. 

   ```
ibmcloud login
   ```
   {:codeblock}

1. 특정 계정 그룹 또는 계정의 사용량을 보려면 **`ibmcloud enterprise`** 명령을 실행하여 이름 또는 ID를 찾으십시오. 

   예를 들면, 다음 명령은 엔터프라이즈에 있는 모든 계정을 표시합니다. 

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}

1. 다음 예에 표시되어 있는 바와 같이 **`ibmcloud billing`** 명령을 실행하여 사용량을 보십시오. 

   * 전체 엔터프라이즈의, 현재 월의 사용량을 봅니다. 

      ```
      ibmcloud billing enterprise-usage
      ```
      {: codeblock}

   * `Development` 계정 그룹의, 2019년 7월의 사용량을 봅니다. 

      ```
      ibmcloud billing enterprise-usage --account-group Development --month 2019-07
      ```
      {:codeblock}

   * 엔터프라이즈 바로 아래에 있는 계정 그룹 및 계정의 사용량을 봅니다. 

      ```
      ibmcloud billing enterprise-usage --children
      ```
      {:codeblock}

   기본적으로 이 명령은 현재 월의 사용량 보고서를 다음 형식으로 출력합니다. 대부분의 비용은 청구 가능 비용으로 나열됩니다. 청구 불가능 비용은 엔터프라이즈에 평가판 계정을 추가한 월과 같이 매우 드문 경우에만 나열됩니다. 

   ```
   Name             Type            Billable Cost   Non-billable Cost   Currency   Month   
Example Corp     account         123.45          0                   USD        2019-07   
Development      account_group   234.56          0                   USD        2019-07   
Marketing        account_group   345.67          0                   USD        2019-07   
Sales            account_group   456.78          0                   USD        2019-07
   ```

   `--output JSON` 옵션을 지정하여 보고서를 JSON 형식으로 출력할 수 있습니다.
   {: tip}

### API를 사용한 엔터프라이즈 사용량 보기
{: #enterprise-usage-api}

<!-- [Enterprise Usage Reports API (Beta)](https://{DomainName}/apidocs/enterprise-apis/resource-usage-reports){: external} --> 엔터프라이즈 사용량 보고서 API(베타)를 호출하여 엔터프라이즈 및 해당 계정으로부터 사용량 보고서를 얻을 수 있습니다. API 호출에서 엔터프라이즈, 계정 그룹 또는 계정으로 조회의 범위를 지정하고 해당 엔티티만 볼지, 또는 해당 하위도 볼지 지정할 수 있습니다. 엔터프라이즈 사용량 보고서 API는 베타 릴리스입니다. 

다음 예는 다양한 사용량 보고서를 얻기 위해 사용할 수 있는 조회를 보여줍니다. 이 API를 호출할 때는 ID 변수 및 IAM 토큰을 자신의 엔터프라이즈의 값으로 대체하십시오. 

전체 엔터프라이즈의, 현재 월의 사용량을 봅니다. 

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

특정 계정 그룹의, 2019년 7월의 사용량을 봅니다. 

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?account_group_id=$ACCOUNT_GROUP_ID&month=2019-07" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

엔터프라이즈 바로 아래에 있는 계정 그룹 및 계정의 사용량을 봅니다. 

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID&children=true" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}


## 엔터프라이즈 사용량에 대한 비용 회수
{: #enterprise-cost-recovery}

엔터프라이즈는 모든 해당 계정 그룹 및 계정의 청구를 하나의 청구서로 통합하여 청구 관리를 간소화합니다. 각 계정 그룹 또는 계정의 사용량 비용을 연관 부서 또는 팀에 청구하여 엔터프라이즈의 리소스 사용량에 대한 비용을 회수할 수 있습니다. 

엔터프라이즈 계층 구조 및 사용량을 보려면 전체 엔터프라이즈에 관한 엔터프라이즈 서비스에 대한 편집자 또는 관리자 역할이 있는 액세스 정책이 필요합니다. 다음 단계에서는 {{site.data.keyword.Bluemix_notm}} 콘솔을 예로 사용하지만, CLI 또는 API를 사용하여 이러한 단계를 수행할 수도 있습니다. 

1. 엔터프라이즈 계정에서 **관리 > 사용량**으로 이동하여 각 부서의 사용량 비용을 찾으십시오. **시간 범위** 메뉴에서 이전 월을 선택하여 최신 청구서에 포함된 사용량을 보십시오. 

  계정 그룹에 대한 비용이 테이블에 나열됩니다. 이러한 비용은 사용자의 청구 지역에서 부과되는 세금을 제외한 모든 비용을 포함합니다. 사용량 비용을 더 세부적으로 보려는 경우에는 계정 그룹 이름을 클릭하여 여기에 포함된 계정 그룹 및 계정을 보십시오. 

1. 회사에서 계정 그룹에 해당하는 부서를 식별하십시오. 

   계정 그룹에 지정된 담당자가 비용을 회수할 부서와 연관되어 있는 경우에는 해당 담당자를 찾아 이 정보를 찾을 수 있습니다. **관리 > 엔터프라이즈**로 이동하여 **계정**을 선택하십시오. 각 계정 그룹의 담당자가 테이블에 나열되어 있습니다. 

   그러나 청구 처리는 회사마다 다르게 이뤄집니다. 예를 들면, 계정 그룹 담당자가 비용을 청구할 부서와 연관되지 않은 기술 관련 담당자인 경우가 있습니다. 항상 회사의 회계 프로세스에 따라 올바른 부서를 확인하십시오. 

   회사가 청구 코드를 사용하여 부서에 비용을 재청구하는 경우에는 청구 코드를 쉽게 식별할 수 있도록 코드를 계정 그룹 이름에 추가하십시오. 예를 들면 `Sales - A2B3`와 같습니다.
   {: tip}

1. 각 계정 그룹의 사용량 비용을 식별된 부서와 짝지은 후 회사의 프로세스에 따라 비용을 청구하십시오. 
