---

copyright:
  years: 2017, 2022
lastupdated: "2022-02-28"

keywords: change service, upgrade service, service plan, pricing plan

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}
{:javascript: .ph data-hd-programlang='javascript'}

# Updating your pricing plan
{: #changing}

You can update the pricing plan of an {{site.data.keyword.Bluemix}} service if plan updates are enabled for that specific service. For example, you might want to upgrade or reduce your pricing plan. You can update the service's pricing plan from the service instance dashboard.
{: shortdesc}

Are you looking for details about upgrading your account type? See [Upgrading your account](/docs/account?topic=account-upgrading-account) for more information.
{: tip}

You can update the pricing plan only for certain services. If plan updates are enabled for the service, a **Plan** option is displayed on the service instance dashboard. Each service has a different set of steps to follow if you update your plan.

## Updating a plan in the console 
{: #changing-plan-ui}
{: ui}

1. From the {{site.data.keyword.Bluemix_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource List**, and select the service. 
1. Click **Plan** in the service instance dashboard. Select the pricing plan that you want, and click **Save**.

    Some services have pricing plans that are not selectable from the Plan page. Typically, these plans aren't selectable because they require assistance from the {{site.data.keyword.Bluemix_notm}} Sales team or they require a migration before you can update plans. See the documentation for the specific service for information about the required next steps.

Depending on the type of plan updates you make, your next steps can vary. For example, if you reduced the pricing plan, restart your app. Or, if you upgraded the pricing plan, you might need to restart your app, and then take other actions.
  
Complete the following steps to restart your app:

1. Click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource List**, and find the app that the service is bound to. 
1. From the app menu, select **Restart App**.

For more information about any further required actions, see the documentation for the specific service.

## Updating a plan by using the CLI
{: #changing_command_line}
{: cli}

Complete the following steps to update a pricing plan by using the {{site.data.keyword.Bluemix_notm}} command-line interface (CLI).

1. Check whether the service is enabled with the resource controller.

   ```bash
   ibmcloud catalog service <service_name>
   ```
   {: codeblock}

   The output lists `RC Compatible true`. Make a note of the ID of the plan that you want to update to.

   ```text
   RC Compatible      true
   RC Provisionable   true
   IAM Compatible     true
   Children   Name                      Kind         ID
              lite                      plan         4bcd3fgh-3cf2-47c0-93d4-d2f2289eac28
              standard                  plan         264d0450-996d-4bcd-894d-fc7018dacf1e
    ```

1. Update the pricing plan for your service instance.

   - If the service is enabled with the resource controller, run the [`ibmcloud resource service-instance-update` command](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_service_instance_update).

     ```bash
     ibmcloud resource service-instance-update <service_instance_name> --service-plan-id <plan_id>
     ```
     {: codeblock}

   - If the service is based on Cloud Foundry, run the [`ibmcloud cf update-service` command](/docs/cli?topic=cli-ibmcloud_commands_services#ibmcloud_service_update).

     ```bash
     ibmcloud cf update-service <service_instance_name> [-p <plan_name>]
     ```
     {: codeblock}

## Updating a pricing plan by using the API
{: #changing-plan-api}
{: api}

You can programmatically update the pricing plan for an instance by calling the [{{site.data.keyword.cloud_notm}} Resource Controller API](/apidocs/resource-controller/resource-controller#update-resource-instance) as shown in the following sample request. The example updates a pricing plan for an instance. 

```curl
curl -X PATCH https://resource-controller.cloud.ibm.com/v2/resource_instances/8d7af921-b136-4078-9666-081bd8470d94 -H 'Authorization: Bearer <>' -H 'Content-Type: application/json' -d '{
    "name": "my-instance-new-binding-1",
    "resource_plan_id": "744bfc56-d12c-4866-88d5-dac9139e0e5d"
  }'
```
{: codeblock}
{: curl}

```java
Map<String, Object> parameters = new HashMap<String, Object>();
parameters.put("exampleProperty", "exampleValue");

UpdateResourceInstanceOptions updateResourceInstanceOptions = new UpdateResourceInstanceOptions.Builder()
  .id(instanceGuid)
  .name(resourceInstanceUpdateName)
  .parameters(parameters)
  .build();

Response<ResourceInstance> response = service.updateResourceInstance(updateResourceInstanceOptions).execute();
ResourceInstance resourceInstance = response.getResult();

System.out.printf("updateResourceInstance() response:\n%s\n", resourceInstance.toString());
```
{: codeblock}
{: java}

```
getAccountUsage(params)
```
{: codeblock}
{: javascript}

```python
parameters = {
    'exampleProperty': 'exampleValue'
}
resource_instance = resource_controller_service.update_resource_instance(
    id=instance_guid,
    name=resource_instance_update_name,
    parameters=parameters
).get_result()

print('\nupdate_resource_instance() response:\n',
      json.dumps(resource_instance, indent=2))
```
{: codeblock}
{: python}

```go
parameters := map[string]interface{}{"exampleProperty": "exampleValue"}
updateResourceInstanceOptions := resourceControllerService.NewUpdateResourceInstanceOptions(
  instanceGUID,
)
updateResourceInstanceOptions = updateResourceInstanceOptions.SetName(resourceInstanceUpdateName)
updateResourceInstanceOptions = updateResourceInstanceOptions.SetParameters(parameters)

resourceInstance, response, err := resourceControllerService.UpdateResourceInstance(updateResourceInstanceOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(resourceInstance, "", "  ")
fmt.Printf("\nUpdateResourceInstance() response:\n%s\n", string(b))
```
{: codeblock}
{: go}



