---



copyright:

  years: 2015, 2018
lastupdated: "2018-11-16"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Facturation
{: #charges}

Le prix varie selon les ressources utilisées par un service, un contexte d'exécution, un conteneur ou une option de support spécifique. Les ressources peuvent correspondre au nombre d'appels d'API, au nombre d'instances, à la mémoire ou au stockage. {{site.data.keyword.Bluemix}} met à disposition des estimateurs de coût vous permettant de planifier vos frais.
{:shortdesc}


Une fois que vous avez généré vos ressources, vous pouvez vérifier leur coût réel. Accédez à **Gérer > Facturation et utilisation** puis sélectionnez **Utilisation**. Avec un compte de facturation {{site.data.keyword.Bluemix_notm}}, vous êtes facturé pour les ressources de calcul, les conteneurs et les services utilisés par votre organisation. Vous pouvez être invité par d'autres utilisateurs
{{site.data.keyword.Bluemix_notm}} à participer à des organisations sur un compte différent. L'utilisation des applications ou des services dans les organisations auxquelles vous êtes invité est facturée dans le compte incluant ces organisations. D'autres informations sur un tarif spécifique sont visibles sur chaque page des détails de ressource.

Différents types de prix s'appliquent selon les fonctions {{site.data.keyword.Bluemix_notm}} que vous utilisez. Une présentation générale est effectuée dans le tableau suivant :

| Type de frais | Description      | Type de ressource            | Exemple                  |
|----------------|------------------|--------------------------|--------------------------|
| Fixe          | La tarification fixe repose sur un prix mensuel convenu qui n'est pas ajusté. | Services  | Pour les serveurs Bare Metal, vous pouvez effectuer une sélection parmi plusieurs plans fixes, ces derniers étant facturés à un taux mensuel fixe. |
| Au compteur        | La tarification au compteur repose sur le nombre de Go/heure consommés pour les contextes d'exécution, sur le nombre d'adresses IP et le stockage consommés pour les conteneurs. | Services, ressources de calcul et conteneurs | Pour le service Push, toute utilisation dépassant la franchise mensuelle est facturée. |
| Différenciée         | Certains plans de tarification s'appuient sur un modèle de tarification différenciée ; ainsi, vous pouvez obtenir une remise selon le volume en fonction de votre utilisation réelle. Les services peuvent proposer des plans de tarification par tranches simples, graduées ou fixes. | Services | En général, la tarification différenciée est utilisée pour les paramètres de calcul des frais pour lesquels des quantités élevées par mois sont prévues, comme les appels d'API. |
| Réservé       | La tarification réservée repose sur un engagement à long terme pour un service, qui permet d'obtenir une remise. Avec un plan réservé, vous obtenez une instance de service dédiée facile à configurer, à déployer et à distribuer dans l'environnement {{site.data.keyword.Bluemix_notm}} public. | Services | DB2 on Cloud propose des plans réservés.|
{:caption="Tableau 1. Prix sur la base des fonctions" caption-side="top"}


## Plans Lite
{: #liteplans}

Les plans Lite sont structurés en tant que quota gratuit. Vous pouvez utiliser vos projets gratuitement, sans risque de générer une facture par accident. Le quota peut fonctionner pour une période spécifique, par exemple, un mois, ou sur la base d'une utilisation unique. La liste suivante répertorie quelques exemples de quotas de plan Lite :

   * Nombre maximal de périphériques enregistrés
   * Nombre maximal de liaisons d'application
   * Limite de stockage de données chiffrées, par exemple, 1 Go
   * Débit mis à disposition

Vous pouvez facilement trouver des services pour des plans Lite dans le catalogue. Par défaut, tous les services dotés d'un plan Lite sont affichés et identifiés par une balise Lite ![Balise Lite](../icons/Lite.svg). Sélectionnez un service pour afficher les détails du quota du plan Lite associé.


## Prix des ressources de calcul
{: #compute}

Vous êtes facturé pour la durée pendant laquelle vos applications s'exécutent et pour la mémoire qui est utilisée, en *Go/heure*. La quantité de Go/heure correspond au nombre d'instances d'application, multiplié par la quantité de mémoire par instance et par le nombre d'heures d'exécution des instances. Vous pouvez personnaliser le nombre d'instances et la quantité de mémoire par instance selon vos besoins. Vous pouvez également ajouter de la mémoire ou des instances afin de pouvoir satisfaire un plus grand nombre d'utilisateurs. Pour obtenir le montant facturé, multipliez vos instances d'application par la mémoire par instance et par le nombre d'heures d'exécution.

Par exemple, imaginez que vous disposez d'un contexte d'exécution qui coûte 0,07 $ par Go/heure dans deux instances de 512 Mo, qui s'exécutent pendant 30 jours (720 heures). Ces ressources coûtent 24,15 $, avec une franchise de 375 Go/heure, selon le calcul suivant :

```
2 instances x
0,5 Go x 720 heures = 720 Go/heure.
(720 - 375) Go/heure x 0,07 $ par Go/heure = 24,15 $
```

## Prix des services
{: #charges-services}

De nombreux services incluent des franchises mensuelles. L'utilisation de services qui ne sont pas inclus dans la franchise est facturée de l'une des façons suivantes :
<dl>
<dt>Tarification fixe</dt>
    <dd>Vous sélectionnez un plan et payez un forfait. Par exemple, les serveurs Bare Metal sont facturés au forfait.</dd>
<dt>Tarification au compteur</dt>
    <dd>Vous payez en fonction de la consommation que vous faites des contextes d'exécution et des services. Par exemple, avec le service Push, toute utilisation dépassant
la franchise mensuelle est facturée.</dd>
<dt>Tarification réservée</dt>
    <dd><p>En tant que propriétaire d'un compte de type Paiement à la carte ou Abonnement, vous pouvez réserver une instance de service avec un engagement à long terme en échange d'une remise. Par exemple, vous pouvez réserver l'offre DB2 on Cloud de grande taille standard pour 12 mois.</p>
    <p>Certains services {{site.data.keyword.Bluemix_notm}} offrent des plans réservés. Vous pouvez demander un plan réservé à partir du catalogue {{site.data.keyword.Bluemix_notm}} en cliquant sur la vignette du service. Ensuite, sélectionnez le plan de service le mieux adapté à vos besoins. Si un plan réservé est disponible, cliquez sur <strong>Demande</strong> et suivez les invites pour envoyer votre demande. Vous recevrez un courrier électronique contenant les informations sur le prix du plan réservé. Un ingénieur commercial {{site.data.keyword.Bluemix_notm}} prendra également contact avec vous rapidement pour finaliser l'achat.</p></dd>
<dt>Tarification différenciée</dt>
    <dd>A l'instar de la tarification au compteur, le prix que vous payez dépend de la consommation que vous faites des contextes d'exécution et des
services. Toutefois, la tarification différenciée propose des tranches de tarification supplémentaires et permet souvent de bénéficier de remises dans les tranches de consommation élevée. La tarification différenciée peut être par tranches simples, graduées ou fixes.</dd>
</dl>

### Tranche simple
{: #simple_tier}

Dans le modèle à tranches simples, le prix unitaire est déterminé par la tranche représentant la quantité que vous utilisez. Le prix total est la quantité que vous utilisez multipliée par le prix unitaire dans cette tranche, par exemple :

| Quantité d'éléments   | Prix unitaire pour tous les éléments |
|---------------------|--------------------------|
| Tranche 1 : 1 à 1000    | 1 $                   |
| Tranche 2 : 1001 à 2000 | 0,90 $                |
| Tranche 3 : 2001 à 3000 | 0,75 $                |
| Tranche 4 : 3001 à 4000 | 0,60 $                |
| Tranche 5 : &gt; 4000   | 0,40 $                |
{:caption="Tableau 2. Tarification à tranches simples" caption-side="top"}

Le tableau suivant indique le montant que vous payez avec un plan qui s'appuie sur un modèle de tarification à tranches simples :

| Quantité d'éléments | Calcul du prix | Prix total |
|-------------------|--------------------|-------------|
| 500               | 500 × 1 = 500      | 500 $    |
| 1500              | 1500 × 0,90 = 1350 | 1350 $   |
| 2500              | 2500 × 0,75 = 1875 | 1875 $   |
| ...               | ...                | ...         |
| 5200              | 5200 × 0,40 = 2080 | 2080 $   |
{:caption="Tableau 3. Calcul des frais à l'aide du modèle de tarification à tranches simples" caption-side="top"}

### Tranche graduée
{: #graduated_tier}

Dans le modèle à tranches graduées, le prix unitaire par tranche diminue à mesure que votre niveau d'utilisation augmente. Le prix total correspond aux frais cumulés pour chaque niveau d'utilisation, c'est-à-dire la quantité que vous utilisez multipliée par le prix unitaire de chaque tranche,

| Quantité d'éléments   |	Prix unitaire pour les éléments dans la tranche|
|---------------------|---------------------------------|
| Tranche 1 : 1 à 1000    |	1 $                          |
| Tranche 2 : 1001 à 2000 |	0,90 $                       |
| Tranche 3 : 2001 à 3000 |	0,75 $                       |
| Tranche 4 : 3001 à 4000 |	0,60 $                       |
| Tranche 5 : &gt; 4000   |	0,40 $                       |
{:caption="Tableau 4. Tarification à tranches graduées" caption-side="top"}

Le tableau suivant indique le montant que vous payez avec un plan qui s'appuie sur un modèle de tarification à tranches graduées :

|Quantité d'éléments | Calcul du prix                                                               | Prix total |
|------------------|----------------------------------------------------------------------------------|-------------|
| 500              | 500 × 1 (prix unitaire pour la tranche 1) = 500                                            |	500 $    |
| 1500             | (1000 × 1 (prix unitaire pour la tranche 1)) + (500 × 0.90 (prix unitaire pour la tranche 2)) = 1450 |	1450 $   |
| 2500             | (1000 × 1 (prix unitaire pour la tranche 1)) + (1000 × 0.90 (prix unitaire pour la tranche 2)) + (500 × 0.75 (prix unitaire pour la tranche 3)) = 2275 | 2275 $ |
| ...              | ...                                                                              | ...         |
| 5200             | (1000 × 1 (prix unitaire pour la tranche 1)) + (1000 × 0.90 (prix unitaire pour la tranche 2)) + (1000 × 0.75 (prix unitaire pour la tranche 3)) + (1000 × 0.60 (prix unitaire pour la tranche 4)) + (1200 × 0.40 (prix unitaire pour la tranche 5)) = 3730 | 3730 $ |
{:caption="Tableau 5. Calcul des frais à l'aide du modèle de tarification à tranches graduées" caption-side="top"}

### Tranche fixe
{: #block_tier}

Dans le modèle à tranches fixes, le prix est fixe pour la quantité que vous utilisez dans le cadre d'un niveau d'utilisation. Le prix total correspond aux frais pour votre niveau d'utilisation, quelle que soit votre utilisation réelle. Chaque tranche suivante propose un rapport prix/quantité inférieur. Exemple :

|Quantité d'éléments    |	Prix total pour tous les éléments |
|---------------------|---------------------------|
| Tranche 1 : &lt;= 1000  |	1000 $                 |
| Tranche 2 : &lt;= 2000  |	1900 $                 |
| Tranche 3 : &lt;= 3000  |	2800 $                 |
| Tranche 4 : &lt;= 4000  |	3500 $                 |
| Tranche 5 : &lt;= 10000 |	5000 $                 |
{:caption="Tableau 6. Tarification à tranches fixes" caption-side="top"}

Le tableau suivant indique le montant que vous payez avec un plan qui s'appuie sur un modèle de tarification à tranches fixes :

|Quantité d'éléments | Calcul du prix                                                      | Prix total|
|------------------|-------------------------------------------------------------------------|------------|
| 500              | Le nombre d'éléments correspond à la tranche 1 ; par conséquent, le prix total est 1000 $. | 1000 $  |
| 1500             | Le nombre d'éléments correspond à la tranche 2 ; par conséquent, le prix total est 1900 $. | 1900 $  |
| ...              | ...                                                                     | ...        |
| 5200             | Le nombre d'éléments correspond à la tranche 5 ; par conséquent, le prix total est 5000 $. | 5000 $  |
{:caption="Tableau 7. Calcul des frais à l'aide du modèle de tarification à tranches fixes" caption-side="top"}
