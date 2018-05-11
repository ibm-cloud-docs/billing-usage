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

# Gerenciando o uso de contas vinculadas do {{site.data.keyword.Bluemix_notm}}
{: #linkedusage}

Se você tiver uma conta do {{site.data.keyword.Bluemix}} e do SoftLayer vinculada, será possível usar o portal do cliente para fazer um pagamento único, mudar os detalhes de seu cartão de pagamento, visualizar seus itens de faturamento e visualizar suas faturas.
{: shortdesc}

As opções de faturamento e de uso que são exibidas no console do {{site.data.keyword.Bluemix_notm}}
podem ser diferentes quando você tem uma conta Lite ou quando você não tem uma conta vinculada.
{: tip}

## Fazendo um pagamento
{: #makepayment}

É possível fazer um pagamento único a qualquer momento. O pagamento pode ser pelo saldo total ou por uma
quantia parcial. Os detalhes que você insere para o pagamento não serão registrados. Conclua as etapas a
seguir para fazer um pagamento único:

1. Na barra de menus, clique em **Gerenciar** > **Faturamento e
uso** > **Fazer um pagamento**.  
2. No campo **Valor do pagamento**, insira a quantia que você deseja pagar.
3. Selecione seu método de pagamento:
 * Pagar com um cartão de crédito. Insira os detalhes de seu cartão e o endereço para cobrança do cartão. Em seguida, clique em **Fazer pagamento com cartão de crédito**.
 * Pagar com PayPal. Digite seus detalhes quando solicitado para concluir o pagamento.

Resolva os problemas relatados com o pagamento. O saldo da conta é atualizado depois de o pagamento ser aceito. É possível entrar em contato com a equipe de Suporte clicando em **Suporte** > **Incluir chamado**.

## Mudando o método de pagamento
{: #changepaymethod}

Cada conta faturável deve ter um cartão de crédito registrado que seja válido. Todo mês, o cartão de crédito é cobrado com a quantia de uso acumulada durante esse mês. 
No console do {{site.data.keyword.Bluemix_notm}}, conclua as etapas a seguir para incluir ou mudar os
detalhes de seu pagamento:

1. Na barra de menus, clique em **Gerenciar** > **Faturamento e
uso** > **Modificar método de pagamento**.  
2. Na seção Incluir método de pagamento, insira os detalhes do cartão de crédito e o endereço para cobrança do cartão. Em seguida, clique em **Incluir cartão de crédito**.

Os detalhes de cartão são validados e seu cartão se torna, então, disponível para uso em sua conta dentro
de 24 horas. Um e-mail de confirmação é
enviado para o contato inserido na seção de endereço para cobrança do cartão.

## Visualizando os itens de faturamento
{: #viewbilling}

É possível associar ou desassociar itens de faturamento para dispositivos específicos. Por padrão, a
página **Itens de faturamento** exibe itens de faturamento associados. É possível mudar a visualização selecionando uma opção no
menu de exibição. É possível associar ou desassociar um item ou usar a operação Ações em massa para associar
ou desassociar múltiplos itens por vez. Também é possível cancelar itens de faturamento individuais a qualquer
momento. 

1. Selecione a opção **ícone Menu ![ícone Menu](../icons/icon_hamburger.svg) >Infraestrutura**. 
2. Na barra de menus, clique em **Conta** > **Faturamento** >
**Itens de faturamento**.
3. Para filtrar sua visualização, selecione uma opção de item de faturamento na lista.

## Visualizando suas faturas
{: #viewinvoices}

É possível visualizar ou pagar suas faturas a qualquer momento. Cada fatura é resumida pelo Número da
fatura, Data, Tipo de fatura e vários saldos monetários. Os tipos de fatura são descritos na lista a seguir:

 *  Nova: a primeira fatura em uma série de faturas recorrentes
 *  Recorrente: uma fatura para encargos contínuos que estão ativos na conta há mais de um mês
 *  Encargos únicos: uma tarifa única para várias despesas, que podem incluir excedentes
 *  Crédito: um crédito do {{site.data.keyword.Bluemix_notm}} para o saldo da conta
 *  Reembolso: um reembolso ou uma reversão para um encargo único ou contínuo

A página **Faturas** também exibe um resumo de faturamento da conta, que inclui
o saldo atual e o próximo saldo estimado, o método de pagamento e as datas da última fatura e da próxima fatura
recorrente.

Conclua as etapas a seguir para visualizar uma fatura:

1. Selecione a opção **ícone Menu ![ícone Menu](../icons/icon_hamburger.svg) >Infraestrutura**. 
2. Na barra de menus, clique em **Conta** > **Faturamento** >
**Faturas**.
3. É possível visualizar uma fatura no portal do cliente ou fazer download da fatura.

## Usando os serviços do {{site.data.keyword.Bluemix_notm}} com ativos do SoftLayer
{: #combined}

É possível usar facilmente serviços públicos do {{site.data.keyword.Bluemix_notm}} baseados em API com os seus ativos do SoftLayer. Todas as APIs são seguras e criptografadas para que os seus
dados estejam protegidos.

Por exemplo, você deseja incluir recursos cognitivos do Watson em seus apps que estão em execução em
servidores bare metal por meio do SoftLayer? É possível incluir um serviço como o {{site.data.keyword.personalityinsightsshort}} para ajudar a entender o usuário de seu aplicativo em quatro etapas:

1. Localize o serviço no catálogo.
2. Provisione uma instância do serviço com apenas alguns cliques.
3. Configure o serviço para executar com o seu código existente, copiando as credenciais de serviço e incluindo-as em seu aplicativo.
4. Após a atualização para o aplicativo, implemente a nova versão em sua infraestrutura do SoftLayer.

É possível obter Insights e Conhecimentos cognitivos chamando APIs do Watson de seus aplicativos no SoftLayer para torná-los mais personalizados. 
Ou então, use serviços de Dados e de Análise de dados para explorar a análise de dados de alto desempenho para
seus apps. Ou,
escolha banco de dados como serviço no qual você pode deixar o
gerenciamento para o
{{site.data.keyword.Bluemix_notm}}.

Modernize o seu desenvolvimento de aplicativo usando contêineres com serviços como {{site.data.keyword.activedeployshort}} e
{{site.data.keyword.deliverypipeline}}. É possível, então, usar o serviço do {{site.data.keyword.vpn_short}} para se comunicar com o SoftLayer
para conectar o seu contêiner em uma rede privada com a rede privada do SoftLayer. Todos os encargos de uso dos recursos de cálculo e serviços são refletidos em sua conta do {{site.data.keyword.Bluemix_notm}}.
