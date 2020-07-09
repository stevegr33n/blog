# Understand Azure billing

## Azure subscription

Remember bro, you only pay for what you use on Azure - pay-as-you go bro.

When you sign up an Azure subscription is created by default. An Azure subscription is a logical container used to provision resources in Azure.

This container holds the details of all your resources like VMs DBs etc

When you create a VM, you identify the subscription it belongs to. As and when you use the VM the usage of the VM is aggregated and billed monthly.

## Additional Azure Subscriptions

You may wanna crate additional subscriptions to better manage your billing of resources.

So you could have a subscription purely for Environments, and another purely for Organisation structures.

- Environment level
  Resource access control occurs at the subscription level. So you may want to set up different subsciptions for different environments; example one subscription for dev, one for test, one for security, or one just to isolate data for compliance reasons.

- Organisation level
  You could create subscriptions to reflect your organisation's structure. For example, one subscription could limit one department to a lower cost resource, while the IT department has a subscription with full access. This allows you to manage and control access to the resources within each subscription.

- Billing level
  You may want to also have additional subscriptions purely for billing purposes. Because costs are first aggregated at the subscription level, you might want to create subscriptions to manage and track costs. For example, a subscription for prod workloads, and another for dev and test workloads.

Subscriptions are also bound by some hard limitations. For example the max amount of Express Route circuits in a subscription is 10. If you need to go over this limit, then you'll need additional subscriptions.

Basically once your organisation is a certain size, it doesn't make sense to have a single subscription.

---

Once you have multiple subscriptions you can organise them into invoice sections.

Each section is an item on the invoice that shows the charges incurred that month.

For example, you might need a single invoice for your organisation, but you want to organisat charges by department, or team, or project.

You can setup multiple invoices in your billing account.

In order to do this you must setup bulling profiles, and each profile has its own invoice and payment method.

![](./billing-structure-overview.png)
