---



copyright:

  years: 2017, 2018
lastupdated: "2017-12-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Gestion de l'utilisation pour les comptes {{site.data.keyword.Bluemix_notm}} liés
{: #linkedusage}

Si vous disposez d'un compte {{site.data.keyword.Bluemix}} et d'un compte SoftLayer liés, vous pouvez utiliser le portail client pour effectuer un paiement ponctuel, changer les détails de votre carte de paiement, afficher vos articles de facturation, et afficher vos factures.
{: shortdesc}

Les options de facturation et d'utilisation qui sont affichées dans la console {{site.data.keyword.Bluemix_notm}} peuvent différer si vous disposez d'un compte gratuit ou si vos comptes {{site.data.keyword.Bluemix_notm}} et SoftLayer ne sont pas liés.
{: tip}

## Paiement
{: #makepayment}

Vous pouvez effectuer un paiement ponctuel à tout moment. Le montant du paiement peut être celui du solde total ou un montant partiel, et les détails que vous entrez pour le paiement ne sont pas enregistrés. Procédez comme suit pour effectuer un paiement ponctuel.

1. Sélectionnez l'une des options suivantes en fonction du tableau de bord que vous utilisez :   
 * Dans le tableau de bord Applis ou Services, cliquez sur **Gérer** > **Facturation et utilisation** > **Effectuer un paiement**.  
 * Dans le tableau de bord Infrastructure, cliquez sur **Compte** > **Effectuer un paiement**.
3. Dans la zone **Payment Amount**, entrez la somme à régler.
4. Sélectionnez votre méthode de paiement :
 * Paiement avec une carte de crédit. Entrez les détails de votre carte ainsi que l'adresse de facturation de la carte. Ensuite, cliquez sur **Make Credit Card Payment**.
 * Paiement avec PayPal. Entrez vos informations lorsque vous êtes invité à procéder au paiement.

Résolvez tout problème signalé qui est lié au paiement. Le solde du compte est mis à jour une fois le paiement accepté. Vous pouvez prendre contact avec l'équipe de support en cliquant sur **Support** > **Ajouter un ticket**.

## Changement de méthode de paiement
{: #changepaymethod}

Une carte de crédit valide doit être enregistrée pour chaque compte facturable. Tous les mois, la carte de crédit est débitée du montant correspondant à l'utilisation mensuelle. Dans la console {{site.data.keyword.Bluemix_notm}}, procédez comme suit pour ajouter ou changer vos détails de paiement.

1. Sélectionnez l'une des options suivantes en fonction du tableau de bord que vous utilisez :  
 * Dans le tableau de bord Applis ou Services, cliquez sur **Gérer** > **Facturation et utilisation** > **Modifier la méthode de paiement**.  
 * Dans le tableau de bord Infrastructure, cliquez sur **Compte** > **Facturation** > **Méthode de paiement**.
2. Dans la section Add Payment Method, entrez les détails de votre carte de crédit ainsi que l'adresse de facturation de la carte. Ensuite, cliquez sur **Ajouter une carte de crédit**.

Les détails de votre carte sont validés et votre carte pourra être utilisée sur votre compte dans les 24 heures. Un courrier électronique de confirmation est
envoyé au contact entré dans la section de l'adresse de facturation de la carte.

## Affichage de vos articles de facturation
{: #viewbilling}

Vous pouvez associer des articles de facturation à des unités spécifiques, mais aussi les dissocier. Par défaut, la page
Articles de facturation affiche les articles de facturation associés. Vous pouvez changer la vue en sélectionnant une option depuis le menu d'affichage. L'association et la dissociation peuvent être effectuées pour un article ou pour
plusieurs articles à la fois avec l'opération Bulk Actions. Vous pouvez annuler des articles de facturation individuels à tout moment depuis la page Articles de facturation. Procédez comme suit pour associer ou dissocier vos articles de facturation sur la console.

1. Sélectionnez l'une des options suivantes en fonction du tableau de bord que vous utilisez :   
 * Dans le tableau de bord Applications ou Services, cliquez sur **Gérer** > **Facturation et utilisation** > **Facturation**.  
 * Dans le tableau de bord Infrastructure, cliquez sur **Compte** > **Facturation** > **Articles de facturation**.
2. Pour filtrer votre vue, sélectionnez dans la liste une option d'élément de facturation.

## Affichage de vos factures
{: #viewinvoices}

Vous pouvez à tout moment consulter ou régler une facture. Le récapitulatif de chaque facture comporte le numéro de la facture, sa date, son type, ainsi que divers soldes. Les types de facture sont classés comme suit :

 *  Nouveau : première facture d'une série de factures récurrentes
 *  Récurrent : facture de frais périodiques actifs sur le compte pour plusieurs mois
 *  Frais ponctuels : frais uniques correspondant à diverses dépenses et pouvant inclure des dépassements
 *  Crédit : crédit accordé par {{site.data.keyword.Bluemix_notm}} sur le solde du compte
 *  Remboursement : remboursement ou annulation de frais, qu'ils soient ponctuels ou périodiques.

La page Factures affiche également un récapitulatif de la facturation pour le compte, qui inclut le solde en cours et le prochain solde estimé, la méthode de paiement, ainsi que la dernière date et la prochaine date de facture récurrente.

Procédez comme suit pour afficher une facture :

1. Sélectionnez l'une des options suivantes, selon le tableau de bord que vous utilisez :  
 * Dans le tableau de bord Applis ou Services, cliquez sur **Gérer** > **Facturation et utilisation** > **Factures**.  
 * Dans le tableau de bord Infrastructure, cliquez sur **Compte** > **Facturation** > **Factures**.
2. Vous pouvez afficher une facture dans le portail client ou la télécharger.

## Utilisation de services {{site.data.keyword.Bluemix_notm}} avec des actifs SoftLayer
{: #combined}

Vous pouvez utiliser sans difficulté des services {{site.data.keyword.Bluemix_notm}} publics reposant sur des API avec vos actifs SoftLayer. Toutes les API sont sécurisées et chiffrées de sorte que vos données sont protégées.

Par exemple, souhaiteriez-vous ajouter des capacités cognitives de Watson à vos applications s'exécutant sur des serveurs sans système d'exploitation depuis SoftLayer ? Vous pouvez ajouter un service tel que {{site.data.keyword.personalityinsightsshort}} pour mieux comprendre l'utilisateur de votre application en quatre étapes :

1. Recherchez le service dans le catalogue.
2. Mettez en place une instance du service en quelques clics.
3. Configurez le service pour son exécution avec le code existant en copiant les données d'identification au service et en les ajoutant à votre application.
4. Après la mise à jour de l'application, déployez sa nouvelle version dans votre infrastructure SoftLayer.

Vous pouvez dégager des enseignements Insights and Cognitive en appelant des API Watson depuis vos applications dans SoftLayer pour les personnaliser davantage. Vous pouvez également utiliser les services Data and Analytics pour exploiter des analyses à hautes performances dans vos applications. Vous pouvez aussi opter pour une approche DBaaS (database-as-a-service) où la gestion est laissée à {{site.data.keyword.Bluemix_notm}}.

Modernisez votre développement d'applications en utilisant des conteneurs avec des services tels que {{site.data.keyword.activedeployshort}} et {{site.data.keyword.deliverypipeline}}. Vous pourrez ensuite utiliser le service {{site.data.keyword.vpn_short}} pour communiquer avec SoftLayer et connecter votre conteneur dans un réseau privé au réseau privé SoftLayer. Tous les frais d'utilisation des ressources de calcul et des services sont reflétés dans votre facture {{site.data.keyword.Bluemix_notm}}.
