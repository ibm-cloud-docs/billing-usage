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


# 管理計費及用量的疑難排解
{: #troubleshoot}

管理計費及用量的一般問題可能包含存取您計費資訊的必要權限。在許多情況下，您可以遵照一些簡單的步驟，從問題回復。
{:shortdesc}


## 為什麼我無法存取計費資訊？
{: #cannot-access-billing-info}
{: troubleshoot}

當您嘗試存取計費資訊（例如付款和發票）時，會出現訊息指出無法使用該功能。
{: tsSymptoms}

出現此訊息是因為您沒有檢視帳戶計費資訊的權限。您必須是帳戶擁有者、Cloud Foundry 組織帳單管理員，或是對所有帳戶管理服務具有 IAM 原則並且已指派管理者角色。
{: tsCauses}

您可以檢視您身為帳戶擁有者之任何帳戶的計費資訊。帳單管理員可以檢視 Cloud Foundry 組織的計費資訊。此外，針對已啟用 IAM 的資源，您必須對所有帳戶管理服務具有 IAM 原則並且已指派管理者角色。

請完成下列步驟來檢查您的存取權：

  1. 移至**管理 > 存取 (IAM)**，然後選取**使用者**。
  2. 從「使用者」頁面中，按一下您的名稱。
  3. 按一下**存取原則**，以檢視您的已指派 IAM 存取原則。
  4. 按一下 **Cloud Foundry 存取權**，然後展開所指派組織的橫列，以查看您是否有「帳戶擁有者」或「帳單管理者」角色。

如需 IAM 存取的相關資訊，請參閱 [Cloud IAM 角色](/docs/iam?topic=iam-userroles)。如需 Cloud Foundry 存取權的相關資訊，請參閱 [Cloud Foundry 角色](/docs/iam?topic=iam-cfaccess)。
{: tsResolve}


## 為什麼無法套用特性碼？
{: #cannot-apply-feature-code}
{: troubleshoot}

當您嘗試套用特性碼時，會看到指出無法套用代碼的錯誤。
{: tsSymptoms}

您的帳戶不符合特性碼的需求，或您沒有帳戶中的必要存取層次。
{: tsCauses}

- 驗證您具有正確的帳戶類型。例如，教育促銷的部分特性碼僅適用於「精簡」帳戶。若要檢視您的帳戶類型，請移至**管理 > 帳戶**，然後選取**帳戶設定**。如需詳細資料，請參閱[套用特性碼](/docs/account?topic=account-codes)。
- 驗證您有權套用特性碼。若要套用任何特性碼，您必須具有所有帳戶管理服務的「編輯者」角色或更高角色。若要檢閱或變更角色，請參閱[指派帳戶管理服務的存取權](/docs/iam?topic=iam-account-services)。
{: tsResolve}
