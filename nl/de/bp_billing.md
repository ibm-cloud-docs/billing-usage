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


# Best Practices für Abrechnung und Nutzung
{: #best-practices}

Folgen Sie unseren Best Practices für die Verfolgung von Kosten und zur automatischen Fakturierung in {{site.data.keyword.Bluemix}}.
{:shortdesc}


## Kosten für verwandte Ressourcen durch Hinzufügen von Tags verfolgen
{:#track-billing-tags}

Sie können Ihren Ressourcen Tags hinzufügen, um die Kosten für verwandte Ressourcen zu organisieren, zu verfolgen und zu verwalten. Wenn Sie ein konsistentes Tagging-Schema verwenden, um zu kennzeichnen, welche Ressourcen an bestimmte Projekte gebunden sind, können Sie diese Tags bei der Analyse der Kosten innerhalb Ihres exportierten Nutzungsberichts gruppieren und filtern.

1. Taggen Sie Ihre Ressourcen anhand eines konsistenten Tagging-Schemas, z. B. mit Tags zur Unterscheidung verschiedener Kostenstellen, Rechenzentren, Projekte oder Teams. Zum Hinzufügen von Tags klicken Sie auf das Menüsymbol ![Menüsymbol](../icons/icon_hamburger.svg) > **Ressourcenliste**. In der Tagspalte klicken Sie auf **Tag hinzufügen** für jede Ressource, die mit einem Tag versehen werden soll.

   Fügen Sie Tags in Form von Schlüssel/Werte-Paaren hinzu, um angepasste Spalten auf Grundlage des Schlüssels im Nutzungsbericht hinzuzufügen. Erstellen Sie Schlüssel auf Grundlage der Kategorien, mit denen Sie Ihre Ressourcen organisieren, z. B. unter Verwendung von `costcenter:`, um nach Kostenstelle zu gruppieren, oder `project:`, um nach Projekt zu gruppieren.
   {: tip}

   Beispiel: Sie haben Ressourcen für zwei Projekte in einem einzigen Konto, nämlich Projekt ABC und Projekt XYZ. Projekt ABC hat einen {{site.data.keyword.containershort_notm}}-Cluster, einige Cloud Foundry-App-Bereitstellungen und eine {{site.data.keyword.cloudant_short_notm}}-Datenbank. Sie können das Tag `project:abc` zu allen diesen Ressourcen hinzufügen, um diese Ressourcen für Projekt ABC von ähnlichen Ressourcen in Projekt XYZ zu unterscheiden, die ihrerseits mit `project:xyz` getaggt sind.

   Weitere Informationen zum Hinzufügen und zur Verwendung von Tags finden Sie unter [Mit Tags arbeiten](/docs/resources?topic=resources-tag).

1. Sie können die Kosten für die getaggten Ressourcen verfolgen, indem Sie den Nutzungsbericht für Ihre Instanzen exportieren. Zum Exportieren des Berichts wechseln Sie zu **Verwalten > Abrechnung und Nutzung** und wählen Sie **Nutzung** aus. Anschließend klicken Sie auf **CSV exportieren > Instanz**.

   Mithilfe der Tagspalte in der CSV-Datei der Instanz können Sie die Ressourcen in Ihrem Konto leichter analysieren. Sie können die CSV-Daten gemäß den Projekt-Tags der einzelnen Instanzen sortieren, sodass Sie die Kosten eines einzelnen Projekts besser analysieren können. Wenn Sie Ihre Ressourcen mit Schlüssel/Werte-Paaren getaggt haben, werden Ihnen im Nutzungsbericht auch Spalten entsprechend dem Schlüssel angezeigt. Zum Beispiel werden mit `project:abc` und `project:xyz` getaggte Ressourcen in einer Projektspalte mit "abc" und "xyz" angezeigt.

   Weitere Informationen finden Sie unter [Nutzung anzeigen](/docs/billing-usage?topic=billing-usage-viewingusage).

## Abrechnungs- und Nutzungsverwaltung mittels CLI oder APIs automatisieren
{: #billing-cli-apis}

Wenn Sie die Prüfung Ihrer Ressourcennutzung und die damit verbundenen Kosten automatisieren möchten, können Sie die CLI [`ibmcloud billing`](/docs/cli?topic=cloud-cli-ibmcloud_billing) oder die APIs [Nutzungsmessung ![Symbol für externen Link](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/usage-metering){: new_window} und [Nutzungsberichte ![Symbol für externen Link](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/metering-reporting){: new_window} verwenden, um diese Funktionalität in Ihre eigenen Apps zu integrieren.

Um mit der Verwendung der APIs zu beginnen, richten Sie das Beispieldashboard für die [{{site.data.keyword.Bluemix_notm}}-Nutzung ![Symbol für externen Link](../icons/launch-glyph.svg)](https://github.com/IBM-Cloud/openwhisk-cloud-usage-sample){: new_window} ein. Mithilfe von {{site.data.keyword.openwhisk}} implementiert das Beispiel einen API-basierten Ansatz zum Abrufen und Darstellen der {{site.data.keyword.Bluemix_notm}}-Nutzungs- und Fakturierungsdaten.
{: tip}
