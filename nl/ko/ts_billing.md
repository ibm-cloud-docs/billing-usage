---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-11"

keywords: troubleshoot billing, billing error, payment error, error message, feature code, subscription code

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# 청구 및 사용량 관리 문제점 해결
{: #troubleshoot}

청구 및 사용량 관리의 일반 문제점에는 청구 정보에 액세스하기 위한 필수 권한이 포함될 수 있습니다. 대부분의 경우에는 약간의 간단한 단계를 거쳐 문제점에서 복구할 수 있습니다.
{:shortdesc}


## 청구 정보에 액세스할 수 없는 이유
{: #cannot-access-billing-info}
{: troubleshoot}

결제 및 송장과 같은 청구 정보에 액세스하려 시도하면 해당 기능을 사용할 수 없다는 메시지가 수신됩니다.
{: tsSymptoms}

계정에 대한 청구 정보를 볼 권한이 없으면 이 메시지가 수신됩니다. 계정 소유자 또는 Cloud Foundry 조직 청구 관리자이거나 관리자 역할이 지정된 모든 계정 관리 서비스에 대한 IAM 정책이 있어야 합니다.
{: tsCauses}

자신이 계정 소유자인 계정에 대한 청구 정보를 볼 수 있습니다. 청구 관리자는 Cloud Foundry 조직에 대한 청구 정보를 볼 수 있습니다. 또한 IAM 사용 리소스의 경우 관리자 역할이 지정된 모든 계정 관리 서비스에 대한 IAM 정책이 있어야 합니다.

다음 단계를 완료하여 액세스를 확인하십시오.

  1. **관리 > 액세스(IAM)**로 이동하여 **사용자**를 선택하십시오.
  2. 사용량 페이지에서 해당 이름을 클릭하십시오.
  3. **액세스 정책**을 클릭하여 지정된 IAM 액세스 정책을 보십시오.
  4. **Cloud Foundry 액세스**를 클릭하고 지정된 조직에 대한 행을 펼쳐서 계정 소유자 또는 청구 관리자 역할을 보유 중인지 여부를 확인하십시오.

IAM 액세스에 대한 자세한 정보는 [Cloud IAM 역할](/docs/iam?topic=iam-userroles)을 참조하십시오. 또한 Cloud Foundry 액세스에 대한 자세한 정보는 [Cloud Foundry 역할](/docs/iam?topic=iam-cfaccess)을 참조하십시오.
{: tsResolve}


## 기능 코드를 적용할 수 없는 이유가 무엇입니까?
{: #cannot-apply-feature-code}
{: troubleshoot}

기능 코드를 적용하려는 경우 코드를 적용할 수 없다는 오류가 표시됩니다.
{: tsSymptoms}

계정은 기능 코드의 요구사항을 충족시키지 않거나 계정에 필요한 액세스 레벨이 없습니다.
{: tsCauses}

- 올바른 계정 유형을 보유하고 있는지 확인합니다. 예를 들어, 교육 목적의 프로모션을 위한 일부 기능 코드는 Lite 계정에서만 적용됩니다. 계정 유형을 보려면 **관리 > 계정**으로 이동하여 **계정 설정**을 선택하십시오. 세부사항은 [기능 코드 적용](/docs/account?topic=account-codes)을 참조하십시오.
- 계정 코드를 적용할 수 있는 액세스 권한을 보유하고 있는지 확인합니다. 기능 코드를 적용하려면 모든 계정 관리 서비스에서 편집자 역할 이상을 보유하고 있어야 합니다. 역할을 검토하거나 변경하려면 [계정 관리 서비스에 대한 액세스 권한 지정](/docs/iam?topic=iam-account-services)을 참조하십시오.
{: tsResolve}
