---



copyright:

  years: 2015, 2018
lastupdated: "2018-04-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Como você é cobrado
{: #charges}

Os encargos variam dependendo dos recursos que são usados por um determinado serviço, tempo de execução,
contêiner ou opção de suporte. O recurso pode ser o número de chamadas API, o número de instâncias, a memória, o armazenamento e assim por diante. {{site.data.keyword.Bluemix}} também fornece estimadores de custo detalhados e uma calculadora de custo que não deixa escapar nenhum centavo para ajudar você a planejar os encargos. 

Depois de construir seus apps, é possível verificar o custo real na página **Gerenciar** > **Faturamento e uso** > **Uso** > **Painel de uso**. Com uma conta faturável do {{site.data.keyword.Bluemix_notm}}, você é cobrado pelo cálculo, contêineres e serviços que são usados em sua organização. Você poderá ser convidado por outros usuários do {{site.data.keyword.Bluemix_notm}} a participar em organizações em uma conta diferente. Se você criar apps ou usar serviços nas organizações para as quais foi convidado, o uso que é incorrido será cobrado na conta que contém essas organizações. É possível ver mais informações sobre um encargo específico das páginas de detalhes do recurso.

Tipos diferentes de encargos se aplicam, dependendo dos recursos do {{site.data.keyword.Bluemix_notm}} que você está usando. A tabela a seguir fornece uma visão geral resumida:

| Tipo de encargo | Descrição | Recursos do {{site.data.keyword.Bluemix_notm}} que usam esse tipo de encargo | Exemplo |
|------------------|------------------|--------------------------|--------------------------|
| Ajustado | A precificação com taxa fixa é baseada em um encargo mensal acordado que não é ajustado. | Serviços  | O Cache de Dados tem um plano fixo que é cobrado em uma taxa mensal fixa. |
| Medido | A precificação com uso medido é baseada no número de GB/horas que são consumidos para tempos de
execução, no número de GB/horas consumidos e no número de endereços IP e de armazenamento para contêineres. | Serviços, cálculo e contêineres | Para o serviço de Push, todo uso acima do abono mensal grátis é cobrado. |
|  Disposto em camadas   |  Alguns planos de precificação são baseados em um modelo de precificação em camadas, de modo que seja possível obter um desconto baseado em volume de acordo com o seu uso real. O serviços podem oferecer planos de precificação simples, graduados ou de camada de bloco. | Serviços | 
A precificação em camadas é geralmente usada para métricas de encargo que devem ter quantidades altas por mês,
como chamadas API. |
| Reserved | A precificação reservada é baseada em um compromisso a longo prazo para um serviço, portanto, é possível obter um preço com desconto. Com um plano reservado, você obtém uma instância de serviço dedicado que é fácil configurar, implementar e entregar no ambiente público do {{site.data.keyword.Bluemix_notm}}. | Serviços | O DB2 on Cloud tem planos reservados.|
{:caption="Tabela 1. Encargos com base em recursos" caption-side="top"}

## Planos Lite
{: #liteplans}

Os planos Lite, que estão disponíveis em contas Lite e pré-pagas, são estruturados como uma cota grátis. É possível trabalhar em seus projetos sem preocupações, sem o risco de gerar uma conta acidental. A cota pode operar por um período específico, por exemplo um mês ou em uma base de uso único. A lista a seguir fornece alguns exemplos de cotas do plano Lite:

   * Número máximo de dispositivos registrados
   * Número máximo de ligações de aplicativos
   * Limite de armazenamento de dados criptografados, por exemplo 1 GB
   * Capacidade de rendimento provisionada

É possível localizar facilmente planos Lite no catálogo. Por padrão, todos os serviços com um plano Lite
são exibidos com uma tag Lite ![Tag Lite](../icons/Lite.svg). Selecione um serviço para
visualizar os detalhes da cota para o plano Lite associado.

## Encargos para recursos de cálculo
{: #compute}

Você é cobrado pelo tempo de execução dos apps e memória usada, calculado como *GB/horas*. 
GB/horas é o cálculo do número de instâncias do aplicativo, que é multiplicado pela memória por instância e,
em seguida, multiplicado pelas horas de execução das instâncias. É possível customizar o número de instâncias e a quantia de memória por instância com base em suas necessidades. Também é possível incluir memória ou instâncias para escalar mais usuários. 
O encargo final é por GB/hora: o número de suas instâncias do aplicativo, que é multiplicado pela memória por
instância e, em seguida, multiplicado pelas horas em execução.

Por exemplo, considere um tempo de execução que custe $0,07 por GB/hora em duas instâncias de 512 MB, em execução por 30 dias (720 horas). Esses  recursos devem custar $24,15 USD, incluindo um abono grátis de 375 GB/horas, com os cálculos a seguir:

```
2 instâncias x 0,5 GB x 720 horas = 720 GB/horas.
(720 - 375) GB/horas x $0,07 por GB/hora = $24,15
```

## Encargos para serviços
{: #services}

Vários serviços incluem abonos grátis mensais. O uso de serviços que não estão incluídos como parte do abono grátis é cobrado de uma das maneiras a seguir:
<dl>
<dt>Encargos fixos</dt>
    <dd>Selecione um plano e pague com uma taxa fixa. Por exemplo, o serviço de Cache de Dados é cobrado em uma taxa fixa.</dd>
<dt>Encargos medidos</dt>
    <dd>Você paga com base no consumo de tempo de execução e de serviço. Por exemplo, com o serviço de Push, qualquer uso acima do abono grátis mensal é cobrado.</dd>
<dt>Encargos reservados</dt>
    <dd><p>Como o proprietário da conta de uma conta Pagamento por uso ou uma conta de Assinatura, é possível reservar uma instância de serviço, com um compromisso a longo prazo, para um preço com desconto. Por exemplo, é possível reservar a grande oferta padrão do DB2 on Cloud para 12 meses.</p>
    <p>Alguns serviços do {{site.data.keyword.Bluemix_notm}} oferecem planos reservados. É possível solicitar um plano reservado no catálogo do {{site.data.keyword.Bluemix_notm}} clicando no tile do serviço. Em seguida, selecione o plano de serviço que atenda melhor às suas necessidades. Se um plano reservado estiver disponível, clique em <strong>Solicitar</strong> e siga os prompts para enviar sua solicitação. 
Você recebe um e-mail que contém as informações de preços do plano reservado. Um representante de vendas do
{{site.data.keyword.Bluemix_notm}} também entrará em contato com você em breve para concluir a compra.</p></dd>
<dt>Encargos em camadas</dt>
    <dd>Semelhante a encargos medidos, você paga com base em seu consumo de tempo de execução e de serviço. No
entanto, os encargos em camadas incluem mais camadas de precificação, geralmente oferecendo encargos com
desconto em camadas com consumo maior. A precificação em camadas é oferecida em simples, graduada ou bloco.</dd>
</dl>

### Camada simples
{: #simple_tier}

No modelo de camada simples, o preço unitário é determinado pela camada na qual a sua quantidade de uso se enquadra. 
O preço total é a sua quantidade que é multiplicada pelo preço unitário na respectiva camada. Por exemplo:

| Quantidade de itens | Preço unitário para todos os itens |
|-------------------|--------------------------|
| Camada 1: 1 - 1.000  | US$ 1                   |
| Camada 2: 1.001 - 2.000    |    US$ 0,90                      |
| Camada 3: 2.001 - 3.000                  |   US$ 0,75                       |
| Camada 4: 3.001 - 4.000           |      US$ 0,60                    |
|Camada 5: &gt; 4.000 | US$ 0,40 |
{:caption="Tabela 2. Tabela de precificação de camada simples" caption-side="top"}

A tabela a seguir ilustra o quanto do valor que você paga pelo seu plano se baseia em um modelo de precificação de camada simples:

| Quantidade de itens | Cálculo de encargo | Preço Total |
|-------------------|--------------------|-------------|
|500 |	500 × 1 = 500 |	US$ 500|
|1.500 |	1.500 × 0,90 = 1.350 |	US$ 1.350|
|2.500 |	2.500 × 0,75 = 1.875 |	US$ 1.875|
|... |	... |	...|
|5.200 |	5.200 × 0,40 = 2.080 |US$ 2.080|
{:caption="Tabela 3. Cálculo de encargo usando o modelo de precificação de camada simples" caption-side="top"}

### Camada graduada
{: #graduated_tier}

No modelo de camada graduada, o preço unitário por camada diminui à medida que o seu nível de uso aumenta. O preço total é o somatório de encargos em cada nível de uso, compostos pela quantidade multiplicada pelo preço unitário na respectiva camada. Por exemplo:

| Quantidade de itens |	Preço unitário dos itens na camada|
|-------------------|------------------------------------|
|    Camada 1: 1 - 1.000 |	US$ 1 |
|   Camada 2: 1.001 - 2.000 |	US$ 0,90 |
|    Camada 3: 2.001 - 3.000 |	US$ 0,75 |
|    Camada 4: 3.001 - 4.000 |	US$ 0,60 |
|    Camada 5: &gt; 4.000 |	US$ 0,40 |
{:caption="Tabela 4. Tabela de precificação de camada graduada" caption-side="top"}

A tabela a seguir ilustra o quanto do valor que você paga pelo seu plano se baseia em um modelo de precificação de camada graduada:

|Quantidade de itens | Cálculo de encargo | Preço total|
|------------------|--------------------|------------|
|500 |	500 × 1 (preço unitário da Camada 1) = 500 |	US$ 500|
|1.500 |	(1000 × 1 (preço unitário da Camada 1) + (500 × 0,90 (preço unitário da Camada 2)) = 1450 |	US$ 1.450|
|2.500 |	(1000 × 1 (preço unitário da Camada 1) + (1000 × 0,90 (preço unitário da Camada 2) + (500 × 0,75 (preço unitário da Camada 3)) = 2275 |	US$ 2.275 |
|... |	... |	...|
|5.200 |	(1000 × 1 (preço unitário da Camada 1) + (1000 × 0,90 (preço unitário da Camada 2) + (1000 × 0,75 (preço unitário da Camada 3) + (1000 × 0,60 (preço unitário da Camada 4) + (1200 × 0,40 (preço unitário da Camada 5)) = 3730 |	US$ 3.730|
{:caption="Tabela 5. Cálculo de encargo usando o modelo de precificação de camada graduada" caption-side="top"}

### Camada em bloco
{: #block_tier}

No modelo de camada em bloco, o preço é um encargo definido pela quantidade utilizada em um nível de uso. O preço total é o encargo do seu nível de uso, independentemente do uso real. Cada camada sucessiva resulta em um preço menor para a razão de quantidade. Por exemplo:

|Quantidade de itens |	Preço total para todos os itens|
|------------------|-----------------------------|
| Camada 1: &lt;= 1.000 |	US$ 1.000|
| Camada 2: &lt;= 2.000 |	U$ 1.900|
| Camada 3: &lt;= 3.000 |	US$ 2.800|
| Camada 4: &lt;= 4.000 |	US$ 3.500|
| Camada 5: &lt;= 10.000 |	US$ 5.000|
{:caption="Tabela 6. Tabela de precificação de camada de bloco" caption-side="top"}

A tabela a seguir ilustra o quanto do valor que você paga pelo seu plano se baseia em um modelo de precificação de camada em bloco:

|Quantidade de itens |	Cálculo de encargo |	Preço total|
|------------------|-----------------------|---------------|
|500 |	O número de itens se enquadra na Camada 1, assim o preço total é US$ 1.000. |	US$ 1.000|
|1.500 |	O número de itens se enquadra na Camada 2, assim o preço total é US$ 1.900. |	U$ 1.900|
|... |	... |	...|
|5.200 |	O número de itens se enquadra na Camada 5, assim o preço total é US$ 5.000. |	US$ 5.000|
{:caption="Tabela 7. Cálculo de encargo usando o modelo de precificação de camada de bloco" caption-side="top"}
