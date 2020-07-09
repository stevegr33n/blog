# Compose SLAs across services

Basically SLAs can be combined. So you'd have one SLA for one product or service and another for another product or service.

You can combine these SLAs into what the Microsoft kids call a **Composite SLA**

The Composite SLA can proivder higher or lower uptime - depending on your app.

Lets say we have an app hosted on a Service Web App and it writes to an Azure SQL Database.

The Web app has an SLA with 99.95% uptime and the DB has an SLA with 99.99% uptime.

If either service fails the whole app fails. If we combine the SLAs to form a composite SLA we have:

99.95 x 99.99 = 99.94

This means the combined probability of failure is higher than the individual SLAs.

Not surprising right, as the app relies on more things and the more things there are the more likely somethings gonna break.

To improve the Composite SLA we can add a fallback path.

If the app cant write to the DB because the DB is down, then we can write to a Queue instead. Then once the DB is back up the Queue can process the transactions into the DB.

So we're sort of mitigting the downtime of the DB. The Queue however also has a downtime, this is 99.9%.

The DB and the Queue could both fail at the same time. The expected percentage for a simultaneous failure is 0.0001 x 0.001.

So the Composite SLA for the DB and the Queue is:

1.0 - (0.0001 x 0.001) = 99.99999%

If we then add Service Web App into the mix, our Composite SLA would be:

99.95 x 99.99999 = ~99.95%

So, the composite SLA has a better uptime with the queue than without.

But, the application logic is more complex and the costs are higher.
