---

copyright:

  years: 2015, 2018

lastupdated: "2018-04-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# 如何計算成本
{: #cost}

您可以使用不同方法來預估使用 {{site.data.keyword.Bluemix}} 平台即服務 (PaaS) 和基礎架構即服務 (IaaS) 資源，以建置及管理應用程式的成本。
{:shortdesc}

您可以使用下列方法來判定您的成本：
* 使用[定價計算機 ![外部鏈結圖示](../icons/launch-glyph.svg)](https://console.bluemix.net/pricing/){: new_window} 來預估您要使用的平台和基礎架構資源的總成本。
* 使用 {{site.data.keyword.Bluemix_notm}} {{site.data.keyword.pricing_sheet}} 上的成本預估器，查看根據您的應用程式大小的約略成本預估。
* 使用「定價」頁面上的成本計算機，查看根據您輸入的運行環境及服務用量的正確應用程式價格。
* 手動計算成本。

## 使用定價計算機
{: #pricing-calculator}

購買前，您可以使用定價計算機來預估平台及許多基礎架構資源的成本。定價計算機提供下列功能：
  * 目前以美元貨幣提供的成本預估。
  * 目前提供於**運算**及**容器**種類的基礎架構資源預估。
  * 目前未包含折扣之資源的成本預估。
  * 成本預估是為了規劃之用而提供。

1. 使用下列其中一種方式來存取定價計算機：
  * 從「探索我們的解決方案」一節的[定價頁面 ![外部鏈結圖示](../icons/launch-glyph.svg)](https://www.ibm.com/cloud/pricing){: new_window}，按一下**試用計算機**。
  * 如果您目前未登入 {{site.data.keyword.Bluemix_notm}}，請從 [{{site.data.keyword.Bluemix_notm}} 首頁 ![外部鏈結圖示](../icons/launch-glyph.svg)](https://console.bluemix.net/) 按一下**定價**。
2. 從**基礎架構**或**平台**清單中，選取您要詢價的資源種類。會顯示種類中的資源，您也可以在種類中搜尋特定資源。
3. 選取種類中的資源以查看其說明。部分資源具有多個選項。例如，如果您選取**基礎架構** > **運算** > **裸機伺服器**，您可以從伺服器清單中選擇。
4. 選取要新增的資源數量。
5. 按一下**新增至預估**。
6. 繼續從**基礎架構**和**平台**種類新增資源，直到您新增完要預估的項目為止。**預估**畫面會顯示您新增的資源、每一項的價格，以及總價。

如果您只針對平台資源進行詢價，可以按一下**尋找標準計算機？**，用 USD 以外的貨幣查看預估。標準計算機不包括基礎架構資源。
{: tip}

### 針對平台資源使用標準計算機
{: #calculator}

若要以 USD 以外的貨幣計算平台資源成本，您可以使用標準計算機。標準計算機不會提供基礎架構資源的定價預估。

1. 移至 {{site.data.keyword.Bluemix_notm}} {{site.data.keyword.pricing_sheet}}。
2. 選取基礎架構中的其中一個選項，以支援所有工作負載區段。

若要使用計算機，請鍵入所列出資源的預測每月用量；例如，實例數或推送通知數。計算機會立即顯示輸入值的價格。您也可以調整計算機以顯示每年成本，而非每月成本。

## 手動計算成本
{: #manual}

您可能要自行估計 {{site.data.keyword.Bluemix_notm}} 成本，以更充分地瞭解 {{site.data.keyword.Bluemix_notm}} 成本的計算方式。您可以透過考量應用程式所使用運行環境及服務的價格，來計算使用 {{site.data.keyword.Bluemix_notm}} 建置及管理應用程式的總價格。運行環境及服務的價格有時會變更，因此，您必須在計算總價格時參照 {{site.data.keyword.Bluemix_notm}} 定價單的最新資訊。

## 支援的計費貨幣

下表列出可用的計費貨幣。

|ISO 4217 代碼| 貨幣|
|-------------|---------|
|AUD|	  澳幣|
|BRL|	  巴西小銀幣|
|CAD|	  加拿大幣|
|CHF|	  瑞士法郎|
|DKK|	  丹麥克朗|
|EUR|	  歐元|
|GBP|	  英鎊|
|INR|	  印度盧比|
|JPY|	  日圓|
|KRW|	  韓圜|
|NOK|	  挪威克朗|
|NZD|	  紐元|
|SEK|	  瑞典克朗|
|USD|    美元|
|ZAR|	  南非幣|
{:caption="表 1. 支援的貨幣" caption-side="top"}

如果您已鏈結 {{site.data.keyword.Bluemix_notm}} 與 SoftLayer 帳戶，則所收到的單一發票的計價單位僅為美元 (USD)。如需相關資訊，請參閱[已鏈結帳戶的合併計費](/docs/account/linking_accounts.html)。
{: tip}
