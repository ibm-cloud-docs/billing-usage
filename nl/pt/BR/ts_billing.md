---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-11"

keywords: troubleshoot billing, billing error, payment error, error message, feature code, subscription code

subcollection: billing-usage

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


## Por que não posso aplicar um código de recurso?
{: #cannot-apply-feature-code}
{: troubleshoot}

Quando você tenta aplicar um código de recurso, você vê um erro que indica que o código não pode ser aplicado.
{: tsSymptoms}

Sua conta não atende aos requisitos do código de recurso ou você não possui o nível de acesso necessário na conta.
{: tsCauses}

- Verifique se você tem o tipo de conta correto. Por exemplo, alguns códigos de recurso para promoções educacionais são somente para contas Lite. Para visualizar seu tipo de conta, acesse **Gerenciar > Conta** e selecione **Configurações da conta**. Para obter detalhes, consulte [Aplicando códigos de recurso](/docs/account?topic=account-codes).
- Verifique se você tem acesso para aplicar o código de recurso. Para aplicar qualquer código de recurso, deve-se ter uma função Editor ou superior em todos os serviços de gerenciamento de conta. Para revisar ou mudar funções, consulte [Designando acesso a serviços de gerenciamento de conta](/docs/iam?topic=iam-account-services).
{: tsResolve}
