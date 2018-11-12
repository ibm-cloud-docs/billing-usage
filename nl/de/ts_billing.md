---



copyright:

  years: 2017, 2018
lastupdated: "2018-10-18"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Fehlerbehebung für die Verwaltung der Abrechnung und Nutzung
{: #troubleshoot}

Zu den allgemeinen Problemen bei der Verwaltung der Abrechnung und Nutzung können auch Probleme im Zusammenhang mit dem Zugriffsberechtigung für die Abrechnungsinformationen gehören. In vielen Fällen können Sie dieses Problem durch Ausführen weniger einfacher Schritte beheben.
{:shortdesc}

## Zugriff auf Abrechnungsinformationen nicht möglich
{: #cannot-access-billing-info}

### Szenario

Wenn Sie versuchen, auf die Abrechnungsinformationen zuzugreifen, erhalten Sie eine Fehlernachricht, in der angegeben ist, dass Sie nicht über die Berechtigung verfügen, die zum Anzeigen der Abrechnungsinformationen für das Konto erforderlich ist.

### Ursache

Sie müssen Kontoeigner oder Abrechnungsmanager für eine Organisation sein. 

### Fehlerbehebung

Führen Sie die folgenden Schritte aus, um Ihre Zugriffsrolle zu überprüfen: 

1. Rufen Sie **Verwalten** > **Sicherheit** > **Identität und Zugriff** auf und klicken Sie auf **Benutzer**.
2. Klicken Sie in der Benutzerliste auf Ihren Namen.
3. Im Bereich **Zugriffsrichtlinie** können Sie Ihre zugeordneten Zugriffsrichtlinien anzeigen. 
4. Überprüfen Sie in der Spalte **Rolle**, ob Sie über die Rolle eines Kontoeigners oder Abrechnungsmanagers verfügen.  

Weitere Informationen zum Zugriff finden Sie unter [Cloud IAM-Rollen](/docs/iam/users_roles.html#iamusermanrol).
