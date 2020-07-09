# Explore Azure App Service

Azure App Service enables us to build and host web apps, background jobs, mobile backends, and RESTful APIs. It's pretty flexible right, and you don't need to manage infrastructure. It's a PaaS.

It offers automatic scaling and high availability.

It supports Windows & Linux and allows you to automatically deploy from GitHub and Azure DevOps.

It basically lets you focus on building your App or Service and not worry about the infrastructure or scaling.

## App Service Costs

You pay for the compute resources your app uses while it processes incoming requests.

You choose an App Service Plan, and this determines how much hardware is dedicated to your host.

This App Service Plan includes how much memory your host has, and whether your host is sharing hardware with other users or not.

## Types of app services

- Web Apps
- API Apps
- WebJobs
- Mobile Apps

Azure App Service handles most of the infrastructure decisions for you.

Deployment and management are integrated into the platform, endpoints can be secured, and websites can be scaled quickly.

There is also a built in load balancer and traffic manager.

All of the app services listed above benefit from these features.

### Web Apps

App Service includes full support for hosting web apps using Java, Node.js, Python etc

You can also choose Windows or Linux as the host OS

### API Apps

Like hosting a website, you can build a RESTful Web API using your language of choice and your framework of choice.

You get full swagger support, and you can package and publish your API in the Azure Marketplace.

### Web Jobs

WebJobs allows you run a program (like a Python or Bash script) in the same context as a web app, API app, or mobile app.

They can be scheduled or run by a trigger. WebJobs are often used to run background tasks as part of your apps' logic.

### Mobile app back-ends

Use the Mobile Apps feature of Azure App Service to quickly build a back-end for iOS or Android Apps.
