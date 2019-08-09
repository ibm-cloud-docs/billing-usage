---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise usage, view enterprise costs, account group usage, account usage, cost recovery, chargeback, support cost

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:external: target="_blank" .external}
{:note: .note}


# Visualizando o uso em uma empresa
{: #enterprise-usage}

É possível rastrear custos de recursos e suporte por meio de contas em sua empresa {{site.data.keyword.Bluemix}} visualizando seu uso. As contas e os grupos de contas cujo uso pode ser visualizado dependem de seu acesso designado.
{: shortdesc}

As empresas do {{site.data.keyword.Bluemix_notm}} permitem gerenciar centralmente múltiplas contas do {{site.data.keyword.Bluemix_notm}}. Como um usuário corporativo, é possível ficar de olho no uso do recurso e nos custos associados para qualquer conta na empresa. Consulte [O que é uma empresa?](/docs/account?topic=account-enterprise) para obter mais informações.

## Acesso necessário para visualizar o uso corporativo
{: #enterprise-usage-access}

Em uma empresa, o acesso às informações de uso é controlado pelo Serviço corporativo. Para visualizar informações de uso, os usuários devem ser convidados para a conta corporativa e ter a função de Visualizador de relatórios de uso, de Editor ou de Administrador no Serviço corporativo. A função Visualizador de relatórios de uso fornece acesso apenas para visualizar relatórios de uso, enquanto as funções de Editor e de Administrador ativam ações de gerenciamento corporativo adicionais. Em conformidade com as boas práticas de segurança, designe a menor quantidade de acesso necessário para que o usuário conclua sua tarefa. Para obter mais informações, consulte [Ações e funções corporativas](/docs/iam?topic=iam-account-services#enterprise-account-management).

É possível fornecer aos usuários acesso granular para que eles possam visualizar o uso para uma determinada conta ou grupo de contas. Por exemplo, digamos que sua empresa tenha grupos de contas para cada departamento e cada departamento tenha grupos de contas para cada equipe. É possível definir o escopo do acesso para que cada usuário corporativo possa ver apenas as informações que são necessárias para cumprir as tarefas relacionadas ao cargo dele.
   * Seu executivo financeiro precisa visualizar o uso para a empresa inteira para que ele possa rastrear e recuperar custos para cada departamento, mas não precisa criar contas ou grupos de contas. Designe a eles a função de Visualizador de relatórios de uso para a empresa.
   * Cada líder de departamento precisa visualizar o uso para seu departamento e ele também precisa criar e gerenciar contas e grupos de contas para suas equipes. Designe a cada líder de departamento a função de Editor para o grupo de contas de seu departamento.
   * Cada líder de equipe precisa visualizar o uso de sua equipe, mas você deseja que ele obtenha aprovação do departamento para incluir novas contas em sua equipe. Designe a cada líder de equipe a função de Visualizador de relatórios de uso para o grupo de contas de sua equipe. Ele pode visualizar o uso de todas as contas dentro do grupo de contas, mas não o uso dos grupos de contas de outras equipes no departamento.

Para obter as etapas detalhadas sobre como designar o acesso corporativo, consulte [Designando acesso corporativo](/docs/iam?topic=iam-assign-access-enterprise).

## Visualizando o uso corporativo
{: #enterprise-usage-console}

1. Efetue login na conta corporativa.
1. Acesse **Gerenciar > Faturamento e uso** e selecione **Uso**.

   A página Uso exibe os custos para todos os usos de recursos em sua empresa, divididos por conta e grupo de contas. Também é possível visualizar o uso de crédito de suporte para toda a empresa e qualquer excedente que tenha sido incorrido.

   As informações de uso para serviços de infraestrutura clássica não são incluídas para o período de faturamento atual. No entanto, elas são incluídas para períodos de faturamento anteriores, que é possível visualizar selecionando um mês anterior no menu **Prazo**. Para obter mais informações, consulte [Visualizando o uso de seus recursos de infraestrutura clássica](/docs/billing-usage?topic=billing-usage-infra-usage).
1. Para visualizar o uso dentro de um grupo de contas, clique no nome do grupo de contas na tabela ou no menu **Nível corporativo**. Semelhante ao nível corporativo, o uso é dividido pela conta e pelo grupo de contas.

   Se um grupo de contas não contiver nenhuma conta, ele não será exibido na página Uso.

1. Para visualizar o uso por recurso, acesse o nível de conta clicando em grupos de contas na tabela ou selecionando a conta no menu **Nível corporativo**. Os custos para cada tipo de recurso que foi usado durante o prazo são exibidos.

   Na conta corporativa, não é possível visualizar dados de uso para o plano de recursos ou para a instância porque isso requer acesso dentro da conta. Se você for um usuário na conta, alterne para a conta a fim de visualizar esses dados. Você precisa de acesso de faturamento para os recursos e serviços na conta, conforme descrito em [Visualizando seu uso](/docs/billing-usage?topic=billing-usage-viewingusage).

Apenas os dados para uso que são incorridos pelas contas na empresa são exibidos na conta corporativa. Para visualizar o uso de antes de uma conta ter sido incluída na empresa, efetue login nessa conta e selecione o prazo relevante.
{: note}

### Visualizando o uso corporativo usando a CLI
{: #enterprise-usage-cli}

É possível obter um relatório de uso para a empresa, um grupo de contas ou uma conta específica.

1. Efetue login e selecione a conta corporativa.

   ```
   ibmcloud login
   ```
   {:codeblock}

1. Se você desejar visualizar o uso de uma conta ou grupo de contas específico, localize o nome ou o ID executando o comando **`ibmcloud enterprise`**.

   Por exemplo, o comando a seguir exibe todos os grupos de contas em uma empresa.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}

1. Visualize o uso executando o comando **`ibmcloud billing`**, conforme mostrado nos exemplos a seguir.

   * Visualize o uso do mês atual da empresa inteira.

      ```
      ibmcloud billing enterprise-usage
      ```
      {: codeblock}

   * Visualize o uso do grupo de contas de `Development` de julho de 2019.

      ```
      ibmcloud billing enterprise-usage --account-group Development --month 2019-07
      ```
      {:codeblock}

   * Visualize o uso dos grupos de contas e contas que estão diretamente sob a empresa.

      ```
      ibmcloud billing enterprise-usage --children
      ```
      {:codeblock}

   Por padrão, os comandos exibem o relatório de uso para o mês atual no formato a seguir. A maioria dos custos são listados como custos faturáveis. Os custos não faturáveis são listados apenas em casos muito raros, como para o mês em que você inclui uma conta para teste na empresa.

   ```
   Name             Type            Billable Cost   Non-billable Cost   Currency   Month
Example Corp     account         123.45          0                   USD        2019-07
Development      account_group   234.56          0                   USD        2019-07
Marketing        account_group   345.67          0                   USD        2019-07
Sales            account_group   456.78          0                   USD        2019-07
   ```

   É possível gerar saída do relatório no formato JSON especificando a opção `--output JSON`.
   {: tip}

### Visualizando o uso corporativo usando a API
{: #enterprise-usage-api}

É possível obter relatórios de uso de uma empresa e suas contas chamando a <!-- [Enterprise Usage Reports API (Beta)](https://{DomainName}/apidocs/enterprise-apis/resource-usage-reports){: external} -->API de relatórios de uso corporativo (Beta). É possível basear a consulta em sua chamada de API em uma empresa, em um grupo de contas ou em uma conta e especificar se deve visualizar a entidade ou seus filhos. A API de Relatórios de uso corporativo é uma liberação beta.

Os exemplos a seguir mostram consultas que podem ser usadas para obter relatórios de uso diferentes. Quando você chamar a API, substitua as variáveis de ID e o token do IAM pelos valores de sua empresa.

Visualize o uso do mês atual da empresa inteira.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

Visualize o uso de um grupo de contas para julho de 2019.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?account_group_id=$ACCOUNT_GROUP_ID&month=2019-07" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

Visualize o uso para grupos de contas e contas diretamente sob a empresa.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID&children=true" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}


## Recuperando custos para uso corporativo
{: #enterprise-cost-recovery}

Uma empresa consolida o faturamento de todas as suas contas e grupos de contas para uma única fatura, o que simplifica o gerenciamento de faturamento. É possível recuperar os custos do uso de recursos na empresa, cobrando os custos de uso de cada grupo de contas ou conta para o departamento ou equipe associada.

Para visualizar a hierarquia corporativa e qualquer uso, você precisa de uma política de acesso com a função de Editor ou de Administrador no Serviço corporativo para a empresa inteira. As etapas a seguir usam o console do {{site.data.keyword.Bluemix_notm}} como um exemplo, mas também é possível executar essas etapas usando a CLI ou a API.

1. Localize os custos de uso para cada departamento, acessando **Gerenciar > Uso** na conta corporativa. No menu **Prazo**, selecione o mês anterior para visualizar o uso que está incluído na fatura mais recente.

  Os custos para os grupos de contas são listados na tabela. Esses custos incluem todos os encargos, exceto qualquer imposto cobrado em sua região de faturamento. Se você desejar um detalhamento adicional de custos de uso, clique no nome do grupo de contas para visualizar as contas e os grupos de contas que ele contém.

1. Identifique os departamentos dentro de sua empresa que correspondem aos grupos de contas.

   Se os contatos designados aos seus grupos de contas estiverem associados ao departamento do qual você deseja recuperar custos, a descoberta do contato será uma maneira de localizar essas informações. Acesse **Gerenciar > Empresa** e selecione **Contas**. O contato para cada grupo de contas é listado na tabela.

   No entanto, as práticas de faturamento variam por empresa. Por exemplo, o contato do grupo de contas pode ser um ponto focal técnico que não está associado ao departamento que você deseja cobrar. Sempre verifique o departamento correto de acordo com os processos contábeis de sua empresa.

   Se a sua empresa usar códigos de faturamento para estornar custos aos departamentos, inclua o código de faturamento no nome do grupo de contas para identificar facilmente o código. Por exemplo, `Sales - A2B3`.
   {: tip}

1. Emparelhe os custos de uso para cada grupo de contas com o departamento identificado e siga os processos de sua empresa para enviar os encargos.
