# Cloud Infrastructure

Cloud is extremely common in the modern day and age. In terms of cloud security (IaaS, PaaS, SaaS, etc), security is vital and well documented. Cloud providers often provide a matrix of responsibilities that everyone must learn up front. These procedures and security protocols may vary from one organization / cloud provider to another.

## Hybrid considerations

Some organizations have multiple clouds under one network. Although this has benefit, this obviously means an entire new system to handle as well, adding complexity. Perhaps server settings or authentications are not the same between cloud systems. Perhaps firewalls on both ends handle each other weirdly.

It can simply also be timely and difficult to log multiple systems at once. And when logging / handling extra data due to new cloud systems, thats an entire new layer of potential data that could leak.\

## Third=party vendors in the cloud

There can be third party vendors applied to parts of the cloud. A third party firewall for an application on the cloud is an example. Much like other security practices regarding applications, risk assessment and monitoring is important. How trustworthy are these??

However, these third party vendors are still part of incident response. They can still be damaged based on any threats that come into the cloud.

## Infrastructure as code

Cloud infrastructure typically refers to the coded side of the system, you describe it as code. What servers, networks, applications, exist in code? Much like regular application code, this can typically be modified to ones liking. 

Similarly, the code can be used as a reference / blueprint for other code instances for consistency purposes. This is an important concept in cloud computing; versions of cloud can be consistent and perfect each time.]

## Serverless architecture

Some systems might not allow access to a server. Instead, **FaaS (Function as a service)** might be utilized. Instead of relying on one application, this application is split into individual, autonomous functions. This provides much less emphasis on the system itself because we only really worry about the functiomn itself.

This is still server-side; the server / organization still handles this. These are typically run on a stateless compute container for ease of use. The fact that it is coded or used like this means it is also possible to make these event triggered and ephemeral / temporary.

## Microservices & APIs

Cloud allows for monolithic applications; these are applications that do a whole bulk of the processes and business logic related to a service (Supabase for SQL as an example). This creates some code complexity and challenges as these apps are not thes easiest to make.

## APIs (Application Programming Interfaces)

APIs are a set of rules and protocols that allow different software applications to share data / communicate with one another. This API allows direct and trusted connection and I/O from client to server.

These work together to act as the application; you usually do not act with the server itself. You talk to the API gateway which talks to the server. 

These are scalable in cloud. You can have the client interact with one API gateway, which can talk to multiple microservices. And these are quite contained and secure in a sense that if one service gets affected, the others do not simply because they are not directly communicating to one another.

# Network Infrastructure Concepts 