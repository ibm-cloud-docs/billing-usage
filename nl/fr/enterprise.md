---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise billing, enterprise, subscription, billing unit, billing option, invoice, credit pool

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}

# Gestion centrale de la facturation et de l'utilisation avec les entreprises
{: #enterprise}

Les entreprises vous permettent de gérer centralement plusieurs comptes {{site.data.keyword.Bluemix}}. Etant donné que la facturation est séparée des comptes enfant individuels et qu'elle est consolidée au niveau de l'entreprise, les entreprises simplifient la gestion de la facturation et des paiements pour les comptes.
{: shortdesc}

Vous êtes novice en matière d'entreprises {{site.data.keyword.Bluemix_notm}} ? Voir [Qu'est-ce qu'une entreprise ?](/docs/account?topic=account-enterprise) pour savoir comment les entreprises peuvent vous aider à gérer de manière centralisée la facturation et l'utilisation.
{: tip}

## Modèle de facturation d'entreprise
{: #enterprise-billing-basics}

Dans une entreprise, la facturation est gérée par l'entreprise et non par les comptes enfant individuels. Vous trouverez ci-dessous les différences entre le modèle de facturation centralisé et un compte autonome.

 * Le crédit des abonnements ou des promotions des comptes ajoutés dans l'entreprise est consolidé dans le pool de crédit de l'entreprise. L'administrateur de facturation ajoute de nouveaux abonnements au pool de crédit à partir du compte d'entreprise.
 * L'utilisation effectuée dans tous les comptes est déduite du pool de crédit partagé. S'ils disposent de l'accès, les utilisateurs de l'entreprise peuvent afficher les coûts d'utilisation pour tous les comptes et groupes de comptes de l'entreprise. Les utilisateurs de chaque compte enfant peuvent continuer de surveiller l'utilisation du compte spécifique mais ils n'ont aucune visibilité sur les autres comptes de l'entreprise.
 * L'utilisation est facturée dans l'ensemble du compte de l'entreprise. Seul l'administrateur de facturation de l'entreprise peut consulter les factures et gérer les paiements.

<figure>
<a href="https://{DomainName}/docs/api/content/billing-usage/images/enterprise-billing-usage.svg">
<img src="images/enterprise-billing-usage.svg" alt="Le crédit des comptes est ajouté au pool de crédit de l'entreprise, géré par l'administrateur de facturation dans le compte d'entreprise. L'accès d'utilisation est géré séparément et peut s'appliquer à l'entreprise, à un groupe de comptes ou à un compte."></a>
<figcaption>Figure 1. Gestion de l'utilisation et de la facturation d'entreprise</figcaption>
</figure>

## Options de facturation
{: #enterprise-billing-options}

Les entreprises ont besoin de facturation d'abonnement, ce qui signifie que vous achetez un abonnement pour une quantité de crédit à dépenser pendant la durée de l'abonnement. L'utilisation est déduite du crédit d'abonnement à un tarif réduit. Le compte que vous utilisez pour créer l'entreprise doit être un [compte Abonnement](/docs/account?topic=account-accounts#subscription-account). Une fois que l'entreprise est créée, vous pouvez ajouter tout type de compte à l'entreprise. Si vous ajoutez un compte Lite ou d'essai, il est automatiquement mis à niveau en compte Paiement à la carte.

Chaque entreprise prend en charge une seule devise de facturation. Tous les comptes doivent utiliser la devise de facturation de l'entreprise pour pouvoir être ajoutés à l'entreprise.
{: note}

Les comptes ajoutés à l'entreprise ne gèrent plus séparément leur facturation. Par conséquent, le crédit d'abonnement ne peut pas être ajouté à des comptes enfant individuels. Il doit être ajouté au compte d'entreprise, où il est intégré au pool de crédit de l'entreprise.

### Transfert de la facturation lors de l'ajout de comptes
{: #billing-transition}

Lorsque vous ajoutez un compte existant à une entreprise, sa facturation est alors gérée par le compte de l'entreprise. Cette transition inclut les modifications suivantes apportées au compte.

   * Pour les comptes Abonnement ajoutés, le type de compte devient Paiement à la carte. Cette modification indique que la compte ne dispose pas de ses propres abonnements mais qu'il a toujours un accès total aux services prêts pour la production et facturables.
   * Les abonnements et les promotions de chaque compte sont déplacés dans le compte de l'entreprise, où ils sont alors intégrés au pool de crédit. Après le déplacement, chaque abonnement a le même crédit restant et la même durée mais un nouvel ID unique lui est attribué.
   * L'accès aux informations de facturation et de paiement pour les périodes de facturation futures est restreint aux utilisateurs du compte de l'utilisateur. Les utilisateurs d'un compte enfant ne peuvent pas accéder aux informations de facturation et de paiement (factures, paiements ou abonnements, par exemple) même s'ils avaient précédemment accès au compte. Pour afficher ou gérer la facturation, les utilisateurs doivent être invités dans le compte de l'entreprise et ils doivent disposer de l'accès au service de facturation dans ce compte.
   * L'utilisation est facturée au compte de l'entreprise pour l'ensemble du mois durant lequel le compte a été ajouté. Par exemple, si vous ajoutez un compte à l'entreprise le 15 juin, l'ensemble de l'utilisation du mois de juin apparaît dans la facture du mois de juillet.

### Pool de crédit partagé
{: #credit-pool}

Le pool de crédit d'entreprise consolide le crédit de tous les comptes de l'entreprise et le partage avec les comptes. Le pool inclut le crédit de toutes les sources, notamment le crédit d'abonnement de plateforme, le crédit promotionnel et le crédit de support. Lorsque les comptes de l'entreprise créent et utilisent des ressources, le coût de cette utilisation est déduit du pool de crédit.

L'administrateur de facturation du compte d'entreprise peut afficher et surveiller la quantité totale du crédit disponible dans le tableau de bord de l'entreprise. Si du crédit supplémentaire est requis pour couvrir l'utilisation de l'entreprise, un nouvel abonnement peut être acheté puis ajouté au compte de l'entreprise. Il n'est possible d'ajouter des abonnements qu'au compte de l'entreprise et non à d'autres comptes au sein de l'entreprise.

Les abonnements pouvant cibler l'entreprise dans son ensemble et non chaque compte, vous disposez des avantages suivants :
   * Définition plus simple de la taille de l'abonnement, les abonnements s'appliquant à plusieurs comptes
   * Remises plus intéressantes sur les coûts d'utilisation car les abonnements sont de plus grande taille
   * Moins de dates d'expiration à suivre et à gérer une fois les abonnements existants arrivés à expiration

Dans une entreprise, les abonnements sont gérés à partir du compte d'entreprise de la même façon qu'à partir d'un compte autonome. Voir [Gestion des abonnements](/docs/billing-usage?topic=billing-usage-subscriptions) pour plus d'informations sur la gestion des abonnements de plateforme et de support.

## Génération de rapports d'utilisation
{: #enterprise-usage-reporting}

Les entreprises fournissent des rapports d'utilisation descendants afin que vous puissiez effectuer le suivi des coûts de l'utilisation des ressources dans tous les comptes de l'entreprise. A partir du niveau de l'entreprise, vous pouvez parcourir la structure de l'entreprise afin de voir les coûts d'utilisation estimés dans chaque compte ou groupe de comptes. Au niveau du compte, les utilisateurs de l'entreprise peuvent consulter les coûts de chaque type de ressource ou de service dans le compte.

Les administrateurs d'entreprise peuvent fournir un accès précis aux utilisateurs afin qu'ils puissent afficher l'utilisation uniquement pour certains groupes de comptes ou comptes. Par exemple, supposons que votre entreprise a des groupes de comptes pour chaque service et que chaque service a des groupes de comptes pour chaque équipe.
   * Vous accordez au responsable financier l'accès lui permettant de consulter l'ensemble de l'entreprise afin qu'il puisse effectuer le suivi des coûts et en effectuer le recouvrement pour chaque service.
   * Vous accordez à chaque responsable de service l'accès lui permettant de consulter l'utilisation de l'ensemble du groupe de comptes du service.
   * Vous accordez à chaque responsable d'équipe l'accès lui permettant de consulter uniquement les comptes du groupe de comptes de son équipe.

Etant donné que l'accès dans l'entreprise est séparé de l'accès dans chaque compte, les utilisateurs de l'entreprise ne peuvent pas automatiquement gérer des ressources dans les comptes enfant. De la même façon, les utilisateurs de chaque compte peuvent continuer à consulter leur utilisation passée et en cours sur la page Utilisation, qu'ils aient ou non accès à l'entreprise.

Vous pouvez consulter l'utilisation sur la page Utilisation de la console, à partir de l'interface CLI ou de l'API Enterprise Usage Reports. Pour plus d'informations, voir [Affichage de l'utilisation dans une entreprise](/docs/billing-usage?topic=billing-usage-enterprise-usage).

## Facturation et paiements
{: #enterprise-invoicing}

L'utilisation dans l'entreprise est facturée via le compte d'entreprise. Tout comme avec les comptes facturables, l'utilisation est facturée sur une base mensuelle et la facture doit être réglée à la date de facturation pour votre compte. Durant chaque cycle de facturation, une seule facture avec les coûts d'utilisation de tous les comptes est disponible dans le compte de l'entreprise. La facture inclut les coûts pour l'ensemble de l'utilisation de plateforme et d'infrastructure sur une seule ligne. Si l'ensemble du crédit du pool de crédit est utilisé, la facture inclut une ligne pour tout frais d'utilisation excédentaire.

Etant donné que l'ensemble de l'utilisation est facturée via le compte d'entreprise, les comptes enfant ne reçoivent pas de factures séparées.

Vous pouvez analyser les coûts d'utilisation de chaque compte ou groupe de comptes sur la page Utilisation dans le compte d'entreprise. Pour plus de détails, voir [Affichage de l'utilisation dans une entreprise](/docs/billing-usage?topic=billing-usage-enterprise-usage).
{: tip}

## Gestion de l'accès pour l'utilisation et la facturation de l'entreprise
{: #enterprise-billing-access}

Tout comme avec les autres rôles de gestion d'entreprise, l'accès à l'utilisation et à la facturation d'entreprise est géré via le compte d'entreprise. Les utilisateurs doivent être invités à rejoindre ce compte et une règle d'accès doit leur être affectée avec un rôle sur le service approprié.

Dans une entreprise, l'accès à la facturation et l'accès à l'utilisation sont affectés séparément.

   * L'accès à la facturation est fourni en affectant aux utilisateurs de l'entreprise un rôle sur le service Facturation. Par exemple, vous pouvez affecter le rôle Afficheur à un utilisateur de l'entreprise de telle sorte qu'il puisse afficher la quantité de crédit d'abonnement disponible dans le pool de crédit ou vous pouvez affecter le rôle Editeur ou Administrateur afin que l'utilisateur puisse ajouter de nouveaux abonnements ou gérer des méthodes de paiement.
   * L'accès à l'utilisation est fourni en affectant aux utilisateurs de l'entreprise le rôle Administrateur, Editeur ou Afficheur des rapports d'utilisation sur le service Enterprise. Vous pouvez affecter cet accès pour l'ensemble de l'entreprise ou pour des groupes de comptes et des comptes spécifiques.

Si vous souhaitez que votre administrateur de facturation puisse afficher les coûts par compte ou groupe de comptes, pensez à lui affecter l'accès approprié à la fois sur le service Entreprise et sur le service Facturation.
{: tip}

Pour plus d'informations, voir [Gestion des utilisateurs et de l'accès pour les entreprises](/docs/iam?topic=iam-enterprise-access).
