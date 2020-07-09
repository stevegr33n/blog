# Explore Serverless computing in Azure

Serverless is a misleading term as there _are_ servers being used.

What it actually means, is the responsibility of actually managing servers is handled for you.

With serverless, Azure takes care of managing the server infrastructure and allocation of resources based on demand.

Serverless computing is the abstraction of servers, infrastructure and OSs away from the user.

Infrastructure is taken care of for you, you dont need to worry about scaling or performance and once again, you are billed only for what you use with something called Micro-billing, explained further below.

Serveless is PaaS.

Serverless encompasses 3 ideas:

- Abstraction of Servers
- Event-driven scale
- Micro-billing

## Abstraction of Servers

You never need to explicitly reserve a server instance; the platform manages that for you.

You don't need to manage infrastructue, or install an OS, or update software - it's all taken care of by the provider.

And the provider will make sure your app has high availability. You app will continue working under any workload.

Your app can scale from nothing, to 10's of thousands of requests with _zero_ configuration.

Each function execution can run on a different compute instance.

With serverless you just deploy your code and it runs with high availability. Boom. That's it.

## Event-driven scale

Serverless is a great fit for workloads that respond to incoming events.

Events like; a trigger on a timer - like a function that needs to run at 10am each day.

Or for HTTP calls, or for queues.

Instead of writing a whole app, you just write the function which contians both the app code and the metadata about its triggers.

The platform will automatically run the function and scales the number of compute instances according to the number of incoming events.

## Micro-billing

With serverless you only pay for the time your code is actually executing. If your code runs once and takes 2 minutes, you get charged for 2 minutes.

# Azure Functions

Azure has 2 implementations of serverless compute:

- Azure Functions
- Azure logic Apps

## Azure Functions

Azure functions are when you just wanna run your code. You just want your service to run. Usually when you want to run code in response to an event. This event is often by a REST request, or a message from another Azure service.

Remember, Azure functions are supposed to finish quickly, in seconds or less.

Azure functions scale automatically based on demand. So they are a good choice when demand fluctuates.

Using a VM approach instead would cost you money even when your VM is idle.

Azure functions can either be stateless (the default) where they behave as if they were restarted every time they respond to an event, or stateful where a context is passed through the function to track prior activity.

If you want to track prior activity your function would also be called a **Durable Function**.

Functions are a key component of serverless computing but they're also usual as a general compute platform for running any type of code.

If your needs change then you can just deploy the code in an environment that isn't serverless. Somewhere that lets you manage scaling or run on virtual networks.

## Azure Logic Apps

Azure Logic Apps are similar to Functions.

They can also be trigged by an event. But where functions execute code, Logic Apps execute workflows designed to automate business scenarios and are built from predefined logic blocks.

Every Logic App starts with a trigger.

The Logic App Engine then creates a Logic App instance that runs the actions in the workflow.

These workflow actions cam have flow controls like conditional statements and loops.

You create Logic App workflows using a visual designer on the Azure portal. The workflows are a JSON file that contains a workflow schema.

Azure provides over 200 different connectors and processing blocks to interact with different services.

You use the visual designer to link connectors and blocks together, passing data through the workflow to do custom processing - often without writing any code.

---

## Functions vs. Logic Apps

They can both create complex orchestrations.

An orchestration is a collection of functions or steps that are executed to accomplish a task.

With Azure functions you write code to complete each step of this task, and with Logic Apps you use the visual designer (a GUI) to define the actions and how they relate to each other.

Azure functions are imperative

Logic Apps are declarative

---

You can't just take any old app you have and instantly make it serverless.

If you want to convert your app to a serverless computing model you would likely need to reorganise your app to an event-based architecture.

If you have an existing app that you want to add capactiy to and you are comfortable with containers, and you are able to repackage your app - you could use containers.

It would be much easier to simple use an Azure VM for your existing app, you can configure the VM server to simply match you on-prem server.
