---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-03"

keywords: view usage, view cost, service usage, usage access, usage report

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}


# Nutzungsinformationen anzeigen
{: #viewingusage}

Sie können Ihre Nutzungsdetails, einschließlich einer Zusammenfassung der voraussichtlichen Gebühren für alle Ressourcen, Services und Unterstützungspläne, die pro Monat in Ihren Organisationen verwendet werden, über die Seite 'Nutzung' in der {{site.data.keyword.Bluemix}}-Konsole anzeigen.
{:shortdesc}

Abrechnungsmanager können nur die Details für die Organisationen anzeigen, in denen ihnen die Rolle des Abrechnungsmanagers zugewiesen ist.
{: note}


## Nutzungsberechtigungen anzeigen
{: #view-usage-permissions}

Für Ressourcen, die über Cloud Foundry verwaltet werden, muss die Rolle des Abrechnungsmanagers auf Organisationsebene angewendet werden. Zum Anzeigen der Nutzung von IAM-Ressourcen von {{site.data.keyword.Bluemix}} muss die Rolle 'Anzeigeberechtigter' auf die Ressourcengruppe angewendet werden. Weitere Informationen zu Berechtigungsrollen finden Sie in den Abschnitten zum [IAM-Zugriff](/docs/iam?topic=iam-userroles), zum [Cloud Foundry-Zugriff](/docs/iam?topic=iam-cfaccess) und zu [Berechtigungen für die klassische Infrastruktur](/docs/iam?topic=iam-infrapermission).

## Servicenutzungsdetails anzeigen
{: #services}

Im Abschnitt 'Services' können Sie eine Liste Ihrer Services sowie die voraussichtlichen Kosten anzeigen, die mit diesen Services verbunden sind. Führen Sie die folgenden Schritte aus, um eine Zusammenfassung der voraussichtlichen Gebühren für alle Instanzen einer bestimmten Ressource anzuzeigen:

1. Rufen Sie **Verwalten > Abrechnung und Nutzung** auf und wählen Sie **Nutzung** aus.
2. Klicken Sie auf **Instanzen anzeigen**, um alle Instanzen eines bestimmten Ressourcentyps anzuzeigen.  
3. Klicken Sie auf die Option **Instanzdetails anzeigen**, um eine detaillierte Zusammenfassung der voraussichtlichen Gebühren für die einzelnen Instanzen eines bestimmten Ressourcentyps anzuzeigen. Es werden auch die ausführlichen monatlichen Nutzungsmetriken für die ausgewählte Instanz angezeigt.

Dem Kontoeigner werden die Gebühren für die Gesamtnutzung, die für alle Organisationen anfallen, am Ende jedes Abrechnungszyklus in Rechnung gestellt. Jeder Abrechnungszyklus dauert einen Monat.

Kontoeigner können die Nutzungszusammenfassung nach Gruppe filtern und den Zeitraum für die Nutzung auswählen. Die angezeigten Gebühren stellen den Betrag dar, der Ihnen als Kontoeigner für diesen Monat in Rechnung gestellt wird.

Wenn Sie in der Liste **Nach Gruppe filtern** eine bestimmte Organisation auswählen, können Sie die gesamte Nutzung für diese Organisation, einschließlich der Nutzung im Rahmen eines gebührenfreien Nutzungskontingents, anzeigen. Die Nutzung des gebührenfreien Nutzungskontingents wird zwar auf Kontoebene als kostenfrei angezeigt, nicht jedoch auf Organisationsebene. Wenn Sie die organisationsbezogene Nutzung anzeigen, wird die tatsächliche Nutzung für diese Organisation einschließlich der kostenfreien und der gebührenpflichtigen Nutzung angezeigt. Beim Anzeigen der Nutzung aller Organisationen wird die Nutzung für das Konto aufsummiert, nachdem das gebührenfreie Nutzungskontingent entfernt wurde.

Der Manager eines nutzungsabhängigen Kontos kann ausgabenbezogene Benachrichtigungen zu den Gesamtkosten des Kontos für Laufzeit, Services und für einzelne Services, Services anderer Anbieter ausgenommen, einrichten. Weitere Informationen hierzu finden Sie unter [Ausgabebenachrichtigungen einstellen](/docs/billing-usage?topic=billing-usage-spending).

## Nutzungsdetails in `CSV`-Datei exportieren
{: #export-csv}

Sie können eine Zusammenfassung Ihrer Nutzungsdaten oder Informationen zu Ihren Services und Instanzen in eine CSV-Datei exportieren. Der Export in eine CSV-Datei erleichtert das Auffinden von Informationen zu Nutzungsschätzungen und voraussichtlichen Kosten für die einzelnen Ressourcen für Kostenerstattungen an die Kunden und ermöglicht Ihnen einen besseren Einblick in Ihre Kosten.

1. Rufen Sie **Verwalten > Abrechnung und Nutzung** auf und wählen Sie **Nutzung** aus.
1. Klicken Sie auf **CSV exportieren** und wählen Sie eine der Optionen aus:
   - Klicken Sie auf **Zusammenfassung**, um für Ihr Konto eine allgemeine Übersicht über Nutzung und zugeordnete Kosten zu erhalten.
   - Klicken Sie auf **Instanz**, um detaillierte Nutzungsinformationen zu den einzelnen Serviceinstanzen zu erhalten.

   Mithilfe der Spalte **Tags** in der CSV-Datei der Instanz können Sie die Ressourcen in Ihrem Konto leichter analysieren. Sie können zum Beispiel in einem einzigen Konto mehrere Projekte haben, von denen jedes einen Kubernetes-Cluster und einige neue Implementierungen von Cloud Foundry-Apps aufweist. Sie können die CSV-Daten gemäß den Projekt-Tags der einzelnen Instanzen organisieren, sodass Sie die Kosten eines einzelnen Projekts besser analysieren können. Weitere Informationen zum Tagging finden Sie in [Mit Tags arbeiten](/docs/resources?topic=resources-tag).
   {: tip}
