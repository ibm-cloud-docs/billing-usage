---

copyright:
  years: 2019
lastupdated: "2019-07-26"

keywords: enterprise usage, view enterprise costs, account group usage, account usage, cost recovery, chargeback, support cost

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:external: target="_blank" .external}
{:note: .note}


# Affichage de l'utilisation dans une entreprise
{: #enterprise-usage}

Vous pouvez effectuer le suivi des coûts et des ressources dans les comptes de votre entreprise {{site.data.keyword.Bluemix}} en consultant leur utilisation. Les comptes et les groupes de comptes dont vous pouvez voir l'utilisation dépendent de votre accès affecté.
{: shortdesc}

Les entreprises {{site.data.keyword.Bluemix_notm}} vous permettent de gérer centralement plusieurs comptes {{site.data.keyword.Bluemix_notm}}. En tant qu'utilisateur d'entreprise, vous pouvez surveiller l'utilisation des ressources et les coûts associés pour tout compte de l'entreprise. Voir [Qu'est-ce qu'une entreprise ?](/docs/account?topic=account-enterprise) pour plus d'informations.

## Accès requis pour l'affichage de l'utilisation de l'entreprise
{: #enterprise-usage-access}

Dans une entreprise, l'accès aux informations d'utilisation est contrôlé par le service Entreprise. Pour afficher les informations d'utilisation, les utilisateurs doivent être invités à rejoindre le compte de l'entreprise et doivent disposer du rôle Administrateur, Editeur ou Afficheur des rapports d'utilisation sur le service Entreprise. Le rôle Afficheur des rapports d'utilisation permet d'accéder uniquement à l'affichage des rapports d'utilisation alors que les rôles Editeur et Administrateur permettent d'effectuer d'autres actions de gestion d'entreprise. Conformément aux meilleures pratiques en matière de sécurité, affectez l'accès minimal permettant à l'utilisateur d'effectuer ses tâches. Pour plus d'informations, voir [Rôles et actions de l'entreprise](/docs/iam?topic=iam-account-services#enterprise-account-management).

Vous pouvez accorder aux utilisateurs un accès plus précis afin qu'ils puissent consulter l'utilisation d'un compte ou d'un groupe de comptes spécifique. Disons par exemple que votre entreprise a des groupes de comptes pour chaque service et que chaque service a des groupes de comptes pour chaque équipe. Vous pouvez définir l'accès de telle sorte que chaque utilisateur de l'entreprise puisse voir uniquement les informations dont il a besoin.
   * Votre responsable financier a besoin de consulter l'utilisation de l'ensemble de l'entreprise afin qu'il puisse effectuer le suivi et recouvrer les coûts pour chaque service mais il n'a pas besoin de créer de compte ou de groupe de comptes. Affectez-lui le rôle d'afficheur de rapports d'utilisation pour l'entreprise.
   * Chaque responsable de service doit consulter l'utilisation concernant son service et il doit également créer et gérer des comptes et des groupes de comptes pour son équipe. Affectez à chaque responsable de service le rôle Editeur pour le groupe de comptes de son service.
   * Chaque responsable d'équipe a besoin de consulter l'utilisation de son équipe mais vous souhaitez qu'il demande l'approbation du service pour pouvoir ajouter de nouveaux comptes à son équipe. Affectez à chaque responsable d'équipe le rôle d'afficheur de rapports d'utilisation pour le groupe de comptes de son équipe. Il peut consulter l'utilisation de tous les comptes du groupe de comptes mais non l'utilisation des groupes de comptes d'autres équipes du service.

Pour accéder à une procédure détaillée permettant d'affecter un accès d'entreprise, voir [Affectation de l'accès d'entreprise](/docs/iam?topic=iam-assign-access-enterprise).

## Affichage de l'utilisation d'entreprise
{: #enterprise-usage-console}

1. Connectez-vous au compte de l'entreprise.
1. Accédez à **Gérer > Facturation et utilisation** puis sélectionnez **Utilisation**.

   La page Utilisation affiche les coûts de l'ensemble de l'utilisation des ressources dans votre entreprise, répartie par compte et groupe de comptes. Vous pouvez également consulter l'utilisation du crédit de support pour l'ensemble de l'entreprise ainsi que tout dépassement.

   Les informations d'utilisation pour les services d'infrastructure classique ne sont pas incluses pour la période de facturation en cours. Toutefois, elles sont incluses pour les périodes de facturation précédentes, que vous pouvez afficher en sélectionnant un mois précédent dans le menu **Période**. Pour plus d'informations, voir [Affichage de l'utilisation pour vos ressources de l'infrastructure classique](/docs/billing-usage?topic=billing-usage-infra-usage).
1. Pour afficher l'utilisation dans un groupe de comptes, cliquez sur le nom du groupe de comptes ou dans le menu **Niveau de l'entreprise**. Comme pour le niveau d'entreprise, l'utilisation est répartie par compte et groupe de comptes.

   Si un groupe de comptes ne contient aucun compte, il ne s'affiche pas sur la page Utilisation.

1. Pour afficher l'utilisation par ressource, accédez au niveau de compte en cliquant sur les groupes de comptes dans le tableau ou en sélectionnant le compte dans le menu **Niveau de l'entreprise**. Les coûts de chaque type de ressource utilisé pendant la période définie sont affichés.

   A partir du compte d'entreprise, vous ne pouvez pas consulter les données d'utilisation de l'instance ou du plan de ressources car l'accès dans le compte est requis. Si vous êtes un utilisateur du compte, accédez au compte pour afficher ces données. Vous avez besoin de l'accès de facturation aux ressources et aux services du compte, comme cela est décrit dans [Affichage de votre utilisation](/docs/billing-usage?topic=billing-usage-viewingusage).

Seules les données de l'utilisation liées aux comptes de l'entreprise s'affichent dans le compte de l'entreprise. Pour afficher l'utilisation avant l'ajout d'un compte à l'entreprise, connectez-vous à ce compte et sélectionnez la période adaptée.
{: note}

### Affichage de l'utilisation de l'entreprise à l'aide de l'interface CLI
{: #enterprise-usage-cli}

Vous pouvez obtenir un rapport de l'utilisation pour l'entreprise, un groupe de comptes ou un compte spécifique.

1. Connectez-vous et sélectionnez le compte de l'entreprise.

   ```
   ibmcloud login
   ```
   {:codeblock}

1. Si vous souhaitez consulter l'utilisation pour un compte ou un groupe de comptes spécifique, recherchez le nom ou l'ID en exécutant la commande **`ibmcloud enterprise`**.

   Par exemple, la commande suivante affiche tous les groupes de comptes d'une entreprise.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}

1. Affichez l'utilisation en exécutant la commande **`ibmcloud billing`** comme cela est présenté dans les exemples suivants.

   * Afficher l'utilisation de l'ensemble de l'entreprise pour le mois en cours.

      ```
      ibmcloud billing enterprise-usage
      ```
      {: codeblock}

   * Afficher l'utilisation du groupe de comptes `Development` pour le mois de juillet 2019.

      ```
      ibmcloud billing enterprise-usage --account-group Development --month 2019-07
      ```
      {:codeblock}

   * Afficher l'utilisation des groupes de comptes et des comptes directement sous l'entreprise.

      ```
      ibmcloud billing enterprise-usage --children
      ```
      {:codeblock}

   Par défaut, les commandes génèrent le rapport d'utilisation du mois en cours au format suivant. La plupart des coûts sont répertoriés comme coûts facturables. Les coûts non facturables sont répertoriés dans de très rares cas, par exemple pour le mois durant lequel vous ajoutez un compte d'essai à l'entreprise.

   ```
   Name             Type            Billable Cost   Non-billable Cost   Currency   Month   
Example Corp     account         123.45          0                   USD        2019-07   
Development      account_group   234.56          0                   USD        2019-07   
Marketing        account_group   345.67          0                   USD        2019-07   
Sales            account_group   456.78          0                   USD        2019-07
   ```

   Vous pouvez générer la sortie au format JSON en spécifiant l'option `--output JSON`.
   {: tip}

### Affichage de l'utilisation de l'entreprise à l'aide de l'API
{: #enterprise-usage-api}

Vous pouvez obtenir des rapports d'utilisation d'une entreprise et de ses comptes en appelant l'[API Enterprise Usage Reports (version bêta)](https://{DomainName}/apidocs/enterprise-apis/resource-usage-reports){: external}. Vous pouvez créer la requête dans votre appel d'API en fonction d'une entreprise, d'un groupe de comptes ou d'un compte et indiquer si vous souhaitez afficher l'entité ou ses enfants. L'API Enterprise Usage Reports est une version bêta.

Les exemples suivants présentent des requêtes que vous pouvez utiliser pour obtenir différents rapports d'utilisation. Lorsque vous appelez l'API, remplacez les variables d'ID et le jeton IAM par les valeurs de votre entreprise.

Afficher l'utilisation de l'ensemble de l'entreprise pour le mois en cours.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

Afficher l'utilisation d'un groupe de comptes pour le mois de juillet 2019.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?account_group_id=$ACCOUNT_GROUP_ID&month=2019-07" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

Afficher l'utilisation des groupes de comptes et des comptes directement sous l'entreprise.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID&children=true" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}


## Recouvrement des coûts pour l'utilisation de l'entreprise
{: #enterprise-cost-recovery}

Une entreprise consolide la facturation à partir de tous ses comptes et groupes de comptes dans une seule facture, ce qui simplifie la gestion de la facturation. Vous pouvez recouvrer les coûts découlant de l'utilisation des ressources dans l'entreprise en facturant les coûts d'utilisation pour chaque groupe de comptes ou compte au service ou à l'équipe associé.

Pour afficher la structure de l'entreprise et l'utilisation, vous devez disposer d'une règle d'accès avec le rôle Editeur ou Administrateur sur le service Entreprise pour l'ensemble de l'entreprise. La procédure suivante utilise la console {{site.data.keyword.Bluemix_notm}} en tant qu'exemple mais il est également possible de suivre cette procédure en utilisant l'interface CLI ou l'API.

1. Recherchez les coûts d'utilisation de chaque service en sélectionnant **Gérer > Utilisation** dans le compte de l'entreprise. Dans le menu **Période**, sélectionnez le mois précédent pour afficher l'utilisation incluse dans la dernière facture.

  Les coûts des groupes de comptes sont répertoriés dans le tableau. Ces coûts incluent tous les frais à l'exception des taxes facturées dans votre zone de facturation. Si vous souhaitez avoir une répartition plus détaillée des coûts d'utilisation, cliquez sur le nom du groupe de comptes pour afficher les comptes et les groupes de comptes qu'il contient.

1. Identifiez les services de votre entreprise qui correspondent aux groupes de comptes.

   Si les contacts affectés à vos groupes de comptes sont associés au service à partir duquel vous souhaitez recouvrer les coûts, la recherche du contact constitue la seule méthode permettant de trouver ces informations. Accédez à **Gérer > Entreprise** puis sélectionnez **Comptes**. Le contact de chaque groupe de comptes est répertorié dans le tableau.

   Toutefois, les pratiques en matière de facturation varient en fonction des différentes entreprises. Par exemple, le contact du groupe de comptes peut être un coordinateur technique qui n'est pas associé au service que vous souhaitez facturer. Vérifiez toujours le service correct en fonction des processus de comptabilité de votre entreprise.

   Si votre entreprise utilise des codes de facturation pour facturer les coûts aux services, ajoutez un code de ce type au nom du groupe de comptes pour identifier facilement le code. Par exemple, `Ventes - A2B3`.
   {: tip}

1. Associez les coûts d'utilisation pour chaque groupe de comptes au service identifié et suivez les processus de l'entreprise afin de soumettre les frais.
