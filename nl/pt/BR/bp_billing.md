---

copyright:
  years: 2019
lastupdated: "2019-06-18"

keywords: best practice billing, best practice usage, automate billing, track costs

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Melhores práticas para faturamento e uso
{: #best-practices}

Siga nossas melhores práticas para rastrear os custos e automatizar o faturamento no {{site.data.keyword.Bluemix}}.
{:shortdesc}


## Rastrear custos para recursos relacionados incluindo tags
{:#track-billing-tags}

Inclua tags em seus recursos para organizar, rastrear e gerenciar custos para recursos relacionados. Quando você usa um esquema de identificação consistente para identificar quais recursos estão ligados a projetos específicos, é possível agrupar e filtrar por essas tags ao analisar custos dentro de seu relatório de uso exportado.

1. Identifique seus recursos usando um esquema de identificação consistente, como criar tags para diferenciar centros de custos, data centers, projetos ou equipes. Para incluir tags, clique no Ícone de menu ![Ícone de menu](../icons/icon_hamburger.svg) > **Lista de recursos**. Na coluna Tag, clique em **Incluir tag** para cada recurso que desejar identificar.

   Inclua tags em pares key:value para incluir colunas customizadas com base na chave no relatório de uso. Crie chaves com base nas categorias que você usa para organizar seus recursos, como o uso de `costcenter:` para agrupar por centro de custo ou `project:` para agrupar por projeto.
   {: tip}

   Por exemplo, é possível ter recursos para dois projetos em uma única conta, Projeto ABC e Projeto XYZ. O Projeto ABC possui um cluster {{site.data.keyword.containershort_notm}}, algumas implementações de app do Cloud Foundry e um banco de dados {{site.data.keyword.cloudant_short_notm}}. É possível incluir a tag `project:abc` em todos esses recursos para distinguir esses recursos para Projeto ABC de recursos semelhantes no Projeto XYZ que são identificados como `project:xyz`.

   Para obter mais informações sobre incluir e usar tags, consulte [Trabalhando com tags](/docs/resources?topic=resources-tag).

1. Rastreie custos para os recursos identificados exportando o relatório de uso para suas instâncias. Para exportar o relatório, acesse **Gerenciar > Faturamento e uso** e selecione **Uso**. Em seguida, clique em **Exportar CSV > Instância**.

   Use a coluna Tags no arquivo CSV de instância para ajudar a analisar os recursos em sua conta. É possível classificar os dados CSV de acordo com a tag do projeto em cada instância para que seja possível analisar melhor o custo dos projetos individuais. Se você identificou seus recursos com os pares key:value, também será possível ver colunas no relatório de uso que correspondam à chave. Por exemplo, recursos identificados como `project:abc` e `project:xyz` aparecem em uma coluna Projeto como "abc" e "xyz".

   Para obter mais informações, consulte [Visualizando seu uso](/docs/billing-usage?topic=billing-usage-viewingusage).

## Automatize o gerenciamento de faturamento e uso usando a CLI ou as APIs
{: #billing-cli-apis}

Se você deseja automatizar como você revisa o uso do seu recurso e quaisquer custos associados, é possível usar a CLI [`ibmcloud billing`](/docs/cli?topic=cloud-cli-ibmcloud_billing) ou as APIs [Medição de uso ![Ícone de link externo](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/usage-metering){: new_window} e [Relatórios de uso ![Ícone de link externo](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/metering-reporting){: new_window} para integrar esta funcionalidade aos seus próprios apps.

Para começar a usar as APIs, configure o [painel de amostra de uso do {{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../icons/launch-glyph.svg)](https://github.com/IBM-Cloud/openwhisk-cloud-usage-sample){: new_window}. Usando o {{site.data.keyword.openwhisk}}, a amostra implementa uma abordagem orientada a API para obter e visualizar os dados de uso e faturamento do {{site.data.keyword.Bluemix_notm}}.
{: tip}
