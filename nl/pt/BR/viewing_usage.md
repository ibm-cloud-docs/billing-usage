---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-03"

keywords: view usage, view cost, service usage, usage access, usage report

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}


# Visualizando seu uso
{: #viewingusage}

É possível visualizar os detalhes de uso, incluindo um resumo dos encargos estimados para todos os recursos, serviços e planos de suporte que são usados por mês em suas organizações, na página Uso no console do {{site.data.keyword.Bluemix}}.
{:shortdesc}

Os gerentes de faturamento podem ver os detalhes somente para as organizações nas quais eles são designados à função de gerente de faturamento.
{: note}


## Visualizando permissões de uso
{: #view-usage-permissions}

Para recursos que são gerenciados pelo Cloud Foundry, a função de gerenciador de faturamento deve ser aplicada ao nível da organização. Para ver o uso do recurso do {{site.data.keyword.Bluemix}} Identity and Access Management (IAM), a função Visualizador deve ser aplicada ao grupo de recursos. Para obter mais informações sobre funções de permissão, consulte [Acesso do IAM](/docs/iam?topic=iam-userroles), [Acesso ao Cloud Foundry](/docs/iam?topic=iam-cfaccess) ou [Permissões de infraestrutura clássica](/docs/iam?topic=iam-infrapermission).

## Visualizando detalhes de uso de serviço
{: #services}

Na seção de serviços, é possível visualizar uma lista de seus serviços e os custos estimados que estão associados a esses serviços. Para visualizar um resumo dos encargos estimados para todas as instâncias de um recurso específico, conclua as etapas a seguir:

1. Acesse **Gerenciar > Faturamento e uso** e selecione **Uso**.
2. Clique em **Visualizar instâncias** para visualizar todas as instâncias de um tipo específico de recurso.  
3. Para ver um resumo detalhado dos encargos estimados para cada instância de um tipo de recurso específico, clique em **Visualizar detalhes da instância**. Também é possível ver as métricas de uso mensais detalhadas para a instância selecionada.

O proprietário da conta é cobrado pelo uso total que é incorrido entre todas as organizações no término de cada ciclo de faturamento. Cada ciclo de faturamento dura um mês.

Os proprietários da conta podem filtrar o resumo de uso por grupo e selecionar o prazo para uso. Os encargos mostrados representam a quantia que você, como o proprietário da conta, é cobrado naquele mês.

Se você selecionar uma organização específica na lista **Filtrar por grupo**, será possível ver o uso total para essa organização, incluindo qualquer uso como parte de uma camada grátis. O uso da camada grátis é mostrado como grátis no nível de conta, mas não no nível organizacional. Quando você visualiza o uso organizacional, você vê o uso real para essa organização, que inclui uso grátis e cobrado. Todo uso organizacional é acumulado para o uso da conta depois que a camada grátis é removida.

O gerente de contas de uma conta Pré-paga pode configurar as notificações de gastos com relação ao custo total da conta, para tempo de execução, serviços e para serviços individuais, exceto serviços de terceiros. Para obter mais informações, consulte [Configurando notificações de gastos](/docs/billing-usage?topic=billing-usage-spending).

## Exportando os detalhes de uso para um arquivo `.csv`
{: #export-csv}

É possível exportar um resumo de seu uso ou informações sobre seus serviços e instâncias, para um arquivo CSV. Ao exportar seu arquivo CSV, é possível localizar facilmente estimativas de informações de uso e custo de cada recurso para estornos a seus clientes ou para entender mais sobre seus custos.

1. Acesse **Gerenciar > Faturamento e uso** e selecione **Uso**.
1. Clique em **Exportar CSV** e selecione uma das opções:
   - Clique em **Resumo** para ter uma visão geral de alto nível do uso e dos custos associados da sua conta.
   - Clique em **Instância** para obter informações de uso detalhadas sobre cada instância de serviço.

   É possível usar a coluna **Tags** no arquivo CSV da instância para ajudar a analisar os recursos em sua conta. Por exemplo, você pode ter múltiplos projetos em uma conta, cada um com um cluster Kubernetes e algumas implementações de app do Cloud Foundry. É possível organizar os dados CSV de acordo com a tag de projeto em cada instância para que seja possível analisar melhor o custo dos projetos individuais. Para obter mais informações sobre a identificação, consulte [Trabalhando com tags](/docs/resources?topic=resources-tag).
   {: tip}
