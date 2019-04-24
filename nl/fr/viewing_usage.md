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


# Affichage de votre utilisation
{: #viewingusage}

Vous pouvez consulter vos informations d'utilisation (notamment un récapitulatif des frais estimés pour les ressources, les services et les plans de support utilisés par mois dans vos organisations) sur la page Utilisation de la console {{site.data.keyword.Bluemix}}.
{:shortdesc}

Les responsables de la facturation peuvent voir uniquement les informations relatives aux organisations dans lesquelles ils disposent de ce rôle.
{: note}


## Affichage des droits d'utilisation
{: #view-usage-permissions}

Pour les ressources gérées par Cloud Foundry, le rôle de responsable de la facturation doit être appliqué au niveau de l'organisation. Pour voir l'utilisation des ressources {{site.data.keyword.Bluemix}} Identity and Access Management (IAM), le rôle Afficheur doit être appliqué au groupe de ressources. Pour plus d'informations sur les rôles, voir [Accès IAM](/docs/iam?topic=iam-userroles), [Accès Cloud Foundry](/docs/iam?topic=iam-cfaccess) ou [Droits d'infrastructure classique](/docs/iam?topic=iam-infrapermission).

## Affichage des informations concernant l'utilisation du service
{: #services}

Dans la section Services, vous pouvez consulter la liste de vos services ainsi que les coûts estimés associés à ces services. Pour afficher un récapitulatif des frais estimés pour toutes les instances d'une ressource donnée, procédez comme suit :

1. Accédez à **Gérer > Facturation et utilisation** puis sélectionnez **Utilisation**.
2. Cliquez sur **Afficher les instances** pour voir toutes les instances d'un type spécifique de ressource.  
3. Pour voir un récapitulatif détaillé des frais estimés de chaque instance d'un type de ressource spécifique, cliquez sur **Afficher les détails de l'instance**. Vous pouvez également consulter des métriques d'utilisation mensuelles détaillées pour l'instance sélectionnée.

Le propriétaire de compte est facturé pour l'utilisation totale occasionnée dans toutes les organisations à la fin de chaque cycle de
facturation. Chaque
cycle de facturation dure un mois.

Les propriétaires de compte peuvent filtrer le récapitulatif d'utilisation par groupe et sélectionner la période pour l'utilisation. Les frais affichés représentent la somme qui vous sera facturée pour ce mois, en tant que propriétaire de compte.

Si vous sélectionnez une organisation spécifique dans la liste **Filtrer par groupe**, l'utilisation totale pour cette organisation apparaît, y compris celle relevant d'un niveau gratuit. L'utilisation d'une tranche gratuite apparaît comme gratuite au niveau du compte, mais pas au niveau de l'organisation. Lorsque vous affichez l'utilisation au niveau de l'organisation, vous consultez l'utilisation réelle pour cette organisation, incluant l'utilisation gratuite et l'utilisation facturée. L'utilisation au niveau de l'organisation correspond à l'utilisation au niveau de compte une fois la
tranche gratuite retirée.

En tant que responsable d'un compte de type Paiement à la carte, vous pouvez définir des notifications relatives aux dépenses en fonction du coût total de votre compte, pour votre contexte d'exécution et vos services et pour des services individuels, à l'exception des services de tiers. Pour plus d'informations, voir [Définition des notifications relatives aux dépenses](/docs/billing-usage?topic=billing-usage-spending).

## Exportation de vos informations d'utilisation dans un fichier `.csv`
{: #export-csv}

Vous pouvez exporter un récapitulatif de votre utilisation ou les informations relatives à vos services et vos instances dans un fichier CSV. En exportant votre fichier CSV, vous pouvez facilement trouver les estimations d'utilisation et de coût pour chaque ressource afin d'imputer des frais à vos clients ou pour mieux comprendre vos coûts.

1. Accédez à **Gérer > Facturation et utilisation** puis sélectionnez **Utilisation**.
1. Cliquez sur **Exporter au format CSV**, puis sélectionnez l'une des options suivantes :
   - **Récapitulatif** pour une présentation générale de l'utilisation et des coûts associés à votre compte.
   - **Instance** pour des informations d'utilisation détaillées concernant chaque instance de service.

   Vous pouvez utiliser la colonne **Etiquettes** du fichier CSV de l'instance pour vous aider à analyser les ressources de votre compte. Par exemple, vous pouvez avoir plusieurs projets dans un compte, ayant chacun un cluster Kubernetes et quelques déploiements d'application Cloud Foundry. Vous pouvez organiser les données CSV en fonction de l'étiquette du projet sur chaque instance de manière à mieux analyser le coût de chaque projet. Pour plus d'informations sur les étiquettes, voir [Utilisation d'étiquettes](/docs/resources?topic=resources-tag).{: tip}
