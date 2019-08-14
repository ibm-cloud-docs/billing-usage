---

copyright:
  years: 2019
lastupdated: "2019-08-06"

keywords: enterprise billing, enterprise, subscription, billing unit, billing option, invoice, credit pool

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}

# Gerenciando de modo centralizado o faturamento e o uso com empresas
{: #enterprise}

As empresas permitem gerenciar centralmente múltiplas contas do {{site.data.keyword.Bluemix}}. Como o faturamento é separado de contas-filhas individuais e consolidado para o nível corporativo, as empresas simplificam o gerenciamento de cobrança, faturamento e pagamentos para as contas.
{: shortdesc}

Novo nas empresas do {{site.data.keyword.Bluemix_notm}}? Consulte [O que é uma empresa?](/docs/account?topic=account-enterprise) para obter mais detalhes sobre como as empresas podem ajudar você a gerenciar centralmente o faturamento e o uso.
{: tip}

## Modelo de faturamento corporativo
{: #enterprise-billing-basics}

Em uma empresa, o faturamento é gerenciado pela empresa em vez de em contas-filhas individuais. Esse modelo de faturamento centralizado difere de uma conta independente das maneiras a seguir.

 * O crédito de quaisquer assinaturas ou promoções existentes em contas que são incluídas na empresa é consolidado no conjunto de crédito da empresa. O administrador de faturamento inclui novas assinaturas no conjunto de crédito por meio da conta corporativa.
 * O uso de todas as contas é deduzido do conjunto de crédito compartilhado. Se fornecido o acesso, os usuários corporativos poderão visualizar custos de uso para todas as contas e grupos de contas na empresa. Os usuários em cada conta-filha podem continuar monitorando o uso na conta específica, mas não têm visibilidade para outras contas na empresa.
 * O uso é faturado por meio da conta corporativa. Somente o administrador de faturamento corporativo pode visualizar faturas e gerenciar pagamentos.

<figure>
<a href="https://{DomainName}/docs/api/content/billing-usage/images/enterprise-billing-usage.svg">
<img src="images/enterprise-billing-usage.svg" alt="Uma diagrama que mostra que o crédito das contas é incluído no conjunto de crédito da empresa, que é gerenciado pelo administrador de faturamento na conta corporativa. O acesso de uso é gerenciado separadamente e pode ser destinado à empresa, a um grupo de contas ou a uma conta."></a>
<figcaption>Figura 1. Gerenciamento de faturamento e de uso corporativos</figcaption> </figure>

## Opções de Faturamento
{: #enterprise-billing-options}

As empresas requerem faturamento de assinatura, o que significa que você adquire uma assinatura por uma quantia de crédito para gastar durante o prazo de assinatura, e o uso é deduzido do crédito de assinatura a uma taxa descontada. A conta que você usa para criar a empresa deve ser uma [Conta de assinatura](/docs/account?topic=account-accounts#subscription-account). Depois que a empresa é criada, é possível incluir qualquer tipo de conta na empresa. Se você incluir uma conta Lite ou para teste, ela será submetida a upgrade automático para uma conta Pré-paga.

Algumas contas Pré-pagas não podem ser diretamente importadas em uma empresa, como muitas contas Pré-pagas que são faturadas em dólares dos Estados Unidos (USD). No entanto, ainda é possível importar essas contas em sua empresa, convertendo-as em Contas de assinatura e, em seguida, importando-as. Para converter uma conta, entre em contato com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}![Ícone de link externo](../icons/launch-glyph.svg).
{: note}

Cada empresa suporta apenas uma moeda de faturamento único. Todas as contas devem usar a moeda de faturamento corporativo antes de você incluí-las na empresa. As contas existentes que são importadas na empresa não gerenciam mais seu faturamento separadamente. Como resultado, o crédito de assinatura não pode ser incluído em contas-filhas individuais. O crédito de assinatura deve ser incluído na conta corporativa, na qual ele se torna parte do conjunto de crédito corporativo.

### Transição de faturamento ao incluir contas
{: #billing-transition}

Ao incluir uma conta existente em uma empresa, a cobrança e o faturamento passam a ser gerenciados pela conta corporativa. Essa transição inclui as mudanças a seguir na conta.

   * Para contas de Assinatura que são incluídas, o tipo de conta é mudado para Pré-paga. Essa mudança reflete que a conta não tem suas próprias assinaturas, mas que ainda tem acesso total aos serviços faturáveis prontos para produção.
   * As assinaturas e as promoções de cada conta são movidas para a conta corporativa, na qual elas se tornam parte do conjunto de crédito. Após a movimentação, cada assinatura tem o mesmo crédito restante e período de prazo, mas recebe um novo ID exclusivo.
   * O acesso às informações de faturamento e pagamento para os períodos de faturamento futuros é restrito aos usuários na conta corporativa. Os usuários em uma conta-filha não podem acessar informações de faturamento e pagamento, como faturas, pagamentos ou assinaturas, mesmo se anteriormente tinham acesso na conta. Para visualizar ou gerenciar o faturamento, os usuários precisam ser convidados para a conta corporativa e receber acesso ao serviço de Faturamento nessa conta.
   * O uso é faturado para a conta corporativa para o mês inteiro quando a conta foi incluída. Por exemplo, se você incluir uma conta na empresa em 15 de junho, todo o uso para o mês de junho será refletido na fatura de julho.

### Conjunto de crédito compartilhado
{: #credit-pool}

O conjunto de crédito corporativo consolida o crédito de todas as contas na empresa e compartilha-o com as contas. O conjunto inclui crédito de todas as origens, incluindo crédito de assinatura de plataforma, crédito promocional e crédito de suporte. Quando as contas na empresa criam e usam recursos, o custo para esse uso é deduzido do conjunto de crédito.

O administrador de faturamento na conta corporativa pode visualizar e monitorar a quantia total de crédito disponível no painel corporativo. Se mais crédito for necessário para cobrir o uso da empresa, uma nova assinatura poderá ser comprada e, em seguida, incluída na conta corporativa. As assinaturas podem ser incluídas somente na conta corporativa e não podem ser incluídas em outras contas na empresa.

Como as assinaturas podem ser dimensionadas para a empresa inteira em vez de por conta, você obterá os benefícios a seguir:
   * Dimensionamento de assinatura mais simples porque as assinaturas se aplicam a mais de uma conta
   * Melhores descontos nos custos de uso porque as assinaturas são maiores
   * Menos datas de expiração para rastrear e gerenciar após a expiração de assinaturas existentes

Em uma empresa, as assinaturas são gerenciadas por meio da conta corporativa da mesma maneira que para uma conta independente. Consulte [Gerenciando assinaturas](/docs/billing-usage?topic=billing-usage-subscriptions) para obter mais informações sobre o gerenciamento de suas assinaturas de plataforma e suporte.

## Relatório de uso
{: #enterprise-usage-reporting}

As empresas fornecem relatórios de uso descendente para que seja possível rastrear os custos de uso de recurso de todas as contas na empresa. No nível corporativo, é possível navegar dentro do nível corporativo para ver os custos de uso estimados dentro de cada conta ou grupo de contas. No nível de conta, os usuários corporativos podem visualizar custos para cada tipo de recurso ou serviço na conta.

Os administradores corporativos podem fornecer acesso granular a usuários para que eles possam visualizar o uso apenas para determinados grupos de contas ou contas. Por exemplo, digamos que sua empresa tenha grupos de contas para cada departamento e cada departamento tenha grupos de contas para cada equipe.
   * Você fornece acesso ao seu executivo financeiro para visualizar a empresa inteira para que eles possam rastrear e recuperar custos para cada departamento.
   * Você fornece acesso a cada líder de departamento para visualizar o uso de tudo no grupo de contas do departamento.
   * Você fornece acesso a cada líder de equipe para visualizar somente as contas no grupo de contas de sua equipe.

Como o acesso na empresa é separado do acesso em cada conta, os usuários corporativos não podem gerenciar automaticamente os recursos dentro das contas-filhas. Da mesma forma, os usuários em cada conta podem continuar visualizando seu uso passado e atual na página Uso, independentemente de eles terem acesso corporativo.

É possível visualizar o uso na página Uso no console, na CLI ou na API de Relatórios de uso corporativo. Consulte [Visualizando o uso em uma empresa](/docs/billing-usage?topic=billing-usage-enterprise-usage) para obter mais informações.

## Faturamento e pagamentos
{: #enterprise-invoicing}

O uso na empresa é faturado por meio da conta corporativa.  Assim como com todas as contas faturáveis, o uso é faturado mensalmente e a fatura vence na data de faturamento para sua conta. Durante cada ciclo de faturamento, uma única fatura com os custos de uso de todas as contas é disponibilizada na conta corporativa. A fatura contém custos para todo o uso de plataforma e de infraestrutura como um item de linha único em sua fatura. Se todo o crédito no conjunto de crédito for usado, a fatura conterá um item de linha para quaisquer encargos excedentes.

Como todo o uso é faturado por meio da conta corporativa, as contas-filhas dentro da empresa não recebem faturas separadas.

É possível analisar custos de uso para cada conta ou grupo de contas na página Uso na conta corporativa. Para obter detalhes, consulte [Visualizando o uso em uma empresa](/docs/billing-usage?topic=billing-usage-enterprise-usage).
{: tip}

## Gerenciamento de acesso para faturamento corporativo e uso
{: #enterprise-billing-access}

Assim como com outras funções de gerenciamento corporativo, o acesso ao faturamento corporativo e ao uso é gerenciado por meio da conta corporativa. Os usuários devem ser convidados para a conta corporativa e designados a uma política de acesso com uma função no serviço relevante.

Em uma empresa, o acesso de faturamento e o acesso de uso são designados separadamente.

   * O acesso de faturamento é fornecido designando a usuários corporativos uma função no serviço de Faturamento. Por exemplo, é possível designar a função de Visualizador a um usuário corporativo para que ele possa visualizar a quantia de crédito de assinatura disponível no conjunto de crédito ou é possível designar a função de Editor ou de Administrador para que ele possa incluir novas assinaturas ou gerenciar métodos de pagamento.
   * O acesso de uso é fornecido designando aos usuários corporativos a função de Visualizador de relatórios de uso, de Editor ou de Administrador no Serviço corporativo. É possível designar esse acesso para a empresa inteira ou para grupos de contas e contas específicos.

Se você deseja que o administrador de faturamento seja capaz de visualizar custos por conta ou grupo de contas, certifique-se de designar a eles o acesso apropriado no Serviço corporativo e no Serviço de faturamento.
{: tip}

Para obter mais informações, consulte [Gerenciamento de usuário e acesso para empresas](/docs/iam?topic=iam-enterprise-access).
