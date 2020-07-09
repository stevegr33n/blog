# Improve your app reliability in Azure

Once you've created some Service Level Agreements (SLAs) you can set performance targets for your app. And you can use SLAs to evaluate how your business requirements meet your user's needs.

This is called an _Application SLA_

# App requirements

You gotta know your workload requirements to be able to build a viable solution for your app. Like does my app need a DB? How many users will it have? What are the legal requirements (if any)? etc

Once you know your workload requirements you can then choose which products and services to use, and then begin to provision resources according to those requirements.

You need to understand the SLAs that define your performance targets for your chosen products and services.

Understanding the SLAs will then let you create achievable Application SLAs.

Stuff's gonna break, basically. Site reliability am I right? Hardware will fail, and networks will go down - you gotta plan for this bruh.

Application availablility is the overall time a system is functional and working.

# Resiliency

Resiliency aint about avoiding failure, it's about responding to them in ways that avoids or minimizes downtime or data loss.

How quick can you get up once you get knocked down essentially.

**High Availability** and **Disaster Recovery** are 2 super important components of a resilient system.

So with these two things in mind, you should consider how to achieve them.

The way to do that is by having an FMA - Failure Mode Analysis.

Identify each and every possible point of failure, and make a plan for how your app is going to get through those failures.

## Cost and complexity vs high availability

Availability means your system or your app is 1 - available and 2 - working.

You wanna maximize availability. If your app is down then that's awful for you and your business.

So you gotta make sure thats as little as possible - like with the example earlier by having your app write to a queue for when the database goes down.

But as we mentioned earlier not only does this increase complexity, it also increases costs.

This increase in complexity may also increase possible failure points too.

Obviously if your workload requires 99.99% uptime you can't depend on a service that has 99.9% uptime.

Btw, 99.999% = 5mins downtime per year. AKA: 5 9's = 5mins

So if you need 99.999% uptime, you can't manually start fixing things - you simply won't have time.

Your solution must be self-diagnosing and self-healing. It's gotta be both the TF2 Heavy and the TF2 medic.
