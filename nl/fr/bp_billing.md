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


# Meilleures pratiques pour la facturation et l'utilisation
{: #best-practices}

Suivez nos meilleures pratiques pour effectuer le suivi des coûts et automatiser la facturation dans {{site.data.keyword.Bluemix}}.
{:shortdesc}


## Suivi des coûts des ressources connexes via l'ajout d'étiquettes
{:#track-billing-tags}

Ajoutez des étiquettes à vos ressources pour organiser les ressources connexes, en effectuer le suivi et gérer leurs coûts. Lorsque vous utilisez un schéma d'étiquetage cohérent pour identifier les ressources liées à des projets spécifiques, vous pouvez grouper des éléments et les filtrer en fonction des étiquettes lors de l'analyse des coûts dans votre rapport d'utilisation exporté.

1. Etiquetez vos ressources en utilisant un schéma d'étiquetage cohérent. Utilisez, par exemple, des étiquettes permettant de différencier les centres de coût, les centres de données, les projets ou les équipes. Pour ajouter des étiquettes, cliquez sur l'icône Menu ![Icône Menu](../icons/icon_hamburger.svg) > **Liste de ressources**. Dans la colonne Etiquette, cliquez sur **Ajouter des étiquettes** pour chaque ressource à étiqueter.

   Ajoutez des étiquettes dans les paires clé:valeur pour ajouter des colonnes personnalisées en fonction de la clé du rapport d'utilisation. Créez des clés en fonction des catégories utilisées pour l'organisation de vos ressources, comme l'utilisation de `costcenter:` pour regrouper les éléments par centre de coût ou de `project:` pour regrouper les éléments par projet.
   {: tip}

   Par exemple, vous pouvez avoir des ressources pour deux projets d'un seul compte, nommés Project ABC et Project XYZ. Project ABC inclut un cluster {{site.data.keyword.containershort_notm}}, des déploiements d'application Cloud Foundry et une base de données {{site.data.keyword.cloudant_short_notm}}. Vous pouvez ajouter l'étiquette `project:abc` à toutes les ressources pour différencier ces ressources du projet ABC des ressources similaires du projet XYZ étiquetées avec la mention `project:xyz`.

   Pour plus d'informations sur l'ajout et l'utilisation d'étiquettes, voir [Utilisation d'étiquettes](/docs/resources?topic=resources-tag).

1. Effectuez le suivi des coûts pour les ressources étiquetées en exportant le rapport d'utilisation pour vos instances. Pour exporter le rapport, accédez à **Gérer > Facturation et utilisation** et sélectionnez **Utilisation**. Cliquez ensuite sur **Exporter au format CSV > Instance**.

   Utilisez la colonne Etiquettes du fichier CSV de l'instance pour analyser plus facilement les ressources de votre compte. Vous pouvez trier les données CSV en fonction de l'étiquette du projet sur chaque instance de manière à mieux analyser le coût de chaque projet. Si vous avez étiqueté vos ressources avec des paires clé:valeur, vous voyez également les colonnes du rapport d'utilisation qui correspondent à la clé. Par exemple, les ressources étiquetées avec la mention `project:abc` et `project:xyz` s'affichent dans une colonne Projet sous la forme "abc" et "xyz".

   Pour plus d'informations, voir [Affichage de votre utilisation](/docs/billing-usage?topic=billing-usage-viewingusage).

## Automatisation de la gestion de la facturation et de l'utilisation en utilisant l'interface CLI ou les API
{: #billing-cli-apis}

Si vous souhaitez automatiser la révision de l'utilisation des ressources et des coûts associés, vous pouvez utiliser l'interface CLI [`ibmcloud billing`](/docs/cli?topic=cloud-cli-ibmcloud_billing) ou les API [Usage Metering ![Icône de lien externe](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/usage-metering){: new_window} et [Usage Reports ![Icône de lien externe](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/metering-reporting){: new_window} pour intégrer cette fonctionnalité dans vos propres applications.

Pour commencer à utiliser ces API, configurez le tableau de bord d'utilisation exemple [{{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg)](https://github.com/IBM-Cloud/openwhisk-cloud-usage-sample){: new_window}. En utilisant {{site.data.keyword.openwhisk}}, l'exemple implémente une approche gérée par API pour obtenir et visualiser les données d'utilisation et de facturation {{site.data.keyword.Bluemix_notm}}.
{: tip}
