---



copyright:

  years: 2017, 2018, 2019
lastupdated: "2019-01-09"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# Resolução de problemas para gerenciar faturamento e uso
{: #troubleshoot}

Problemas gerais ao gerenciar seu faturamento e uso podem incluir a autoridade necessária para acessar suas informações de faturamento. Em muitos casos, é possível recuperar-se do problema seguindo algumas etapas simples.
{:shortdesc}


## Por que não consigo acessar as informações de faturamento?
{: #cannot-access-billing-info}
{: troubleshoot}

Ao tentar acessar suas informações de faturamento, como pagamentos e faturas, você recebe uma mensagem dizendo que a função não está disponível.
{: tsSymptoms}

Você receberá essa mensagem porque não tem autorização para visualizar as informações de faturamento da conta. Deve-se ser proprietário de uma conta, gerente de faturamento de organização do Cloud Foundry ou ter uma política do IAM em todos os serviços de gerenciamento de conta com a função de administrador designada.
{: tsCauses}

É possível visualizar informações de faturamento em qualquer conta da qual você seja um proprietário. Um gerenciador de faturamento é capaz de visualizar informações de faturamento de uma organização do Cloud Foundry. E, para recursos ativados pelo IAM, deve-se ter uma política do IAM em todos os serviços de gerenciamento de conta com a função de Administrador designada.

Verifique seu acesso concluindo as etapas a seguir:

  1. Acesse **Gerenciar > Acesso (IAM)** e selecione **Usuários**.
  2. Clique em seu nome na página Usuários.
  3. Clique em **Políticas de acesso** para visualizar suas políticas de acesso do IAM designadas.
  4. Clique em **Acesso do Cloud Foundry** e expanda as linhas para suas organizações designadas para ver se você tem uma função de proprietário da Conta ou de gerente de faturamento.

Para obter mais informações sobre o acesso ao IAM, consulte [Funções do IAM da nuvem](/docs/iam?topic=iam-userroles). E, para obter mais informações sobre o acesso do Cloud Foundry, consulte [Funções do Cloud Foundry](/docs/iam?topic=iam-cfaccess).
{: tsResolve}
