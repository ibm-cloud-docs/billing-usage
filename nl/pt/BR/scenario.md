---

copyright:

  years: 2015, 2018
lastupdated: "2018-04-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Cenário: estimando os custos de um app de Nó de exemplo
{: #sample}

Suponha que você tenha um app da web Node.js com recursos de ajuste de escala e o app usa
vários serviços que são fornecidos pelo {{site.data.keyword.Bluemix}}. É possível aprender como o custo real de seu app é calculado neste exemplo. O app da web usa os serviços e itens do {{site.data.keyword.Bluemix_notm}} a seguir:

* Quatro instâncias de tempo de execução do Node.js de 256 MB
* Duas políticas de {{site.data.keyword.autoscaling}}, processador e memória
* 2 GB por mês de {{site.data.keyword.datacshort}}
* 150 GB por mês de banco de dados NoSQL, 100.000 chamadas API pesadas e 500.000 chamadas API leves
* 20 GB de tráfego de rede de entrada e saída

## Preços para recursos do {{site.data.keyword.Bluemix_notm}}
{: #sample_resources}

Para manter o exemplo simples, suponha que os preços na tabela a seguir não flutuam dentro ou entre um
prazo, por exemplo, um mês. Toda a precificação neste exemplo é em moeda dos EUA.

|Serviço |	Recursos |	Preço |
|--------|-----------|--------|
|SDK for Node.js |	375 GB/horas grátis por mês (compartilhados entre todos os tempos de execução) |	$0,07 USD/GB/hora|
|{{site.data.keyword.autoscaling}} |	Plano de serviço grátis para o serviço {{site.data.keyword.autoscaling}} |	Grátis|
|{{site.data.keyword.datacshort}} - Starter |	1 GB de espaço em cache e uma réplica |	$55,00 USD/instância |
|{{site.data.keyword.datacshort}} -
Standard |	5 GB de espaço em cache e uma réplica |	$155,00 USD/instância |
|{{site.data.keyword.datacshort}} -
Premium |	25 GB de espaço em cache e uma réplica |	$505,00 USD/instância|
|IBM Cloudant® NoSQL DB for {{site.data.keyword.Bluemix_notm}} |	2 GB de armazenamento de dados grátis<br/>50.000 chamadas API leves grátis por mês<br/>10.000 chamadas API pesadas grátis por mês | $1,00 USD/GB<br/>$0,03 USD/1000 chamadas API leves<br/>$0,15 USD/1000 chamadas API pesadas |
{:caption="Tabela 1.  Preços para recursos" caption-side="top"}

## Calculando o preço do app

O preço do app pode ser calculado da maneira a seguir:

<dl>
<dt>Quatro instâncias de tempo de execução do Node.js de 256 MB</dt>
<dd>O
{{site.data.keyword.Bluemix_notm}} cobra por
um tempo de execução por GB/horas. O número de GB usado por mês é <code>4 x 256 = 1024 MB ou 1 GB por mês</code>. Suponha que haja <code>24 x 30 = 720 horas em um mês</code>, portanto, o aplicativo é cobrado por <code>1 x 720 = 720 GB/horas</code>.
<p>
375 GB/horas são incluídos em um abono grátis por mês, que é compartilhado entre todos os tempos de execução
do {{site.data.keyword.Bluemix_notm}}. Assim, o custo total para o tempo de execução é <code>$0,07 x (720-375) = $24,15</code>.</p></dd>

<dt>Duas políticas de
{{site.data.keyword.autoscaling}} (processador
e memória)</dt>
<dd>As políticas de
{{site.data.keyword.autoscaling}} são livres
de encargos.</dd>

<dt>2 GB por mês de {{site.data.keyword.datacshort}}</dt>
<dd>O plano de 50 MB que é fornecido pelo serviço
{{site.data.keyword.datacshort}} é livre de encargos. Porém, o plano livre não cobriria o seu uso projetado de 2 GB por mês. Os três planos pagos para o {{site.data.keyword.datacshort}} custam uma quantia configurada para uma
quantia de espaço específica, independentemente de quanto espaço você utiliza. Portanto, você deseja escolher o plano mínimo que atenda ao seu uso projetado, que é o plano padrão de 5 GB. O custo total é de $155 por mês.</dd>

<dt>150 GB por mês no banco de dados NoSQL</dt>
<dd>Os encargos de serviço do Cloudant NoSQL DB para {{site.data.keyword.Bluemix_notm}} são baseados no armazenamento de dados e na capacidade de acessar esses dados por diferentes métodos de API. Os comandos <strong>PUT</strong> e <strong>POST</strong> são considerados como chamadas API pesadas, mas os comandos <strong>GET</strong> são considerados como chamadas API leves.
<p>
Inclua o número de GB e deduza um abono grátis de 2 GB. 148 GB é cobrado por mês. Subtraia o abono grátis de 50.000 para chamadas API leves e 10.000 para chamadas API pesadas. O preço total do armazenamento inclui as partes a seguir:</p>
<pre class="codeblock">
<codeblock>
    148 x 1 = $148
    (450.000 / 1000) x 0,03 = $13,5
    (90.000 / 1000) x 0,15 = $13,5
</codeblock>
</pre>
<p>
O preço total é 148 + 13,5 + 13,5 = $175.</p></dd>

<dt>20 GB de tráfego de rede de entrada e saída</dt>
<dd>O tráfego de rede de entrada e saída é livre de encargo.</dd>

</dl>

Quando todos os itens são incluídos, o preço total do aplicativo é de US$ 354,15.
