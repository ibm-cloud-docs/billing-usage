---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise usage, view enterprise costs, account group usage, account usage, cost recovery, chargeback, support cost

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:external: target="_blank" .external}
{:note: .note}


# Nutzung in einem Unternehmen anzeigen
{: #enterprise-usage}

Sie können die Ressourcen- und Supportkosten über die Konten in Ihrem {{site.data.keyword.Bluemix}}-Unternehmen (Enterprise) durch Anzeigen der Nutzung überwachen. Die Konten und Kontogruppen, für die Sie die Nutzung anzeigen können, hängen von dem Ihnen zugewiesenen Zugriff ab.
{: shortdesc}

{{site.data.keyword.Bluemix_notm}}-Unternehmen ermöglichen es Ihnen, mehrere {{site.data.keyword.Bluemix_notm}}-Konten zentral zu verwalten. Als Unternehmensbenutzer können Sie die Ressourcennutzung und die damit verbundenen Kosten für jedes Konto im Unternehmen im Auge behalten. Weitere Informationen finden Sie im Abschnitt [Was ist ein Unternehmen?](/docs/account?topic=account-enterprise).

## Erforderlicher Zugriff für die Anzeige der Unternehmensnutzung
{: #enterprise-usage-access}

In einem Unternehmen wird der Zugriff auf Nutzungsinformationen durch den Unternehmensservice gesteuert. Zum Anzeigen von Nutzungsinformationen müssen Benutzer für das Unternehmenskonto eingeladen werden und sie müssen über die Rolle "Anzeigeberechtigter", "Bearbeiter" oder "Administrator" für den Unternehmensservice verfügen. Die Rolle "Anzeigeberechtigter für Nutzungsberichte" ermöglicht den Zugriff nur für die Anzeige von Nutzungsberichten, während die Rollen "Bearbeiter" und "Administrator" zusätzliche Aktionen für das Unternehmensmanagement ermöglichen. In Übereinstimmung mit bewährten Sicherheitsverfahren weisen Sie dem Benutzer nur die Zugriffsrechte zu, die er zur Erfüllung seiner Aufgaben benötigt. Weitere Informationen finden Sie unter [Aktionen und Rollen im Unternehmen](/docs/iam?topic=iam-account-services#enterprise-account-management).

Sie können Benutzern einen differenzierten Zugriff gewähren, sodass sie die Nutzung für ein bestimmtes Konto oder eine bestimmte Kontogruppe anzeigen können. Beispiel: Ihr Unternehmen verfügt über Kontogruppen für jede Abteilung und jede Abteilung hat Kontogruppen für jedes Team. Sie können den Zugriff so eingrenzen, dass jeder Unternehmensbenutzer nur die Informationen sehen kann, die er für seine Tätigkeit benötigt.
   * Ihr Finanzverantwortlicher muss die Nutzung für das gesamte Unternehmen anzeigen können, damit er die Kosten für jede Abteilung verfolgen und einziehen kann. Er muss jedoch keine Konten oder Kontogruppen erstellen können. Weisen Sie ihm die Rolle "Anzeigeberechtigter für Nutzungsberichte" für das Unternehmen zu.
   * Jeder Abteilungsleiter muss die Nutzung der Abteilung anzeigen und auch Konten und Kontogruppen für die eigenen Teams erstellen und verwalten können. Weisen Sie jedem Abteilungsleiter die Rolle "Bearbeiter" für die Kontogruppe der Abteilung zu.
   * Jeder Teamleiter muss die Nutzung des eigenen Teams anzeigen können. Ein Hinzufügen neuer Konten für das Team soll aber nur mit der Genehmigung der Abteilung möglich sein. Weisen Sie jedem Teamleiter die Rolle "Anzeigeberechtigter für Nutzungsberichte" für die Kontogruppe des Teams zu. Sie können die Nutzung für alle Konten innerhalb der Kontogruppe anzeigen, nicht jedoch die Nutzung durch Kontogruppen anderer Teams in der Abteilung.

Ausführliche Schritte zum Zuweisen von Zugriffsrechten für das Unternehmen finden Sie unter [Unternehmenszugriff zuweisen](/docs/iam?topic=iam-assign-access-enterprise).

## Unternehmensnutzung anzeigen
{: #enterprise-usage-console}

1. Melden Sie sich bei dem Unternehmenskonto an.
1. Rufen Sie **Verwalten > Abrechnung und Nutzung** auf und wählen Sie **Nutzung** aus.

   Auf der Seite "Nutzung" werden die Kosten für die gesamte Ressourcennutzung in Ihrem Unternehmen angezeigt, aufgeschlüsselt nach Konto und Kontogruppe. Sie können auch die Nutzung des Supportguthabens für das gesamte Unternehmen sowie eventuelle Überschreitungen anzeigen.

   Nutzungsinformationen für klassische Infrastrukturservices sind für den aktuellen Abrechnungszeitraum nicht enthalten. Sie sind aber für frühere Abrechnungszeiträume enthalten, die Sie anzeigen können, indem Sie einen früheren Monat im Menü **Zeitrahmen** auswählen. Weitere Informationen finden Sie unter [Nutzung für Ressourcen der klassischen Infrastruktur anzeigen](/docs/billing-usage?topic=billing-usage-infra-usage).
1. Um die Nutzung innerhalb einer Kontogruppe anzuzeigen, klicken Sie auf den Namen der Kontogruppe in der Tabelle oder im Menü **Unternehmensebene**. Ähnlich wie bei der Unternehmensebene wird die Nutzung nach Konto und Kontogruppe aufgegliedert.

   Wenn eine Kontogruppe keine Konten enthält, wird sie nicht auf der Seite 'Nutzung' angezeigt.

1. Wenn Sie die Nutzung nach Ressource anzeigen möchten, rufen Sie die Kontoebene auf, indem Sie sich in der Tabelle durch die Kontogruppen klicken oder das Konto im Menü **Unternehmensebene** auswählen. Es werden die Kosten für jeden Ressourcentyp angezeigt, der innerhalb des Zeitrahmens genutzt wurde.

   Über das Unternehmenskonto können Sie die Nutzungsdaten für den Ressourcenplan oder die Instanz nicht anzeigen, da ein Zugriff innerhalb des Kontos erforderlich ist. Wenn Sie ein Benutzer in dem Konto sind, wechseln Sie zu dem Konto, um die Daten anzuzeigen. Sie benötigen den Abrechnungszugriff auf die Ressourcen und Services im Konto, wie dies unter [Nutzung anzeigen](/docs/billing-usage?topic=billing-usage-viewingusage) beschrieben ist.

Nur die Nutzungsdaten, die bei Konten im Unternehmen anfallen, werden im Unternehmenskonto angezeigt. Um die Nutzung für den Zeitraum anzuzeigen, bevor ein Konto zum Unternehmen hinzugefügt wurde, melden Sie sich bei diesem Konto an und wählen Sie den entsprechenden Zeitraum aus.
{: note}

### Unternehmensnutzung über die Befehlszeilenschnittstelle (CLI) anzeigen
{: #enterprise-usage-cli}

Sie können einen Nutzungsbericht für das Unternehmen, eine Kontogruppe oder ein bestimmtes Konto abrufen.

1. Melden Sie sich an und wählen Sie das Unternehmenskonto aus.

   ```
   ibmcloud login
   ```
   {:codeblock}

1. Wenn Sie die Nutzung für eine bestimmte Kontogruppe oder ein bestimmtes Konto anzeigen möchten, suchen Sie den Namen oder die ID, indem Sie den Befehl **`ibmcloud enterprise`** ausführen.

   Der folgende Befehl zeigt zum Beispiel alle Kontogruppen in einem Unternehmen an.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}

1. Zeigen Sie die Nutzung an, indem Sie den Befehl **`ibmcloud billing`** ausführen, wie dies in den folgenden Beispielen gezeigt wird.

   * So zeigen Sie die Nutzung für das gesamte Unternehmen für den aktuellen Monat an:

      ```
      ibmcloud billing enterprise-usage
      ```
      {: codeblock}

   * So zeigen Sie die Nutzung für die Kontogruppe `Development` für Juli 2019 an:

      ```
      ibmcloud billing enterprise-usage --account-group Development --month 2019-07
      ```
      {:codeblock}

   * So zeigen Sie die Nutzung für die Kontogruppen und Konten auf der Ebene direkt unter dem Unternehmen an:

      ```
      ibmcloud billing enterprise-usage --children
      ```
      {:codeblock}

   Die Befehle geben standardmäßig den Nutzungsbericht für den aktuellen Monat im folgenden Format aus. Die meisten Kosten werden als abrechnungsfähige Kosten (Billable Cost) aufgeführt. Nicht abrechnungsfähige Kosten (Non-billable Cost) werden nur in sehr seltenen Fällen aufgelistet, z. B. für den Monat, in dem Sie dem Unternehmen ein Testkonto hinzufügen.

   ```
   Name             Type            Billable Cost   Non-billable Cost   Currency   Month
Example Corp     account         123.45          0                   USD        2019-07
Development      account_group   234.56          0                   USD        2019-07
Marketing        account_group   345.67          0                   USD        2019-07
Sales            account_group   456.78          0                   USD        2019-07
   ```

   Sie können den Bericht im JSON-Format ausgeben, indem Sie die Option `--output JSON` angeben.
   {: tip}

### Unternehmensnutzung über die Anwendungsprogrammierschnittstelle (API) anzeigen
{: #enterprise-usage-api}

Sie können Nutzungsberichte von einem Unternehmen und seinen Konten abrufen, indem Sie die <!-- [Enterprise Usage Reports API (Beta)](https://{DomainName}/apidocs/enterprise-apis/resource-usage-reports){: external} --> Enterprise Usage Reports API (Beta) aufrufen. Sie können die Abfrage in Ihrem API-Aufruf für ein Unternehmen, eine Kontogruppe oder ein Konto ausführen und angeben, ob die Entität oder ihre untergeordneten Elemente angezeigt werden sollen. Die Enterprise Usage Reports API ist ein Betarelease.

Die folgenden Beispiele zeigen Abfragen, die Sie verwenden können, um unterschiedliche Nutzungsberichte abzurufen. Wenn Sie die API aufrufen, ersetzen Sie die ID-Variablen und das IAM-Token durch die Werte Ihres Unternehmens.

So zeigen Sie die Nutzung für das gesamte Unternehmen für den aktuellen Monat an:

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

So zeigen Sie die Nutzung für eine Kontogruppe für Juli 2019 an:

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?account_group_id=$ACCOUNT_GROUP_ID&month=2019-07" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

So zeigen Sie die Nutzung für Kontogruppen und Konten auf der Ebene direkt unter dem Unternehmen an:

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID&children=true" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}


## Kosten für die Unternehmensnutzung einziehen
{: #enterprise-cost-recovery}

Ein Unternehmen konsolidiert die Abrechnung aller seiner Konten und Kontogruppen in einer einzigen Rechnung, wodurch das Abrechnungsmanagement vereinfacht wird. Sie können die Kosten für die Ressourcennutzung im Unternehmen einziehen, indem Sie die Nutzungskosten für jede Kontogruppe oder jedes Konto der entsprechenden Abteilung oder dem jeweiligen Team berechnen.

Um Ihre Unternehmenshierarchie und jede Nutzung anzuzeigen, benötigen Sie eine Zugriffsrichtlinie mit der Rolle "Bearbeiter" oder "Administrator" für den Unternehmensservice für das gesamte Unternehmen. Für die folgenden Schritte wird als Beispiel die {{site.data.keyword.Bluemix_notm}}-Konsole verwendet, Sie können diese Schritte aber auch mithilfe der CLI oder der API ausführen.

1. Sie finden die Nutzungskosten für die einzelnen Abteilungen, indem Sie im Unternehmenskonto die Optionen **Verwalten > Nutzung** auswählen. Wählen Sie im Menü **Zeitrahmen** den Vormonat aus, um die Nutzung anzuzeigen, die in der letzten Rechnung enthalten ist.

  Die Kosten für Ihre Kontogruppen sind in der Tabelle aufgelistet. Diese Kosten beinhalten alle Gebühren mit Ausnahme der Steuern, die in Ihrer Abrechnungsregion erhoben werden. Wenn Sie eine weitere Aufschlüsselung der Nutzungskosten wünschen, klicken Sie auf den Namen der Kontogruppe, um die enthaltenen Konten und Kontogruppen anzuzeigen.

1. Ermitteln Sie die Abteilungen in Ihrem Unternehmen, die den Kontogruppen entsprechen.

   Wenn die Kontakte, die Ihren Kontogruppen zugewiesen sind, der Abteilung zugeordnet sind, von der Sie die Kosten einziehen möchten, ist das Suchen des Kontakts eine Möglichkeit, nach diesen Informationen zu suchen. Rufen Sie **Verwalten > Unternehmen** auf und wählen Sie **Konten** aus. Der Kontakt für jede Kontogruppe ist in der Tabelle aufgelistet.

   Die Abrechnungspraktiken variieren jedoch je nach Unternehmen. Beispielsweise kann der Kontogruppenkontakt ein technischer Ansprechpartner sein, der nicht zu der Abteilung gehört, von der Sie Kosten einziehen möchten. Prüfen Sie stets, welches die richtige Abteilung entsprechend den Abrechnungsprozessen Ihres Unternehmens ist.

   Wenn Ihr Unternehmen Abrechnungscodes verwendet, um Abteilungen die von ihnen verursachten Kosten zurückzubelasten, fügen Sie den Abrechnungscode dem Namen der Kontogruppe hinzu, damit der Code leicht erkennbar ist. Beispiel: `Sales - A2B3`.
   {: tip}

1. Ordnen Sie die Nutzungskosten für jede Kontogruppe der angegebenen Abteilung zu und befolgen Sie Unternehmensprozesse, um die Gebühren verarbeiten zu lassen.
