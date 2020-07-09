# Essential Azure compute concepts

## What is Azure compute

It's a computing service for running cloud apps.

It provides resources like multi-core processors and supercomputers via VMs and containers.

It also has serverless computing to run apps - servless lets you skip setting up infrastructure.

The reosources are available on demand and can be created in minutes/seconds.

Once again, it's pay-as-you-go

There's 4 common compute options:

- VMs
- Containers
- App Service
- Serverless

## What are virtual machines

VMs are emulations of actual physical computers. So they have virtual CPUs instead of a physical ones. Virtual RAM instead of physical RAM. Virtual SDDs or HDDs instead of physical ones. You get the point.

Then you can use a remote desktop client to control the VM like it were a physical one.

## What are containers

Containers are a virtualisation environment for running apps.

Just like VMs containers run ontop of a host OS. But unlike VMs, containers dont include an OS for the apps that run inside the container. Instead they just use the host OS.

For example, if 5 containers are running on a Linux server with some version of the Linux kernel; all 5 containers - and subsequently the apps on those containers - share that same Linux kernel.

## What is Azure App Service

Azure App Service is a PaaS that allows you to host web apps. You get good performance and security, as well as scalability. It's all managed for you as it's a PaaS.

## What is Serverless Computing

Serverless is basically writing an app or function, and then just giving it to a execution environment. It's basically a service that Azure provides, you create an instance of that service and add your code, job done. No faff needed in regards to configuring infrastructure, you just point your consumer at that serverless service, it computes the code and returns a result.

Both serverless PaaS architectures keep the entire backend invisible to developers, they are somewhat similar. The differences are in scalability, pricing, startup time, tooling, and the ability to deploy at the network edge.

## Which computing strategy is right for me

You don't need to choose, this isn't like picking a hero in DotA. You can use each compute service in tandem with one another if you'd like. They all have benefits and trade offs.

For example, severless expects the work to be finished quickly - usually within seconds. So you might want to run your core app on a VM or container, but offload some of the data processing to a serverless app.
