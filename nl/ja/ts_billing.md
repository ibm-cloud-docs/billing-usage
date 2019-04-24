---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-09"

keywords: troubleshoot billing, billing error, payment error, error message

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


# 請求および使用量の管理に関するトラブルシューティング
{: #troubleshoot}

請求および使用量の管理の一般的な問題には、請求処理情報にアクセスするために必要な権限が含まれる場合があります。 多くの場合、いくつかの簡単なステップに従うことで、この問題から復旧できます。
{:shortdesc}


## 請求処理情報にアクセスできないのはなぜですか?
{: #cannot-access-billing-info}
{: troubleshoot}

支払いや送り状などの請求処理情報にアクセスしようとすると、機能が使用できないことを示すメッセージが表示されます。
{: tsSymptoms}

このメッセージを受け取る理由は、ユーザーがアカウントの請求処理情報を表示する権限を持っていないためです。 アカウント所有者か Cloud Foundry 組織請求マネージャーであるか、または管理者役割が割り当てられているすべてのアカウント管理サービスで IAM ポリシーを持っている必要があります。
{: tsCauses}

アカウント所有者であれば、そのアカウントの請求処理情報を表示できます。 請求管理者は、Cloud Foundry 組織の請求処理情報を表示できます。 また、IAM 対応リソースの場合は、管理者役割が割り当てられているすべてのアカウント管理サービスに対して IAM ポリシーが必要です。

以下のステップを実行してアクセス権限を確認します。

  1. **「管理」 > 「アクセス (IAM)」**に移動して、**「ユーザー」**を選択します。
  2. 「ユーザー」ページから自分の名前をクリックします。
  3. **「アクセス・ポリシー」**をクリックして、割り当てられている IAM アクセス・ポリシーを表示します。
  4. **「Cloud Foundry アクセス権限」**をクリックし、割り当てられた組織の行を展開して、アカウント所有者または請求管理者の役割を持っているかどうかを確認します。

IAM アクセス権限について詳しくは、[Cloud IAM 役割](/docs/iam?topic=iam-userroles)を参照してください。 Cloud Foundry アクセス権限について詳しくは、[Cloud Foundry の役割](/docs/iam?topic=iam-cfaccess)を参照してください。
{: tsResolve}
