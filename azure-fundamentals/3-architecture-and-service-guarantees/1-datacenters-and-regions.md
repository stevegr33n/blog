# Understand Datacenters and Regions

Microsoft has a ton of datacenters located around the globe right, this is like a massive local area network, like a mini internet.

When you use a service or spin up a resource like a VM or DB, you will be using physical equipment in one or more of these locations around the globe.

The specific datacenters are not exposed to the end users like us, instead we select a region.

## What is a region

A region is an area on the globe that contains at least one but usually multiple datacenters that are nearby and networked together with a low latency network.

Azure controls the resources within each region to balance the workloads.

When we deploy a resource we usually need to choose the region.

Azure has more regions than any other cloud provider. Why does this even matter? Well it means that you can bring your apps closer to users no matter if they are located in London or Timbuktu.

It also provides better scalability and redundancy.

## Special regions

There are some special regions that we might wanna use for compliance or legal reasons.

- US DoD
- China

The special US regions are for the US government and its partners.

Microsoft has a partnership with 21Vianet to provide China East and China North regions.
