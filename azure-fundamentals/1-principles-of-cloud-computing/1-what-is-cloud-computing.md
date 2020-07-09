# What is cloud computing?

Cloud computing is renting resources as and when you need it on another company's computers. You only pay for what you use.

Examples of cloud computing services:

- Compute power - like Linux servers or web apps for computation and processing
- Storage - like files and databases
- Networking - like secure connections between the cloud provider and your company
- Analytics - like visualising telemetry and performance data

Compute power is generated from:

## VMs

Isolated and secure running on physical servers in a cloud provider's datacenter

## Containers

Isolated and consistent execution environment for apps. Similar to VMs but they don't need a guest OS. Instead the app and its dependencies are packaged into a container, and then a runtime environment is used to execute the app. This is is faster than a VM as there is no OS to boot and initialize. Docker is one of the leading platforms for managing containers. It allows different components of the app to be deployed independently on different containers. Multiple containers can run on a single machine/VM. Containers are super portable and can be deployed in multiple environments (on-prem/in the cloud) often without any changes to the app.

## Serverless

Serverless computing lets you run app code without creating, configuring or maintaining a server.

The core idea is that your app is broken into seperate functions that run when triggered by some action. For exmaple lets say a customer makes an online purchase; a serverless function is then triggered to send a confirmation email to the customer.

The serveless model is different from the VM/Container model in that you only pay for the processing time used by each function. VMs and containers are charged while they are running - even if the apps on them are totally idle.

Serverless doesnt work for every app, but when the app logic can be seperated to independent units, then you can test them seperately, update them seperately and launch them in microseconds - making this the fastest approach for deployment.

## Storage

Most apps read/write data, cloud providers offer services that cand handle different types of data. If you wanted to store text or a movie clip, you could use a file on a disk. If you wanted to store data that had a set of relationships you could use a database.

Cloud based storage has the same benefits as mentioned above with cloud compute - mainly that you only pay for what you use and you can easily scale.
