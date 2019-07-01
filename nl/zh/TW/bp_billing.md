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


# 計費及用量最佳作法
{: #best-practices}

遵循我們在 {{site.data.keyword.Bluemix}} 中追蹤成本和自動計費的最佳作法。
{:shortdesc}


## 透過新增標籤追蹤相關資源的成本
{:#track-billing-tags}

將標籤新增到資源以組織、追蹤和管理相關資源的成本。當您使用一致的標籤綱目來識別哪些資源與特定專案相關時，您可以在匯出的使用報告中分析成本時按標籤分組和過濾。

1. 使用一致的標籤綱目（例如建立標籤以區分成本中心、資料中心、專案或團隊）來標籤資源。要新增標籤，請按一下「功能表」圖示 ![「功能表」圖示](../icons/icon_hamburger.svg) > **資源清單**。在「標籤」直欄中，對要進行標籤的每個資源按一下**新增標籤**。

   使用「索引鍵:值」配對新增標籤，以根據用量報告中的索引鍵新增自訂直欄。根據用於組織資源的種類建立索引鍵，例如使用 `costcenter:` 以按成本中心分組，或使用 `project:` 以按專案分組。
   {: tip}

   例如，您可能具有用於單一帳戶中的兩個專案（專案 ABC 和專案 XYZ）的資源。專案 ABC 具有一個 {{site.data.keyword.containershort_notm}} 叢集、一些 Cloud Foundry 應用程式部署和一個 {{site.data.keyword.cloudant_short_notm}} 資料庫。您可以將 `project:abc` 標籤新增到所有這些資源，以識別專案 ABC 的這些資源與專案 XYZ 中標籤為 `project:xyz` 的類似資源。

   有關新增和使用標籤的相關資訊，請參閱[使用標籤](/docs/resources?topic=resources-tag)。

1. 透過匯出實例的用量報告來追蹤已標記資源的成本。要匯出報告，請移至**管理 > 計費及用量**，並選取**用量**。然後，按一下**匯出 CSV > 實例**。

   使用實例 CSV 檔案中的「標籤」直欄來說明分析帳戶中的資源。您可以根據每個實例上的專案標籤對 CSV 資料分類，以便您可以更妥善地分析個別專案的成本。如果您使用「索引鍵:值」配對標記了資源，則您還將在用量報告中看到與索引鍵配對應的直欄。例如，標記了 `project:abc` 的資源和標記了 `project:xyz` 的資源，在「專案」直欄中分別顯示為 abc 和 xyz。

   如需相關資訊，請參閱[檢視用量](/docs/billing-usage?topic=billing-usage-viewingusage)。

## 使用 CLI 或 API 進行自動計費和用量管理
{: #billing-cli-apis}

如果您想要自動化資源用量和任何相關成本的檢閱方式，可以使用 [`ibmcloud billing`](/docs/cli?topic=cloud-cli-ibmcloud_billing) CLI 或[用量計量 ![外部鏈結圖示](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/usage-metering){: new_window} 和[用量報告 ![外部鏈結圖示](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/metering-reporting){: new_window} API 來將此功能整合到您自己的 APP 中。

要開始使用這些 API，請設定 [{{site.data.keyword.Bluemix_notm}} 用量範例儀表板 ![外部鏈結圖示](../icons/launch-glyph.svg)](https://github.com/IBM-Cloud/openwhisk-cloud-usage-sample){: new_window}。使用 {{site.data.keyword.openwhisk}}，範例實作了 API 驅動的方法來取得和視覺化 {{site.data.keyword.Bluemix_notm}} 用量和計費資料。
{: tip}
