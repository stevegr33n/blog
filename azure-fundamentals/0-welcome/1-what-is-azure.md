# What is Azure?

Azure is a private and public cloud platform.

It allows you to build, deploy and manage apps.

It's pay as you go pricing wise.

You rent infrastructure from Azure.

The business value in this is helping your teams deliver features faster, and your end users have a better experience with your products and services.

## Cloud Power

Things are moving at a neck-breaking pace tech wise. Cloud is a huge player in this space, speech recognition and AI services are powered by the cloud.

Analytics and machine learning on those analytics allowing you to make sense of that information is powered by the cloud.

Azure has over 100 hundred cloud services. #Let that sink in. #Think about that. lol

## Hows it work dude

Azure makes use of **Virtualisation**

Virtualisation decouples the hardware from the software.

This decoupling is achieved via an abstraction called a **Hypervisor**

A Hypervisor emulates all the functionality of a real computer, but it's not a real computer - it's a virtual machine (VM).

The hypervisor can run multiple VMs at the same time, and optimize the performance of the abstracted hardware.

So Azure does virtualisation on a MASSIVE scale.

Microsoft has a ton of servers right. Each of those servers uses a hypervisor to then multiple VMs.

These racks and racks of servers are connected to a network switch via a Fabric Controller.

Each Fabric Controller connects through the network switch to connect to an Orchestrator.

The orchestrator is like Spiderman - with great power comes great responsibility, and one of the things the orchestrator is responsible for is responding to user requests.

These user requests are made directly to the orechstrator via its web API. This API can be called by Postman, Insomnia or by the Azure Portal.

So, when a user makes a request via this orchestrator API to create a VM, the orchestrator packages up everything that is needed, takes the best server rack (based on the users requirements, like location, or region pairing, and Azure requirements), and then sends the request and the package to the fabric controller via the network switch.

Once the fabric controller creates the VM, the user can connect to it.

---

VMs are just the beginning of what Azure offers, they are constantly expanding with new tools and services that allow you as a developer to use their services in conjunction with your favourite developer tools/frameworks.
