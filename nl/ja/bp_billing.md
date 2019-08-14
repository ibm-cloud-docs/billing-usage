---

copyright:
  years: 2019
lastupdated: "2019-06-20"

keywords: best practice billing, best practice usage, automate billing, track costs

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 請求および使用量に関するベスト・プラクティス
{: #best-practices}

{{site.data.keyword.Bluemix}} でコストを追跡して請求処理を自動化するためのベスト・プラクティスを適用できます。
{:shortdesc}


## タグを追加して関連リソースのコストを追跡する
{:#track-billing-tags}

リソースにタグを追加して、関連リソースのコストを編成、追跡、および管理します。 一貫性のあるタグ付けスキーマを使用して、どのリソースが特定のプロジェクトに結合されているかを識別すると、エクスポートした使用量レポート内でコストを分析する際にそれらのタグでグループ化およびフィルタリングを行うことができます。

1. コスト・センター、データ・センター、プロジェクト、またはチームを差別化するためのタグを作成するなど、一貫性のあるタグ付けスキーマを使用してリソースにタグ付けします。 タグを追加するには、「メニュー」アイコン ![「メニュー」アイコン](../icons/icon_hamburger.svg) > **「リソース・リスト」**の順にクリックします。 「タグ」列で、タグを付けるリソースごとに**「タグの追加」**をクリックします。

   key:value のペアでタグを追加して、使用状況レポートのキーに基づいてカスタム列を追加します。 リソースを編成するために使用するカテゴリーに基づいてキーを作成します。例えば、`costcenter:` を使用して、コスト・センターを基準にしてグループ化したり、`project:` を使用して、プロジェクトを基準にしてグループ化したりします。
   {: tip}

   例えば、1 つのアカウント内に Project ABC と Project XYZ という 2 つのプロジェクトがある場合があります。 Project ABC には、{{site.data.keyword.containershort_notm}} クラスター、数個の Cloud Foundry アプリのデプロイメント、および {{site.data.keyword.cloudant_short_notm}} データベースがあります。 これらのすべてのリソースに `project:abc` タグを追加して、Project ABC 用のこれらのリソースを、`project:xyz` のタグが付いている Project XYZ 内の同様のリソースと区別することができます。

   タグの追加と使用について詳しくは、『[タグの処理](/docs/resources?topic=resources-tag)』を参照してください。

1. インスタンスの使用状況レポートをエクスポートして、タグ付けされたリソースのコストを追跡します。 レポートをエクスポートするには、**「管理」>「請求および使用量」**と進み、**「使用量」**を選択します。 次に、**「CSV のエクスポート」>「インスタンス」**をクリックします。

   インスタンス CSV ファイルの「タグ」列を使用して、アカウント内のリソースの分析に役立ててください。 個々のプロジェクトのコストを詳しく分析できるように、各インスタンスのプロジェクト・タグに従って CSV データをソートすることができます。 key:value のペアを使用してリソースにタグ付けした場合は、使用状況レポート内にキーに対応する列も表示されます。 例えば、`project:abc` と `project:xyz` のタグが付いたリソースは、「プロジェクト」列に `abc` および `xyz` として表示されます。

   詳しくは、[「使用量の表示」](/docs/billing-usage?topic=billing-usage-viewingusage)を参照してください。

## CLI または API を使用して請求および使用量の管理を自動化する
{: #billing-cli-apis}

リソース使用量と関連するコストの確認方法を自動化したい場合は、[`ibmcloud billing`](/docs/cli?topic=cloud-cli-ibmcloud_billing) CLI または [使用量の計量 ![外部リンク・アイコン](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/usage-metering){: new_window} と [使用状況レポート ![外部リンク・アイコン](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/metering-reporting){: new_window} の API を使用して、この機能を独自のアプリに統合することができます。

これらの API の使用を開始するには、[{{site.data.keyword.Bluemix_notm}} usage sample dashboard ![外部リンク・アイコン ](../icons/launch-glyph.svg)](https://github.com/IBM-Cloud/openwhisk-cloud-usage-sample){: new_window} をセットアップします。 サンプルは、{{site.data.keyword.openwhisk}} を使用して API ドリブン・アプローチを実装し、{{site.data.keyword.Bluemix_notm}} の使用量と請求処理データを取得して視覚化します。
{: tip}
