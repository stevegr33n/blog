# Explore Azure Virtual Machines

Azure VMs let you create and use VMs in the cloud.

They provide IaaS in the form of a virtualised server and can be used in many ways.

Just like a physical computer, you can customize all the software running on the VM.

Choose a VM when you need:

- Control over the OS
- The ability to run custom software
- To use custom hosting configurations

An Azure VM gives you the flexibility of virtualisation without having to buy physical servers to run the VMs on. And Azure manages those servers for you.

BUT - you need to maintain the VM - that's why you chose to use a VM! You want control over the OS and with that you need to also maintain it.

This means you need to configure and update and maintain the software on your VM.

You can spin up a VM in minutes when you select a pre-configured VM image.

Choosing an image is of huge importance when creating a VM - an image is a template used to create a VM.

These templates include an OS and other software like dev tools and web hosting environments.

## Examples of when to use virtual machines

- During dev and test. VMs give a quick and easy way to create different OS configs and app configs. Dev and test personnel can easily delete VMs when they are no longer needed.

- When running apps in the cloud. Being able to run apps in the cloud as opposed to physical on-prem infrastructure can provide large economic benefits. This is due to the whole pay-as-you-go thing and scaling down infra when its no longer needed.

- Disaster recovery. If a primary datacenter fails you can create some VMs on Azure and host your critical apps on there until your primary datacenter is operational.

### Lift n Shift

VMs are also a good choice for lift-n-shift. This is where you take an image snapshot of your physical server and host that on an Azure VM with little to no changes needed.

### Scaling

You can group VMs together to provide high availability, scalability and redundancy.

Azure has VM scaling features:

- Availability Sets
- VM Scale Sets
- Azure Batch

#### What are availability sets

An availability set is a grouping of at least 2 VMs. This is so that your application is available during maintenance.

So if you use an availability set then you wont be in a situation where all your VMs are down for maintenance.

There's this concept of **update domains**, these indicate groups of VMs and the underlying hardware that can be rebooted at the same time.

Sometimes Microsoft needs to do maintenance on the Azure VM service. Improving performance, adding features, patching security vulns that kinda thing.

Or sometimes shit hits the fan, and a hardware failure hits the datacenter - like a power outage or disk failure. When this happens, VMs that are affected and part of an availability set switch over to a working physical server so that the VM continues to run.

There's a concept of **fault domain**, which is essentially a rack of servers. A group of VMs that share common hardware are also said to be in the same fault domain. Basically when shit gets fucked up they are all gonna eat it because they all use the same physical hardware.

So basically you want your VMs to be in different fault domains right, simple.

Well guess what, with an availability set you get up to 3 fault domains. Each fault domain has its own dediecated power and networking.

And you also get 5 update domains up to a max of 20.

The best thing about availablity sets - they are motherfucking free! You just pay for the VMs! Goddamn bargain.

#### What are virtual machine scale sets

VM Scale Sets let you create and manage a group of identical, load balanced VMs.

Lets say you're running a website that allows images to be uploaded and processed.

If we duplicate the VM we'd need to configure an additional service to route requests between multiple instances of the website - VM Scale Sets can do that for you.

Essentially a load balancer it seems.

Scale Sets allow you to centrally configure and update a large amount of VMs to make your apps highly available.

#### What is Azure Batch

It's large scale job scheduling and compute management with the ability to scale to 1000's of VMs.

When you want to run a job Batch does the following:

- Starts a pool of compute VMs
- Installs apps and staging data
- Runs jobs with as many tasks as you have
- Identifies failures
- Requeues work
- Scales down the pool when the work is finished

There may be times where you need raw compute power or supercomputer compute power - Azure provides these options.
