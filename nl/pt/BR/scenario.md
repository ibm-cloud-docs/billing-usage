---

copyright:

  years: 2015, 2018
lastupdated: "2018-11-15"

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
* Banco de dados {{site.data.keyword.cloudant_short_notm}} de 150 GB por mês, 1.000 procuras, 500 gravações
e 50 consultas.
* 20 GB de tráfego de rede de entrada e saída


## Preços para recursos do {{site.data.keyword.Bluemix_notm}}
{: #sample_resources}

Para manter o exemplo simples, suponha que os preços na tabela a seguir não flutuam dentro ou entre um
prazo, por exemplo, um mês. Toda a precificação neste exemplo é em moeda dos EUA.

| Serviço                           |	Recursos                                                            |	Preço             |
|-----------------------------------|---------------------------------------------------------------------|-------------------|
| {{site.data.keyword.runtime_nodejs_short}}                   |	375 GB/horas grátis por mês (compartilhados entre todos os tempos de execução)            |	$0,07 USD/GB/hora |
| {{site.data.keyword.autoscaling}} |	Plano de serviço grátis para o serviço {{site.data.keyword.autoscaling}} |	Grátis              |
| {{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}} - Lite | Inclui 20 GB de
armazenamento de dados grátis</br>Escale a capacidade de rendimento provisionada em incrementos de:</br>100 consultas por segundo</br>50 gravações por segundo</br>5 consultas por segundo | $1,00 USD/GB de armazenamento de dados</br>$0,25 USD/Lookup por segundo</br>$0,50 USD/Gravação por segundo</br>US$ 5,00/consulta por segundo |
{:caption="Tabela 1.  Preços para recursos" caption-side="top"}


## Calculando o preço do app
{: #calc-app-price}

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

<dt>150 GB por mês de  {{site.data.keyword.cloudant_short_notm}}</dt>
<dd>As cobranças de serviço do {{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}} são baseadas no armazenamento de dados e na capacidade de acessar esses dados por capacidade de rendimento provisionada denotada
por procuras, gravações e consultas por segundo.
<p>
Inclua o número de GB e deduza o abono grátis de 20 GB. 130 GB é cobrado por mês. O preço total do armazenamento inclui as partes a seguir:</p>
<pre class="codeblock">
<codeblock>
    130 x 1 = $130
    (1,000 / 100) x 0.25 = $2.50
    (500 / 50) x 0.50 = $5.00
    (50 / 5) x 5.00 = $50.00
</codeblock>
</pre>
<p>
O preço total é 130 + 2,50 + 5,00 + 50,00 = US$ 187,50.</p></dd>

<dt>20 GB de tráfego de rede de entrada e saída</dt>
<dd>O tráfego de rede de entrada e saída é livre de encargo.</dd>

</dl>

Quando todos os itens forem incluídos, o preço total do aplicativo será US$ 211,65.
