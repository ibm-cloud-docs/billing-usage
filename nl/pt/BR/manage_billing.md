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

# Gerenciando o uso de contas vinculadas do {{site.data.keyword.Bluemix_notm}}
{: #linkedusage}

Se você tiver uma conta do {{site.data.keyword.Bluemix}} e do SoftLayer vinculada, será possível usar o portal do cliente para fazer um pagamento único, mudar os detalhes de seu cartão de pagamento, visualizar seus itens de faturamento e visualizar suas faturas.
{: shortdesc}

As opções de faturamento e uso que são exibidas no console do {{site.data.keyword.Bluemix_notm}} poderão ser diferentes se você tiver uma conta grátis ou se não tiver uma conta do {{site.data.keyword.Bluemix_notm}} e do SoftLayer vinculada.
{: tip}

## Fazendo um pagamento
{: #makepayment}

É possível fazer um pagamento único a qualquer momento. O pagamento pode ser pelo saldo total ou por uma quantia parcial e os detalhes inseridos para o pagamento não serão registrados. Conclua as etapas a seguir para fazer um pagamento único.

1. Selecione uma das opções a seguir, dependendo de qual painel você estiver usando:   
 * No painel Apps ou Serviços, clique em **Gerenciar** > **Faturamento e uso** > **Fazer um pagamento**.  
 * No painel Infraestrutura, clique em **Conta** > **Fazer um pagamento**.
3. No campo **Quantia de pagamento**, insira a quantia que deseja pagar.
4. Selecione seu método de pagamento:
 * Pagar com um cartão de crédito. Insira os detalhes de seu cartão e o endereço para cobrança do cartão. Em seguida, clique em **Fazer pagamento com cartão de crédito**.
 * Pagar com PayPal. Digite seus detalhes quando solicitado para concluir o pagamento.

Resolva os problemas relatados com o pagamento. O Saldo da conta é atualizado depois de o pagamento ser aceito. É possível entrar em contato com a equipe de Suporte clicando em **Suporte** > **Incluir chamado**.

## Mudando o método de pagamento
{: #changepaymethod}

Cada conta faturável deve ter um cartão de crédito registrado que seja válido. Todo mês, o cartão de crédito é cobrado com a quantia de uso acumulada durante esse mês. No console do {{site.data.keyword.Bluemix_notm}}, conclua as etapas a seguir para incluir ou mudar os detalhes de seu pagamento.

1. Selecione uma das opções a seguir, dependendo de qual painel você estiver usando:  
 * No painel Apps ou Serviços, clique em **Gerenciar** > **Faturamento e uso** > **Modificar método de pagamento**.  
 * No painel Infraestrutura, clique em **Conta** > **Faturamento** > **Método de pagamento**.
2. Na seção Incluir método de pagamento, insira os detalhes do cartão de crédito e o endereço para cobrança do cartão. Em seguida, clique em **Incluir cartão de crédito**.

Os detalhes de seu cartão são validados e, em seguida, o cartão ficará disponível para uso em sua conta dentro de 24 horas. Um e-mail de confirmação é
enviado para o contato inserido na seção de endereço para cobrança do cartão.

## Visualizando os itens de faturamento
{: #viewbilling}

É possível associar itens de faturamento a dispositivos específicos e também desassociá-los. Por padrão, a
página Itens de faturamento exibe itens de faturamento associados. É possível mudar a visualização selecionando uma opção no
menu de exibição. A associação e desassociação podem ocorrer para um item ou para mais de um item de cada vez usando a operação Ações em massa. Os itens de faturamento individuais podem ser cancelados a qualquer momento na página Itens de faturamento. Conclua as etapas a seguir para associar ou desassociar os itens de faturamento no console.

1. Selecione uma das opções a seguir, dependendo de qual painel você estiver usando:   
 * No painel Apps ou Serviços, clique em **Gerenciar** > **Faturamento e uso** > **Faturamento**.  
 * No painel Infraestrutura, clique em **Conta** > **Faturamento** > **Itens de faturamento**.
2. Para filtrar sua visualização, selecione uma opção de item de faturamento na lista.

## Visualizando suas faturas
{: #viewinvoices}

As faturas podem ser visualizadas ou pagas a qualquer momento. Cada fatura é resumida pelo Número da fatura, Data, Tipo de fatura e vários
saldos monetários. Os tipos de fatura são categorizados como segue:

 *  Nova: a primeira fatura em uma série de faturas recorrentes
 *  Recorrente: uma fatura para encargos contínuos que estão ativos na conta há mais de um mês
 *  Encargos únicos: uma tarifa única para várias despesas, que podem incluir excedentes
 *  Crédito: um crédito do {{site.data.keyword.Bluemix_notm}} para o saldo da conta
 *  Reembolso: um reembolso ou uma reversão para um encargo único ou contínuo

A página Faturas também exibe um resumo de faturamento da conta, que inclui o próximo saldo atual e estimado,
o método de pagamento e a última e a próxima datas da fatura recorrente.

Conclua as etapas a seguir para visualizar uma fatura:

1. Selecione uma das opções a seguir, dependendo do painel que estiver sendo usado:  
 * No painel Apps ou Serviços, clique em **Gerenciar** > **Faturamento e uso** > **Faturas**.  
 * No painel Infraestrutura, clique em **Conta** > **Faturamento** > **Faturas**.
2. É possível visualizar uma fatura no portal do cliente ou fazer download da fatura.

## Usando os serviços do {{site.data.keyword.Bluemix_notm}} com ativos do SoftLayer
{: #combined}

É possível usar facilmente serviços públicos do {{site.data.keyword.Bluemix_notm}} baseados em API com os seus ativos do SoftLayer. Todas as APIs são seguras e criptografadas para que os seus
dados estejam protegidos.

Por exemplo, você já quis incluir recursos cognitivos do Watson em seus aplicativos em execução em servidores bare metal a partir do SoftLayer? É possível incluir um serviço como o {{site.data.keyword.personalityinsightsshort}} para ajudar a entender o usuário de seu aplicativo em quatro etapas:

1. Localize o serviço no catálogo.
2. Provisione uma instância do serviço com apenas alguns cliques.
3. Configure o serviço para executar com o seu código existente, copiando as credenciais de serviço e incluindo-as em seu aplicativo.
4. Após a atualização para o aplicativo, implemente a nova versão em sua infraestrutura do SoftLayer.

É possível obter Insights e Conhecimentos cognitivos chamando APIs do Watson de seus aplicativos no SoftLayer para torná-los mais personalizados. Ou, use serviços de Dados e Analítica para explorar a análise de alto desempenho para seus aplicativos. Ou,
escolha banco de dados como serviço no qual você pode deixar o
gerenciamento para o
{{site.data.keyword.Bluemix_notm}}.

Modernize o seu desenvolvimento de aplicativo usando contêineres com serviços como {{site.data.keyword.activedeployshort}} e
{{site.data.keyword.deliverypipeline}}. É possível, então, usar o serviço do {{site.data.keyword.vpn_short}} para se comunicar com o SoftLayer
para conectar o seu contêiner em uma rede privada com a rede privada do SoftLayer. Todos os encargos de uso dos recursos de cálculo e serviços são refletidos em sua conta do {{site.data.keyword.Bluemix_notm}}.
