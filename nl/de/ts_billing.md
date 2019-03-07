---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-09"

keywords: troubleshoot billing, billing error, payment error, error message

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# Fehlerbehebung für die Verwaltung der Abrechnung und Nutzung
{: #troubleshoot}

Zu den allgemeinen Problemen bei der Verwaltung der Abrechnung und Nutzung können auch Probleme im Zusammenhang mit dem Zugriffsberechtigung für die Abrechnungsinformationen gehören. In vielen Fällen können Sie dieses Problem durch Ausführen weniger einfacher Schritte beheben.
{:shortdesc}


## Warum kann ich nicht auf Abrechnungsinformationen zugreifen?
{: #cannot-access-billing-info}
{: troubleshoot}

Wenn Sie versuchen, auf die Abrechnungsinformationen, z. B. Zahlungen und Rechnungen, zuzugreifen, erhalten Sie eine Nachricht mit dem Hinweis, dass die Funktion nicht verfügbar ist.
{: tsSymptoms}

Sie erhalten diese Nachricht, wenn Sie nicht über die Berechtigung zum Anzeigen der Abrechnungsinformationen für das Konto verfügen. Sie müssen ein Kontoeigner oder Abrechnungsmanager für eine Cloud Foundry-Organisation sein oder Ihnen muss über eine IAM-Richtlinie die Administratorrolle für alle Kontoverwaltungsservices zugewiesen sein.
{: tsCauses}

Sie können die Abrechnungsinformationen für jedes Konto anzeigen, dessen Eigner Sie sind. Abrechnungsmanager können Abrechnungsinformationen für eine Cloud Foundry-Organisation anzeigen. Für IAM-fähige Ressourcen muss Ihnen über eine IAM-Richtlinie die Administratorrolle für alle Kontoverwaltungsservices zugewiesen sein.

Überprüfen Sie Ihren Zugriff wie im Folgenden beschrieben:

  1. Rufen Sie **Verwalten > Zugriff (IAM)** auf und wählen Sie **Benutzer** aus.
  2. Klicken Sie auf der Benutzerseite auf Ihren Namen.
  3. Klicken Sie auf **Zugriffsrichtlinien**, um die Ihnen zugewiesenen IAM-Zugriffsrichtlinien anzuzeigen.
  4. Klicken Sie auf **Cloud Foundry-Zugriff** und erweitern Sie die Zeilen für die Ihnen zugewiesenen Organisationen, um herauszufinden, ob Sie Kontoeigner sind oder über die Rolle 'Abrechnungsmanager' verfügen.

Weitere Informationen zum IAM-Zugriff finden Sie unter [Cloud IAM-Rollen](/docs/iam?topic=iam-userroles). Weitere Informationen zum Cloud Foundry-Zugriff finden Sie unter [Cloud Foundry-Rollen](/docs/iam?topic=iam-cfaccess).
{: tsResolve}
