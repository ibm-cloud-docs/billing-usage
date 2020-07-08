---

copyright:
  years: 2017, 2020
lastupdated: "2020-06-03"

keywords: change service, upgrade service, service plan, pricing plan

subcollection: account

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}


# Updating your pricing plan
{: #changing}

You can change the pricing plan of an {{site.data.keyword.Bluemix}} service if plan changes are enabled for the specific service. You might want to change the plan, for example, to upgrade or reduce your plan. You can change the service's pricing plan from the service instance dashboard.
{: shortdesc}

Are you looking for details about upgrading your account type? See [Upgrading your account](/docs/account?topic=account-upgrading-account) for more information.
{: tip}

You can change the service plans for only certain services. If plan changes are enabled for the service, the service instance dashboard displays a **Plan** option in the navigation. Each service has a different set of next steps to follow if you change your plan.

1. From the {{site.data.keyword.Bluemix_notm}} console, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) > **My resources** to view your list of resources. Click the service that you want to update.
1. Click **Plan** in the service instance dashboard. Select the plan that you want to change to, and click **Save**.

    Some services have plans that are not selectable from the Plan page. Typically, these plans aren't selectable because they require assistance from the Sales team or they require a migration before you can change plans. See the documentation for the service for information about required next steps.

1. After you change your plan, you must complete extra steps. The steps vary depending on the type of plan change and the service. For example, if you reduced your plan, you might need to restage your app. Or, if you upgraded your plan, you might need to restage your app and take other actions.

   To restage your app, go to the My resources page to find the app that the service is bound to. Click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) **> My resources**. In the app menu, select **Restart App**.

  For more information about any further required actions, see the documentation for the service.

## Changing a plan by using the CLI
{: #changing_command_line}

As an alternative to the console, you can change a service's pricing plan by using the {{site.data.keyword.Bluemix_notm}} command-line interface (CLI).

1. Check whether the service is enabled with the resource controller.

   ```
   ibmcloud catalog service <service_name>
   ```
   {:codeblock}

   If the service is enabled with the resource controller (RC), it lists `RC Compatible true`. Make note of the ID of the plan that you want to change to.

   ```
   RC Compatible      true
   RC Provisionable   true
   IAM Compatible     true
   Children   Name                      Kind         ID
              lite                      plan         4bcd3fgh-3cf2-47c0-93d4-d2f2289eac28
              standard                  plan         264d0450-996d-4bcd-894d-fc7018dacf1e
    ```

1. Change the plan for your service instance.

   - If the service is RC-enabled, change your plan by using the [`ibmcloud resource service-instance-update` command](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_service_instance_update).

     ```
     ibmcloud resource service-instance-update <service_instance_name> --service-plan-id <plan_id>
     ```
     {: codeblock}

   - If the service is not RC-enabled and is therefore based on Cloud Foundry, change your plan by using the [`ibmcloud cf update-service` command](/docs/cli?topic=cli-ibmcloud_commands_services#ibmcloud_service_update).

     ```
     ibmcloud cf update-service <service_instance_name> [-p <plan_name>]
     ```
     {:codeblock}
