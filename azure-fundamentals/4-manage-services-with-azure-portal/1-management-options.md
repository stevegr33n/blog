# Azure management options

We can use a variety of tools to configure and manage Azure.

- Azure portal - the Azure website
- Azure PowerShell & Azure CLI - CLI for Azure
- Cloud Shell - web based CLI
- Mobile app - lol monitoring and managing resources from yo phone bruh

## Portal

Its a public website accessible with a browser. You can browse services and deploy manage and delete resources.

## Azure PowerShell

This is a module that we can install for PowerShell. Azure PowerShell allows us to connect to our Azure subscription and manage resources.

For example you can run `New-AzVM` in Azure PowerShell and create a VM in your Azure subscription.

To do this, run PowerShell, install the Azure PowerShell module, sign in to Azure using `Connect-AzAccount` abd then issue the command

```
New-AzVM `
    -ResourceGroupName "MyResourceGroup" `
    -Name "TestVm" `
    -Image "UbuntuLTS" `
```

## Azure CLI

This is cross platform for all major OS's. Here's how to create a VM:

```
az vm create \
  --resource-group MyResourceGroup \
  --name TestVm \
  --image UbuntuLTS \
  --generate-ssh-keys \
```

## Azure Cloud Shell

It's a web based, authenticated shell that has the same functionality as the Azure CLI and Azure PowerShell.

It'll prompt you to create an Azure Storage Account when you first use it to store data which allows it to be a persistent shell and store any scripts.

## Mobile App lol

You can install the iOS app if you want, itkk allow you to restart VMs or Apps and check the health of your services among a bunch of other things as well as use the Azure Cloud Shell.
