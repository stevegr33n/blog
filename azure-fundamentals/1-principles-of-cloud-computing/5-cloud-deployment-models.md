# Cloud deployment models

A cloud deplpoyment model defines where your data is stored and how your customers interact with it - how do they get to it, and where do the apps run?

There are 3 different cloud deployment models:

- Public
- Private
- Hybrid

## Public

This is the most common deployment model. All the servers are owned by the cloud provider. Everything runs on the cloud providers hardware. In some cases you can save costs by sharing computing resources with other cloud users.

Your data is secure and isolated, but the cloud provider decides where your data stored and when your apps run.

The main attraction to this model is cost. You scale based on what you need.

### Advantages

- High scalability - you don't have to buy a new server in order to scale
- Pay-as-you-go - you only pay for what you use, no CapEx costs
- Cloud provider takes care of maintenance on the hardware
- Minimum technical knowledge to set up and use, you leverage the cloud provider's skills and expertise

Example; deploying a blog on hardware resources owned by a cloud provider. Using a public cloud in this scenario allows cloud users to get their blog up and running quickly and not worry about maintaining the hardware on which is runs.

### Disadvantages

- You may need specific security requirements that public cloud cannot meet
- There may be government policies or industry standards or legal policies public cloud cannot meet
- You cant manage the hardware services as you may want to

## Private

In a private cloud the organisation creates a cloud environment in their own datacenter and provides self-service access to compute resources for the users of that organisation.

It's a simulation of public cloud to the users, but the organisation is completely responsible for the purchase and maintenance of the hardware and software services.

### Adantages

- You can ensure the configuration can support any scenario as you control the hardware
- You have control over security
- You can meet strict security, government policies, industry standards or legal policies

### Disadvantages

- Some CapEx costs to pay for the hardware and the setup/maintanence of said hardware
- Owning the hardware limits the scalability as you now need to purchase/install/setup the new hardware
- Requires technical expertise

Lloyds bank is a good example of an organisation that would use private cloud. They cannot put certain data in the public cloud due to legal reasons.

## Hybrid

Like the name suggests it's a mix of public and private clouds. This allows the organisation to run their apps in the most appropriate location. Your app doesn't have any security or legal requirements? Fuck it, put it in the public cloud why not.

Or you could host a website in the public cloud which connects to a highly confidential database storing medical records which is hosted in your private cloud.

### Adantages

- You can keep any systems running that require out-of-date hardware or an out-of-date OS
- Massive flexibility regarding where you run your apps
- Take advantage of economies of scale from public cloud providers for services and resources where it's cheaper - then switch to your own when it's not
- You can meet strict security, government policies, industry standards or legal policies because you can host the apps that require them on your private cloud

### Disadantages

- More complicated to manage
- More expensive than selecting one deployment model as it involves some CapEx costs
