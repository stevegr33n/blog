# Scale with Azure Load Balancer

Using our vitamins business from before, we moved it from on-prem to Azure cloud - but how do we ensure it's running 24/7?

## Yo what's availability and what's high availability

Availability - how long is your service running without interruption.

High availability - your service is running for a long ass time.

Five 9's availability = 99.999% uptime

Five 9's is what a lot of teams strive for.

## Yo what's resiliency

Resiliency refers to a systems ability to stay operational during cray conditions.

Cray conditions are things like the datacenter blew up, or systems went down for maintenance, spikes in traffico or DDoS attacks.

## Yo what's a load balancer

A load mother fucking balancer distributes traffic evenly among each system in a pool.

A load balancer is real helpful in helping us achieve resiliency and high availability.

In our vitamins example we added some VMs to a virtual network for each tier of our system. The idea is to have additional systems ready incase one goes down, or if it is serving too many users at the same time.

The problem here is that each VM would have its own IP address. And you dont have a way to distribute traffic in case one system goes down or is busy. The question is - how do we connect our VMs so that they appear to the user as one system?

Enter Load Balancer.

The load balancer becomes the entry point for the user, and the load balancer distributes the traffic among the VMs.

The user doesn't know or care which VM the load balancer chooses to receive the request.

![](./load-balancer.png)

The load balancer receives the users request and directs this request to one of the VMs on the web tier.

If a VM goes down or stops responding, the load balancer stops sending traffic to it. Then the load balancer directs traffic to the responsive VMs.

Load balancing allows us to run maintenance tasks without interrupting the service, giving us higher availability. In this case, just perform maintenance on each VM one after the other.

We can also have a load balancer for other parts of the system, not just the web interface tier but for the application logic tier too.

## What is Azure Load Balancer

It's a load balancer service that has the maintenance taken care of for us by Microsoft.

It supports inbound/outbound scenarios. It has low latency and high throughput. It scales up to millons of flows for all Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) apps.

The downside of running your own load balancer is that you've added another system you need to maintain. If your load balancer goes down or needs maintenance - you're back to your original problem.

But with Azure, they do the maintenance, and you don't have to maintain the software. It's SaaS. You just define the forwarding rules based on the source IP/port to a set of destination IP/ports.

![](./azure-load-balancer.png)

---

## Azure Application Gateway

If all your traffic is HTTP, a better option is to use Azure Application Gateway.

This is a load balancer designed for web apps.

It uses Azure Load Balancer at the transport level (TCP) and applies URL-based routing rules to support multiple scenarios.

![](./appgateway.png)

This type of routing is called application layer load balancing because it understands the structure of the HTTP message.

Here's some benefits of using Azure Application Gateway instead of a regular load balancer:

- Cookie affinity - useful when you want to keep a user session on the same backend server
- SSL termination - Appilication Gateway can manage your SSL certificates and pass unencrypted traffic to the backend servers to avoid encryption/decryption overhead. And it also supports full end-to-end encryption for apps that require it.
- Web app firewall - Application Gateway supports a sophisticated firewall (WAF) with detailed monitoring and logging
- URL rule-based routes - Application Gateway allows you to route traffic based on URL patterns - source IP/port to destionation IP/port. This is helpful when setting up a content delivery network (CDN)
- Rewrite HTTP headers - You can add or remove info from the inbound/outbound HTTP headers of each request to scrub sensitive info like server names

## Whats a CDN

A CDN is a distributed network of servers that can efficiently deliver web content to users. It's a way to get content to users in their local region to minimize latency. CDNs can be hosted in Azure. You can cache content at strategically placed physical nodes across the globe and provide better performance to users. They are useful for web apps that contain multimedia content, or an event in a particular region, or really any event where you expect a high-bandwidth requirement in a region.
