# Create a website hosted in Azure

## Whats an App Service

An Azure App Service is an HTTP-based service that enables you to build and host many types of web-based solutions without having to manage infrastructure.

You can host web apps, mobile back-ends, and RESTful APIs.

## Creating resources in Azure

First thing we gotta do is create a resource group to hold all the things we need to create. The resource group allows us to administer all the services, disks, network interfaces, and other elements the make up our solution as a unit.

We can use the Azure Portal to create and manage our solution's resource groups.

You can also use the Azure CLI, the CLI is useful to automate things in the future.

## Here's a guide on making a website hosted on an App Service

https://docs.microsoft.com/en-gb/learn/modules/welcome-to-azure/4-exercise-create-website

## What is scale?

The cloud is elastic, you can scale up and down temporarily. Either to deal with increased load or to save money. Azure Advisor and Azure Cost Management are two services that help you optimize cloud spenditure.

Scaling refers to adding network bandwidth, memory, storage, or compute power to achieve better performance.

**Vertical Scaling or Scaling Up** is adding more RAM, a better CPU (compute power), more storage, faster storage, on an existing VM. For example, adding more memory to a DB to make it run faster.

**Horizontal Scaling or Scaling Out** is adding extra VMs to power your app. For example, you might add a bunch of VMs configured in exactly the same way, and then use a load balancer to distribute work across them.

## What is Azure Cloud Shell?

Azure Cloud Shell is a browser based CLI for managing and developing Azure resources.

It can run either Bash or PowerShell, and both can access the Azure CLI.

For example, you can restart multiple App Services from the CLI instead of using the web interface to navigate to each App Service and restarting it from there - essentially it's much faster.

`az account list --output table`

`az group list --output table`

```
az resource list \
    --resource-group [sandbox resource group name] \
    --resource-type Microsoft.Web/sites
```

Here we are just returning the list of sites within our resource group, the json below contains our web app "MyWebApp"

```
{
  "id": "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx/resourceGroups/[sandbox resource group name]/providers/Microsoft.Web/sites/BlogFor",
  "identity": null,
  "kind": "app",
  "location": "centralus",
  "managedBy": null,
  "name": "MyWebApp",
  "plan": null,
  "properties": null,
  "resourceGroup": "[sandbox resource group name]",
  "sku": null,
  "tags": null,
  "type": "Microsoft.Web/sites"
}
```

Here we can stop and then start the web app by specifying the resource-group and name of the web app.

```
az webapp stop \
 --resource-group [sandbox resource group name] \
 --name <web app name>

```

```
az webapp start \
    --resource-group [sandbox resource group name] \
    --name <web app name>
```
