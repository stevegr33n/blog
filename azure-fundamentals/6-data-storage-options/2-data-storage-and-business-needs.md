# How Azure data storage can meet your business storage needs

Azure provides several storage options for different data types

- Azure SQL DB
- Azure Cosmos DB
- Azure Blob Storage
- Azure Data Lake Storage
- Azure Files
- Azure Queue
- Disk Storage

## SQL DB

SQL DB is a relational DB as a service - DaaS. DaaS good ya?

It's based on the latest version of Microsofts SQL Server DB engine and because it's DaaS it's provided to us and managed for us exactly like SaaS.

DaaS model is similar to a SaaS in that it provides software as a service, but DaaS is usually more extensive.

You can use SQL DB to build front-end apps and build websites without needing to manage your DB infrastructure.

You can migrate existing SQL server DBs with minimal downtime using the Azure DB migration service.

All you need to do is change the connection string in your apps or websites and the Microsoft Data Migration Assistant will take care of the rest.

## Cosmos DB

Cosmos DB is a globally distributed DB service.

It supports schema-less data that lets you build responsive and **Always On** apps to support constantly changing data.

You can use this **Always On** feature to store data that is updated and maintained by users around the globe.

## Blob Storage

Blob Storage is unstructured, so you can store whatever kind of data you want in it.

Blobs are highly scalable, like flubber. It kinda works like a file on disk, you can read and write data to it. Seems like a good fit for videos.

Blobs aren't limited to common file formats, it can pretty much hold anything.

Blobs are also good for backing up data for archiving or incase of disaster recovery.

## Data Lake Storage

Data Lake lets you perform analytics on your data usage, preparing reports and shit.

Data Lake is a large repo the stores both structured and unstructured data. It stores all your tweets, you relational DB, your videos, Sensors, Website data - all this stuff. Then you can perform machine learning, and queries, and analytics on this Data Lake Store.

Data Lake combines the scalability and cost benefits of object storage with the reliability and performance of Big Data file system capabilities.

Btw, Hadoop and Spark are analytic engines.

## Azure Files

Azure Files offers a managed file share in the cloud.

You access your file shares via the SMB protocol (Server Message Block).

You gotta mount your file shares and that can be done on-prem or in the cloud.

Apps running Azure VMs or cloud services can mount a file share to access data, just like a desktop app would mount a SMB share.

Any number of Azure VMs can mount and access the file share at the same time.

Typical usage for Azure files is when you wanna share app data.

## Azure Queue

This is a servicefor storing large numbers of messages that can be accessed globally.

It can be used to help build flexible apps and seperate functions for better durability across large workloads.

When app components are decoupled, they can scale independently.

Queue storage provides async message queueing for communication between components.

Usually there are one or more sender components and one or more receiver components.

The senders add messages to the queue and the receivers take messages from the front of the queue.

Queues are good if you need to:

- create a backlog of work and pass messages between different Azure web servers
- distribute load among different web servers and manage bursts of traffic
- build resilience against failure when many users access your data concurrently

## Disk Storage

Disk storage provides disks for VMs, apps, and other services.

Disk storage allows data to be persistently stored and accessed from an attached virtual hard disk.

The disks can be managed and configured by the user through Azure.

Typical use cases for Disk Storage is when you want to lift-and-shift apps that read and write to persistent disks, or if you are storing data that isn't required to be accessed from outside the VM to which the disk is attached.

So the Disk Storage that is attached to a VM cannot be accessed outside of the VM that it is attached to.

Disk Storage comes in many sizes and perfomance levels, and you can choose SSD or HDD.

Use HDD for less critical workloads, and SSD for critical production apps.

---

## Storage Tiers

Azure has 3 tiers for blob object storage

- Hot Storage - data that is frequently accessed
- Cool Storage - data that is infrequently accessed - stored for 30 days
- Archive Storage - data that is rarely accessed - stored for at least 180 days

## Encryption and replication

- Storage Service Encryption (SSE) - it encrypts the data beofre storing it and decrypts the data before returning it - this is transparent to the end user
- Client-side Encryption - this is for when the data is already encrypted by the client-side libraries, Azure stores the data in the encrypted state at rest, and decrypts it before returning it

## Replication for storage availability

A replication type is setup when you create a storage account.

The replication feature ensures that your data is durable and always available.
