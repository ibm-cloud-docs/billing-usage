---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-28"

keywords: view usage, view cost, service usage, usage access, usage report

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# 檢視用量
{: #viewingusage}

您可以從 {{site.data.keyword.Bluemix}} 主控台的「用量」頁面檢視您的用量詳細資料，包括組織中每個月使用的所有資源、服務和支援方案的預估費用摘要。
{:shortdesc}

帳單管理員只能看到他們被指派了「帳單管理員」角色之組織的詳細資料。
{: note}


## 檢視用量許可權
{: #view-usage-permissions}

針對 Cloud Foundry 所管理的資源，必須在組織層次套用「帳單管理員」角色。若要查看 {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) 資源用量，必須將「檢視者」角色套用至資源群組。如需許可權角色的相關資訊，請參閱 [IAM 存取](/docs/iam?topic=iam-userroles)、[Cloud Foundry 存取權](/docs/iam?topic=iam-cfaccess)或[標準基礎架構許可權](/docs/iam?topic=iam-infrapermission)。

## 檢視服務用量詳細資料
{: #services}

在服務區段中，您可以檢視服務清單以及與這些服務相關聯的預估成本。若要檢視特定資源之所有實例的預估費用摘要，請完成下列步驟：

1. 移至**管理 > 計費及用量**，然後選取**用量**。
2. 按一下**檢視實例**，以檢視特定資源類型的所有實例。  
3. 若要查看特定資源類型之每個實例的預估費用詳細摘要，請按一下**檢視實例詳細資料**。您也可以查看所選取實例的詳細每月用量度量值。

在每一個計費週期結束時，會針對在所有組織發生的用量總計，向帳戶擁有者收取費用。每個計費週期為期一個月。

帳戶擁有者可以依群組來過濾用量摘要，及選取用量的時間範圍。顯示的費用代表您（帳戶擁有者）該月份的帳單金額。

如果您從**依群組過濾**清單選取特定組織，則可以看到該組織的用量總計，包括免費層級的任何用量。免費層級用量在帳戶層次會顯示為免費，但在組織層次則不是。當您檢視組織用量時，會看到該組織的實際用量，這同時包括免費和收費用量。在移除免費層級之後，所有組織用量都會累積更新至帳戶用量。

「隨收隨付制」帳戶的帳戶管理員可以針對帳戶、運行環境、服務和個別服務（不包括協力廠商服務）的總成本，設定消費通知。如需相關資訊，請參閱[設定消費通知](/docs/billing-usage?topic=billing-usage-spending)。

## 將用量詳細資料匯出成 `.csv` 檔案
{: #export-csv}

您可以將用量摘要或是服務和實例的相關資訊匯出成 CSV 檔案。匯出 CSV 檔案後，您可以輕鬆找到每個資源的用量和成本預估資訊，以向客戶扣款或進一步瞭解您的成本。

1. 移至**管理 > 計費及用量**，然後選取**用量**。
2. 按一下**匯出 CSV**。  
