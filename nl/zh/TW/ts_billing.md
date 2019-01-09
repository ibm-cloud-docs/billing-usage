---



copyright:

  years: 2017, 2018
lastupdated: "2018-11-16"

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

這是因為您沒有檢視帳戶計費資訊的權限。您必須是帳戶擁有者、Cloud Foundry 組織帳單管理員，或是對所有帳戶管理服務具有 IAM 原則並且已指派管理者角色。
{: tsCauses}

您可以檢視您身為帳戶擁有者之任何帳戶的計費資訊。帳單管理員可以檢視 Cloud Foundry 組織的計費資訊。此外，針對已啟用 IAM 的資源，您必須對所有帳戶管理服務具有 IAM 原則並且已指派管理者角色。 

請完成下列步驟來檢查您的存取權： 

  1. 移至**管理** > **存取 (IAM)**，然後選取**使用者**。 
  2. 從「使用者」頁面中，按一下您的名稱。
  3. 按一下**存取原則**，以檢視您的已指派 IAM 存取原則。
  4. 按一下 **Cloud Foundry 存取**，然後展開所指派組織的橫列，以查看您是否有「帳戶擁有者」或「帳單管理者」角色。

如需 IAM 存取的相關資訊，請參閱 [Cloud IAM 角色](/docs/iam/users_roles.html#userroles)。如需 Cloud Foundry 存取的相關資訊，請參閱 [Cloud Foundry 角色](/docs/iam/cfaccess.html#cfaccess)。
{: tsResolve}
