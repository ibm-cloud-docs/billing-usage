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

# Calcul des coûts
{: #cost}

Vous pouvez utiliser différentes méthodes pour estimer le coût de l'utilisation de ressources {{site.data.keyword.Bluemix}} PaaS et IaaS afin de générer et d'héberger vos applications.
{:shortdesc}

Vous pouvez utiliser les méthodes suivantes pour déterminer vos coûts :
* Utilisez la [calculatrice de tarification![Icône de tarification](../icons/launch-glyph.svg)](https://console.bluemix.net/pricing/){: new_window} afin d'estimer le coût total des ressources PaaS et IaaS que vous souhaitez utiliser. 
* Utilisez les estimateurs de coût sur la page {{site.data.keyword.pricing_sheet}} {{site.data.keyword.Bluemix_notm}}
pour voir une estimation approximative du coût en fonction de la taille de votre application.
* Utilisez la calculatrice de coût sur la page Tarification pour voir les prix précis des applications en fonction des données d'utilisation des
contextes d'exécution et des services que vous avez entrées.
* Calculez votre coût manuellement. 

## Utilisation de la calculatrice de tarification
{: #pricing-calculator}

Vous pouvez utiliser la calculatrice de tarification pour estimer le coût des ressources PaaS et IaaS avant de réaliser un achat.
La calculatrice de tarification fournit les fonctions suivantes :
  * Les estimations de coûts qui sont actuellement fournies en devise américaine. 
  * Les estimations des ressources IaaS qui sont actuellement disponibles pour les catégories **Calcul** et **Conteneurs**. 
  * Les estimations de coûts des ressources qui n'incluent pas de remises.
  * Les estimations de coûts qui sont fournies à des fins de planification. 

1. Accédez à la calculatrice de tarification en procédant de l'une des façons suivantes :
  * Sur la [page de tarification ![Icône de lien externe](../icons/launch-glyph.svg)](https://www.ibm.com/cloud/pricing){: new_window}, cliquez sur **Essayer la calculatrice** dans la section Explorez nos solutions. 
  * Si vous n'êtes pas connecté à {{site.data.keyword.Bluemix_notm}}, cliquez sur **Tarification** sur la [page d'accueil de {{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg)](https://console.bluemix.net/).
2. Dans les listes **Infrastructure** ou **Plateforme**, sélectionnez la catégorie de la ressource à tarifer. Les ressources de la catégorie que vous avez sélectionnée s'affichent et vous pouvez également rechercher une ressource spécifique dans une catégorie. 
3. Sélectionnez une ressource dans la catégorie pour voir sa description. Certaines ressources comportent plusieurs options. Par exemple, si vous sélectionnez **Infrastructure** > **Calcul** > **Serveurs bare metal**, vous pouvez effectuer une sélection dans une liste de serveurs.  
4. Sélectionnez la quantité de la ressource à ajouter. 
5. Cliquez sur **Add to estimate**.
6. Continuez d'ajouter des ressources à partir des catégories **Infrastructure** et **Plateforme** jusqu'à ce que vous ayez ajouté ce que vous souhaitez estimer. 

Le panneau **Estimation** présente les ressources que vous avez ajoutées, le prix de chacune de ces ressources, et un prix total.  

Si vous calculez la tarification des ressources PaaS uniquement, vous pouvez cliquer sur **Basculer sur classique** pour afficher une estimation dans une devise autre que le dollar américain. La calculatrice classique n'inclut pas les ressources IaaS.
{: tip}

### Utilisation de la calculatrice classique pour les ressources PaaS
{: #calculator}

Pour calculer les coûts de vos ressources PaaS dans une devise autre que le dollar américain, vous pouvez utiliser la calculatrice classique. La calculatrice classique ne fournit pas d'estimations de tarification pour les ressources IaaS.


1. Accédez à la page {{site.data.keyword.pricing_sheet}} {{site.data.keyword.Bluemix_notm}}.
2. Sélectionnez l'une des options IaaS pour prendre en charge la section Toutes vos charges de travail. 

Pour utiliser la calculatrice, entrez votre utilisation mensuelle prévue pour les ressources répertoriées, par exemple le nombre d'instances ou de
notifications push. La calculatrice affiche immédiatement le prix pour les données entrées. Vous pouvez aussi
paramétrer la calculatrice pour qu'elle affiche les coûts annuels au lieu des coûts mensuels.

## Calcul manuel de vos coûts
{: #manual}

Vous pouvez décider d'estimer le coût de {{site.data.keyword.Bluemix_notm}} vous-même pour mieux comprendre comment les coûts relatifs à {{site.data.keyword.Bluemix_notm}} sont calculés. Vous pouvez calculer le prix total de l'utilisation de {{site.data.keyword.Bluemix_notm}} pour la construction
et l'hébergement de votre application, en tenant compte des prix du contexte d'exécution et des services qu'il utilise. Les prix des contextes d'exécution et des
services peuvent changer ; par conséquent, vous devez vous référer aux informations les plus récentes sur la fiche de prix {{site.data.keyword.Bluemix_notm}} lorsque vous calculez le prix total.

## Devises de facturation prises en charge

Le tableau ci-dessous répertorie les devises prises en charge disponibles.

|Code ISO 4217| Devise|
|-------------|---------|
|AUD |	  Dollar australien|
|BRL |	  Réal brésilien|
|CAD |	  Dollar canadien|
|CHF |	  Franc suisse|
|DKK |	  Couronne danoise|
|EUR |	  Euro|
|GBP |	  Livre sterling|
|INR |	  Roupie indienne|
|JPY |	  Yen japonais|
|KRW |	  Won sud-coréen|
|NOK |	  Couronne norvégienne|
|NZD |	  Dollar néo-zélandais|
|SEK |	  Couronne suédoise|
|USD |    Dollar américain|
|ZAR |	  Rand sud-africain|
{:caption="Tableau 1. Devises prises en charge" caption-side="top"}

Si vous avez lié vos comptes {{site.data.keyword.Bluemix_notm}} et SoftLayer, la facture unique que vous recevez est en dollars américains (USD) uniquement. Pour plus d'informations, voir [Facturation en bloc pour des comptes liés](/docs/account/linking_accounts.html).
{: tip}
