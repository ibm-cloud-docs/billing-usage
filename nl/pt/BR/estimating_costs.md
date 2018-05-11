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

# Como calcular seus custos
{: #cost}

É possível usar diferentes métodos para estimar o custo do uso de recursos de
plataforma como serviço (PaaS) e de infraestrutura como serviço (IaaS) do {{site.data.keyword.Bluemix}} para construir e hospedar seus
apps.
{:shortdesc}

É possível usar os métodos a seguir para determinar seus custos:
* Use a [calculadora de precificação
![Ícone de link externo](../icons/launch-glyph.svg)](https://console.bluemix.net/pricing/){: new_window} para
estimar o custo total dos recursos de plataforma e de infraestrutura que você deseja utilizar.
* Use os estimadores de custo no {{site.data.keyword.Bluemix_notm}}
{{site.data.keyword.pricing_sheet}} para ver uma estimativa aproximada do custo com base no tamanho de
seu app.
* Use a calculadora de custo na página Precificação para ver os preços de apps precisos com base em sua
entrada de usos de tempo de execução e de serviço.
* Calcule seu custo manualmente.

## Usando a calculadora de precificação
{: #pricing-calculator}

É possível usar a calculadora de precificação para estimar o custo de muitos recursos de plataforma e
de infraestrutura antes de fazer uma compra.
A calculadora de precificação fornece as funções a seguir:
  * Estimativas de custo que são atualmente fornecidas na moeda USD.
  * Estimativas para recursos de infraestrutura que estão atualmente disponíveis para as
categorias **Cálculo** e **Contêineres**.
  * Estimativas de custo de recursos que não incluem descontos atualmente.
  * Estimativas de custos são fornecidas para propósitos de planejamento.

1. Acesse a calculadora de precificação em uma das seguintes maneiras:
  * Na [Página de precificação
![Ícone de link externo](../icons/launch-glyph.svg)](https://www.ibm.com/cloud/pricing){: new_window}, clique
em **Tentar a calculadora** na seção Explorar nossas soluções.
  * Se você não estiver atualmente com login efetuado no {{site.data.keyword.Bluemix_notm}},
clique em **Precificação** na página inicial do
[{{site.data.keyword.Bluemix_notm}}
![Ícone de link externo](../icons/launch-glyph.svg)](https://console.bluemix.net/).
2. Nas listas **Infraestrutura** ou **Plataforma**, selecione a
categoria do recurso que você deseja precificar. Os recursos na categoria que você selecionou são mostrados e
também é possível procurar na categoria por um recurso específico.
3. Selecione um recurso na categoria para ver uma descrição dele. Alguns recursos possuem múltiplas opções. Por exemplo, se você selecionar **Infraestrutura** > **Cálculo** > **Servidores bare metal**, será possível escolher entre uma lista de servidores. 
4. Selecione a quantidade do recurso a ser incluída.
5. Clique em **Incluir na estimativa**.
6. Continue incluindo recursos nas categorias **Infraestrutura** e **Plataforma** até que você inclua o que deseja estimar.

O painel **Estimativa** mostra os recursos que você incluiu, o preço de cada um e o preço total. 

Se você estiver precificando apenas os recursos da plataforma, será possível clicar em
**Alternar para a calculadora clássica** para ver uma estimativa em uma moeda diferente de
USD. A calculadora clássica não inclui recursos de infraestrutura.
{: tip}

### Usando a calculadora clássica para recursos de plataforma
{: #calculator}

Para calcular os custos de recursos de sua plataforma em uma moeda diferente de USD, é possível usar a
calculadora clássica. A calculadora clássica não fornece estimativas de precificação para recursos de
infraestrutura.

1. Acesse o {{site.data.keyword.Bluemix_notm}} {{site.data.keyword.pricing_sheet}}.
2. Selecione uma das opções na infraestrutura para suportar todas as suas cargas de trabalho na seção.

Para usar a calculadora, digite seu uso mensal projetado dos recursos listados, por exemplo, o número de instâncias ou de notificações push. A calculadora exibe o preço de sua entrada imediatamente. Também é possível ajustar a calculadora para exibir custos anuais, em vez de mensais.

## Calculando seus custos manualmente
{: #manual}

Você pode desejar estimar seus custos do {{site.data.keyword.Bluemix_notm}} para entender melhor como os custos do {{site.data.keyword.Bluemix_notm}} são calculados. É possível calcular o preço total do uso do {{site.data.keyword.Bluemix_notm}} para construir e hospedar seu app considerando os preços do tempo de execução e os serviços que ele usa. 
Como os preços de tempos de execução e de serviços às vezes mudam, deve-se consultar as informações
mais recentes sobre a folha de precificação do {{site.data.keyword.Bluemix_notm}} ao
calcular o preço total.

## Moedas de faturamento suportadas

A tabela a seguir lista as moedas de faturamento que estão disponíveis.

|Código ISO 4217| Moeda|
|-------------|---------|
|AUD |	  Dólar australiano|
|BRL |	  Real brasileiro|
|CAD |	  Dólar canadense|
|CHF |	  Franco suíço|
|DKK |	  Coroas dinamarquesas|
|EUR |	  Euro|
|GBP |	  Libra Esterlina|
|INR |	  Rúpia Indiana|
|JPY |	  Iene japonês|
|KRW |	  Uon sul-coreano|
|NOK |	  Coroa Norueguesa|
|NZD |	  Dólar da Nova Zelândia|
|SEK |	  Coroa sueca|
|USD |    Dólar americano|
|ZAR |	  Rand sul-africano|
{:caption="Tabela 1. Moedas suportadas" caption-side="top"}

Se você tiver vinculado suas contas do {{site.data.keyword.Bluemix_notm}} e do SoftLayer, a única fatura que receberá será apenas em dólares americanos (US$). Para obter mais informações, consulte [Faturamento consolidado para contas vinculadas](/docs/account/linking_accounts.html).
{: tip}
