# Reduce latency with Azure Traffic Manager

We still gotta solve our problems of latency, and resiliency across geographic locations

How do we make our vitamins website which is located in the US, load fast for people in the EU or Asia?

## Whats network latency

Latency refers to the time it takes for data to travel over a network - it's typically mesaured in milliseconds (ms)

Latency refers to the time it takes for data to reach its destination.

Bandwidth refers to the amount of data that can fit on the connection.

Factors like the type of connection you use, and how the app is designed can affect latency - but the biggest factor is distance.

The further away a user is from the location of your website, the longer the latency is for them.

You gotta send them all the HTML, CSS, JS, and images and whatnot, and that further they are from your site the longer thats gonna take

## Scale out to different regions

One way to reduce latency is to have copies of your service in more than one region. Like this:

![](./global-deployment.png)

Notice the DNS name for each site. We want to connect to the closest service under the contoso name, but how?

## Traffic Manager

One way is to use Azure Traffic Manager.

Traffic Manager uses the DNS server closest to the user to direct user traffic to a globally distributed endpoint.

Traffic Manager doesnt see the traffic thats passed between the server and the client, it just directs the client's web browser to a preferred endpoint.

Traffic Manager can route traffic in a few ways, one being - route traffic to the endpoint with the lowest latency

## Load balancer vs Traffic Manager

Azure Load Balancer distributes traffic within the same region to make your services more highly available and resilient.

Traffic Manager works at the DNS level, and directs the client to a preferred endpoint. This preferred endpoint can be the region closest to your user.

When Traffic Manager finds an unresponsive endpoint it directs traffic to the next closest endpoint.

When Load Balancer detects an unresponsive VM it directs traffic to other VMs in the pool.

So they work in slightly different ways.
