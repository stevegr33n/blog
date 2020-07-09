# Types of cloud services

There are three major categories of cloud computing:

- IaaS - Infrastructure as a service
- PaaS - Platform as a service
- Saas - Software as a service

## Iaas

This is the most flexible category of cloud services. It aims to give you the most control over the provided hardware that runs your app.

Servers, VMs, storage and OS's this is the infrastructure that is being provided to you as a service - you are renting it. Instant computing infrastructure provisioned and managed via the fucking internet.

The **cloud provider** is responsible for ensuring the cloud infrastructure is functioning properly.

The **cloud customer** is responsible for ensuring the service they are using is configured correctly, is up-to-date and is available to their customers.

These two things togther are referred to as the **shared responsibility model**

IaaS is commonly used for:

- Migrating workloads
  IaaS facilities usually provide an easy migration path for moving existing apps to the cloud

- Testing and development
  Teams can quickly spin up and wind down test and dev environments, bringing new apps to market faster. IaaS makes scaling dev and test environments fast and economical

- Storage, backup, and recovery
  Organisations avoid the CapEx and complexity of storage management which usually requires technical staff to manage data and meet legal and compliance requirements. IaaS is useful to managing unpredictable demand and steadily growing storage needs.

## PaaS

The goal of PaaS is to help you create apps quickly without bothering with the underlying infrastructure.

PaaS provides an environment for building, testing, and deploying software apps.

Example; you don't need to install an OS, install OS updates or a web server when deploying a web app using PaaS.

PaaS is a complete dev and deployment environment in the cloud with resources that allow an organisation to deliver everything from simple cloud based apps to sophisticated cloud enabled enterprise apps.

It's pay-as-you-go once again, with resources being purchased from a cloud provider.

PaaS is commonly used for:

- Deployment framework
  PaaS provides a framework that developers can build upon to develop or customise cloud apps. PaaS lets developers create apps using built-in software components.

- Analytics
  PaaS also provides tools to analyse and mine data. These tools can help the organisation learn more about itself and find insights and patterns to improve business decisions; like improvements for the Flash product for example.

## SaaS

The goal of SaaS is to host and manage software for the end user. It's usually based on an architecture where there is a single version of the software for all users, and those users are paying a subscription fee to use the software.

---

![](./IaaS-PaaS-SaaS-layer-diagram.png)

- IaaS requires the most user management. You gotta manage the OS, the data and the apps.

- PaaS just requires you to manage your app and the data - the provider manages the OS for you.
- SaaS you just use the software - zero management needed.

You can use a combination of IaaS, PaaS and SaaS to fufill your organisations needs right; for example, Office 365 on your companies computers (SaaS), Azure SQL DB (PaaS) to store some data, and Azure to host your VMs (IaaS).
