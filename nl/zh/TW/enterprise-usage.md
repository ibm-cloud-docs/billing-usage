---

copyright:
  years: 2019
lastupdated: "2019-07-26"

keywords: enterprise usage, view enterprise costs, account group usage, account usage, cost recovery, chargeback, support cost

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:external: target="_blank" .external}
{:note: .note}


# 在企業中檢視用量
{: #enterprise-usage}

您可以從 {{site.data.keyword.Bluemix}} 企業中的帳戶追縱資源及支援成本，方法為檢視其用量。您可以檢視其用量的帳戶及帳戶群組，視您獲指派的存取權而定。
{: shortdesc}

{{site.data.keyword.Bluemix_notm}} 企業可讓您集中管理多個 {{site.data.keyword.Bluemix_notm}} 帳戶。身為企業使用者，您可以隨時留意企業中任何帳戶的資源用量及關聯成本。請參閱[何謂企業？](/docs/account?topic=account-enterprise)，以取得相關資訊。

## 檢視企業用量所需的存取權
{: #enterprise-usage-access}

在企業中，存取用量資訊是由「企業」服務控制。若要檢視用量資訊，使用者必須受邀加入企業帳戶，並具有「企業」服務的「用量報告檢視者」、「編輯者」或「管理者」角色。「用量報告檢視者」角色只會提供檢視用量報告的存取權，而「編輯者」及「管理者」角色則會啟用其他企業管理動作。在兼顧安全最佳作法下，指派使用者完成其作業所需的最少存取權。如需相關資訊，請參閱[企業動作及角色](/docs/iam?topic=iam-account-services#enterprise-account-management)。

您可以提供使用者精細存取權，讓他們可以檢視特定帳戶或帳戶群組的用量。例如，假設您的企業具有每一個部門的帳戶群組，而且每一個部門具有每一個團隊的帳戶群組。您可以設定存取範圍，讓每一個企業使用者都只能看到履行其工作角色所需的資訊。
   * 您的財務主管需要檢視整個企業的用量，讓他們可以追縱及回復每一個部門的成本，但不需要建立帳戶或帳戶群組。請將企業的「用量報告檢視者」角色指派給他們。
   * 每一個部門領導人都需要檢視其部門的用量，而且他們也需要為其團隊建立並管理帳戶和帳戶群組。請將其部門帳戶群組的「編輯者」角色指派給每一個部門領導人。
   * 每一個團隊領導人都需要檢視其團隊的用量，但您希望他們取得部門核准，以新增帳戶至其團隊。請將其團隊帳戶群組的「用量報告檢視者」角色指派給每一個團隊領導人。他們可以檢視帳戶群組內所有帳戶的用量，但無法檢視部門中其他團隊的帳戶群組用量。

如需指派企業存取權的詳細步驟，請參閱[指派企業存取權](/docs/iam?topic=iam-assign-access-enterprise)。

## 檢視企業用量
{: #enterprise-usage-console}

1. 登入企業帳戶。
1. 移至**管理 > 計費及用量**，然後選取**用量**。

   「用量」頁面會顯示企業中所有資源用量的成本，依帳戶及帳戶群組細分。您也可以檢視整個企業的支援額度用量，以及產生的任何超額。

   現行計費期間不包含標準基礎架構服務的用量資訊。不過，先前的計費期間卻會包含它，因此您可以從**時間範圍**功能表中選取先前的月份來進行檢視。如需相關資訊，請參閱[檢視標準基礎架構資源的用量](/docs/billing-usage?topic=billing-usage-infra-usage)。
1. 若要檢視帳戶群組內的用量，請按一下表格中或**企業層級**功能表中的帳戶群組名稱。與企業層級類似，用量會依帳戶及帳戶群組細分。

   如果帳戶群組未包含任何帳戶，則不會顯示在「用量」頁面上。

1. 若要依資源檢視用量，請按一下表格中的帳戶群組，或從**企業層級**功能表中選取帳戶，以移至帳戶層次。系統會顯示在時間範圍期間使用的每一種資源類型的成本。

   從企業帳戶中，您無法檢視資源方案或實例的用量資料，因為它需要在帳戶內存取。如果您是帳戶中的使用者，請切換至帳戶以檢視此資料。您需要帳戶中資源及服務的計費存取權，如[檢視您的用量](/docs/billing-usage?topic=billing-usage-viewingusage)所述。

只有由企業中帳戶所產生的用量資料，才會顯示在企業帳戶中。若要檢視在帳戶新增至企業之前的用量，請登入該帳戶，並選取相關的時間範圍。
{: note}

### 使用 CLI 檢視企業用量
{: #enterprise-usage-cli}

您可以取得企業、帳戶群組或特定帳戶的用量報告。

1. 登入，並選取企業帳戶。

   ```
   ibmcloud login
   ```
   {:codeblock}

1. 如果您要檢視特定帳戶群組或帳戶的用量，請執行 **`ibmcloud enterprise`** 指令來尋找名稱或 ID。

   例如，下列指令會顯示企業中的所有帳戶群組。

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}

1. 執行 **`ibmcloud billing`** 指令來檢視用量，如下列範例所示。

   * 檢視整個企業的當月用量。

      ```
      ibmcloud billing enterprise-usage
      ```
      {: codeblock}

   * 檢視`開發`帳戶群組 2019 年 7 月的用量。

      ```
      ibmcloud billing enterprise-usage --account-group Development --month 2019-07
      ```
      {:codeblock}

   * 檢視直接位於企業下之帳戶群組及帳戶的用量。

      ```
      ibmcloud billing enterprise-usage --children
      ```
      {:codeblock}

   依預設，指令會以下列格式輸出當月的用量報告。大部分成本都會列為可計費成本。只在極少數情況下，才會列出不可計費成本，例如您新增試用帳戶至企業的月份。

   ```
   Name             Type            Billable Cost   Non-billable Cost   Currency   Month   
Example Corp     account         123.45          0                   USD        2019-07   
Development      account_group   234.56          0                   USD        2019-07   
Marketing        account_group   345.67          0                   USD        2019-07   
Sales            account_group   456.78          0                   USD        2019-07
   ```

   您可以指定 `--output JSON` 選項，以 JSON 格式輸出報告。
   {: tip}

### 使用 API 檢視企業用量
{: #enterprise-usage-api}

您可以呼叫[「企業用量報告 API（測試版）」](https://{DomainName}/apidocs/enterprise-apis/resource-usage-reports){: external}，來取得企業及其帳戶的用量報告。您可以根據企業、帳戶群組或帳戶進行 API 呼叫中的查詢，並指定是要檢視實體還是其子項。「企業用量報告 API」是測試版。

下列範例顯示您可以使用來取得不同用量報告的查詢。當您呼叫 API 時，請將 ID 變數及 IAM 記號取代為您企業的值。

檢視整個企業的當月用量。

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

檢視帳戶群組 2019 年 7 月的用量。

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?account_group_id=$ACCOUNT_GROUP_ID&month=2019-07" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

檢視直接位於企業下之帳戶群組及帳戶的用量。

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID&children=true" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}


## 回復企業用量的成本
{: #enterprise-cost-recovery}

企業會將從其所有帳戶及帳戶群組中的計費合併為單一發票，以簡化計費管理。您可以向關聯的部門或團隊收取每一個帳戶群組或帳戶之用量成本的費用，以從企業中的資源用量回復成本。

若要檢視企業階層及任何用量，您需要整個企業的「企業」服務的「編輯者」或「管理者」角色的存取原則。下列步驟使用 {{site.data.keyword.Bluemix_notm}} 主控台作為範例，但您也可以使用 CLI 或 API 來執行這些步驟。

1. 在企業帳戶中移至**管理 > 用量**，以尋找每一個部門的用量成本。從**時間範圍**功能表中，選取前一個月份，以檢視最新發票中所包括的用量。

  您帳戶群組的成本即會列示在表格中。這些成本包括所有費用，但在計費地區中收取的任何稅金除外。如果您想要進一步細分用量成本，請按一下帳戶群組名稱，以檢視其包含的帳戶及帳戶群組。

1. 識別公司內與帳戶群組對應的部門。

   如果指派給您帳戶群組的聯絡人與您要從中回復成本的部門相關聯，則尋找聯絡人是尋找此資訊的一種方式。請移至**管理 > 企業**，然後選取**帳戶**。每一個帳戶群組的聯絡人即會列示在表格中。

   不過，計費作法會因公司而異。例如，帳戶群組聯絡人可能是與您要收費之部門無關的技術聯絡人。請一律根據貴公司的帳戶處理程序來驗證部門正確無誤。

   如果貴公司使用計費代碼來向部門收取成本的費用，請將計費代碼新增至帳戶群組名稱，以輕鬆地識別此代碼。例如，`Sales - A2B3`。
   {: tip}

1. 將每一個帳戶群組的用量成本與所識別部門配對，然後遵循貴公司的處理程序來提交費用。
