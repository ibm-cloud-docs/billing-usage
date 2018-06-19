---



copyright:

  years: 2015, 2018
lastupdated: "2018-06-11"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Nutzung für mit {{site.data.keyword.Bluemix_notm}} verknüpfte Konten verwalten
{: #linkedusage}

Wenn Sie über ein verknüpftes {{site.data.keyword.Bluemix}}- und SoftLayer-Konto verfügen, können Sie über das Kundenportal einmalige Zahlungen leisten, die Kreditkartendetails ändern, Ihre Rechnungspositionen und Rechnungen anzeigen.
{: shortdesc}

Die in der {{site.data.keyword.Bluemix_notm}}-Konsole angezeigten Abrechnungs- und Nutzungsoptionen können anders sein, wenn Sie ein Lite-Konto verwenden oder über kein verknüpftes Konto verfügen.
{: tip}

## Zahlung vornehmen
{: #makepayment}

Sie können eine einmalige Zahlung jederzeit vornehmen. Die Zahlung kann für den gesamten Restbetrag oder einen Teilbetrag sein. Die Details, die Sie für die Zahlung eingeben, werden nicht aufgezeichnet. Führen Sie die folgenden Schritte aus, um eine einmalige Zahlung vorzunehmen:

1. Klicken Sie in der Menüleiste auf **Verwalten** > **Abrechnung und Nutzung** > **Zahlung vornehmen**.  
2. Geben Sie im Feld für den **Zahlungsbetrag** den gewünschten Zahlungsbetrag ein.
3. Wählen Sie die Zahlungsmethode aus:
 * Bezahlung mit einer Kreditkarte. Geben Sie die Kartendetails und die Rechnungsadresse der Karte ein. Klicken Sie anschließend auf **Kreditkartenzahlung vornehmen**.
 * Bezahlung mit PayPal. Wenn Sie dazu aufgefordert werden, geben Sie Ihre Daten ein, um die Zahlung abzuschließen.

Beheben Sie alle gemeldeten Probleme für die Zahlung. Der Kontostand wird aktualisiert, nachdem die Zahlung akzeptiert wird. Sie können sich ggf. an das Support-Team wenden, indem Sie auf **Support** > **Ticket hinzufügen** klicken.

## Zahlungsmethode ändern
{: #changepaymethod}

Jedes gebührenpflichtiges Konto muss eine registrierte Kreditkarte haben, die gültig ist. Die Abrechnung für die Kreditkarte erfolgt monatlich für die Verbrauchsmenge, die sich während dieses Monats angesammelt hat. Führen Sie in der {{site.data.keyword.Bluemix_notm}}-Konsole die folgenden Schritte aus, um Ihre Zahlungsinformationen hinzuzufügen oder zu ändern:

1. Klicken Sie in der Menüleiste auf **Verwalten** > **Abrechnung und Nutzung** > **Zahlungsmethode ändern**.  
2. Geben Sie im Abschnitt 'Zahlungsmethode' Ihre Kreditkartendaten und Rechnungsadresse der Karte ein. Anschließend klicken Sie auf **Kreditkarte hinzufügen**.

Ihre Kreditkartendaten werden überprüft und Ihre Karte steht dann innerhalb von 24 Stunden für die Verwendung in Ihrem Konto zur Verfügung. Eine entsprechende Bestätigungs-E-Mail wird an die Kontaktadresse gesendet, die im Abschnitt mit der Rechnungsadresse der Karte angegeben wurde.

## Rechnungspositionen anzeigen
{: #viewbilling}

Sie können Rechnungspositionen zu bestimmten Geräten zuordnen oder die Zuordnung aufheben. Standardmäßig werden auf der Seite **Rechnungspositionen** die zugehörigen Rechnungspositionen angezeigt. Sie können die Ansicht ändern, indem Sie eine Option aus dem Menü 'Anzeigen' auswählen. Sie können eine einzelne Position zuordnen oder deren Zuordnung aufheben oder mit der Operation 'Massenaktionen' mehrere Positionen gleichzeitig zuordnen oder deren Zuordnung aufheben. Sie können auch jederzeit einzelne Rechnungspositionen stornieren. 

1. Wählen Sie die Option **Menüsymbol ![Menüsymbol](../icons/icon_hamburger.svg) > Infrastruktur** aus. 
2. Klicken Sie in der Menüleiste auf **Konto** > **Abrechnung** > **Rechnungspositionen**.
3. Wählen Sie zum Filtern der Ansicht in der Liste eine Option für die Rechnungspositionen aus.

## Rechnungen anzeigen
{: #viewinvoices}

Sie können Ihre Rechnungen jederzeit anzeigen oder bezahlen. Jede Rechnung wird nach Rechnungsnummer, Datum, Rechnungstyp und verschiedenen monetären Bilanzposten zusammengefasst. Die Rechnungstypen werden in der folgenden Liste beschrieben:

 *  Neu: Die erste Rechnung in einer Reihe von Einzelrechnungen.
 *  Wiederholt auftretend: Eine Rechnung für wiederkehrende Gebühren, die seit mehr als einem Monat für das Konto anfallen.
 *  Einmalige Gebühr: Eine einmalige Gebühr für verschiedene Ausgaben, die Überschreitungen enthalten kann.
 *  Guthaben: Ein Guthaben von {{site.data.keyword.Bluemix_notm}} für den Kontostand.
 *  Rückerstattung: Eine Rückerstattung oder Rückbuchung für eine einmalige oder wiederkehrende Gebühr.

Auf der Seite **Rechnungen** wird außerdem eine Rechnungszusammenfassung für das Konto angezeigt, die den aktuellen und erwarteten nächsten Kontostand, die Zahlungsmethode und die letzten und nächsten Einzelrechnungsdaten enthält.

Führen Sie die folgenden Schritte aus, um eine Rechnung anzuzeigen:

1. Wählen Sie die Option **Menüsymbol ![Menüsymbol](../icons/icon_hamburger.svg) > Infrastruktur** aus. 
2. Klicken Sie in der Menüleiste auf **Konto** > **Abrechnung** > **Rechnungen**.
3. Sie können eine Rechnung im Kundenportal anzeigen oder die Rechnung herunterladen.

## {{site.data.keyword.Bluemix_notm}}-Services mit SoftLayer-Assets verwenden
{: #combined}

Es ist einfach, API-basierte öffentliche {{site.data.keyword.Bluemix_notm}}-Services mit den SoftLayer-Assets zu verwenden. Alle APIs sind gesichert und verschlüsselt, damit Ihre Daten geschützt sind.

Wollen Sie beispielsweise die kognitiven Fähigkeiten von Watson in Apps einfügen, die auf Bare-Metal-Servern über SoftLayer ausgeführt werden? Sie können in vier Schritten einen Service wie {{site.data.keyword.personalityinsightsshort}} hinzufügen, um den Benutzer Ihrer App besser zu verstehen:

1. Suchen Sie den Service im Katalog.
2. Stellen Sie eine Instanz des Service bereit. Dazu sind nur einige Klicks notwendig.
3. Konfigurieren Sie den Service für die Ausführung mit dem bereits vorhandenen Code, indem Sie die Berechtigungsnachweise des Service kopieren und diese zur Anwendung hinzufügen.
4. Nach der Aktualisierung der App können Sie die neue Version in der SoftLayer-Infrastruktur bereitstellen.

Erweitern Sie Ihr Insights- und Ihr kognitives Wissen, indem Sie Watson-APIs über Ihre Apps in SoftLayer aufrufen, um diese stärker zu personalisieren. Oder nutzen Sie die Daten- und Analyseservices, um leistungsstarke Analysen für Ihre Apps auszuführen. Sie können sich auch für Database as a Service entscheiden und das Management {{site.data.keyword.Bluemix_notm}} überlassen.

Modernisieren Sie die Anwendungsentwicklung unter Verwendung von Containern mit Services wie {{site.data.keyword.activedeployshort}} und {{site.data.keyword.deliverypipeline}}. Sie können dann über den {{site.data.keyword.vpn_short}}-Service mit SoftLayer kommunizieren, um den Container in einem privaten Netz mit dem privaten SoftLayer-Netz zu verbinden. Alle Nutzungsgebühren für Rechenressourcen und -services werden über die {{site.data.keyword.Bluemix_notm}}-Rechnung abgerechnet.
