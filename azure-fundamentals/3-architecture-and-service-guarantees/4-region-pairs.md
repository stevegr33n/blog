# Understand Region Pairs in Azure

Availability Zones are created using one or more datacenters, and there are minimum of 3 zones within a single region.

However, it is possible a massive tornado comes along and wipes out multiple datacenters or even an entire Availability Zone.

To combat this Azure has a trick up its sleeve - Region Pairs.

## What's a region pair

As the name suggests, each region is paired with another region inside the same geography - **at least 300 miles away.**

This allows for the replication of resources across a geography whilst avoiding natural disasters, civil unrest, power outages or network outages affecting both regions at once.

Obviously both regions in a region pair _could_ be affected at once, but it's less likely.

Example region pair - West US & East US

---

Some services offer automatic geo-redundant storage using region pairs. This means your data will be copied to another storage in the other region pair of the geography you've chosen.

Other benefits of region pairs are:

- If Azure is down for a long time they will prioritise restoring one region out of every pair
- Planned Azure updates are rolled out to region pairs one region at a time, to minimize downtime
- Data continues to exist in the same geography for tax and other purposes
