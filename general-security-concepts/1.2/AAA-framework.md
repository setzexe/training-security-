# Authentication, Authorization, and Accounting

Identification on a network or system usually follows the AAA framework. Take your typical log-in on a website for example.

You **identify** yourself. This is who you claim to be and it is typically a username. This is paired with a password to **authenticate** you, verifying that it actually is who you identified as.

After you are authenticated, you are **authorized** to do whatever privileges you have access to do. Essentially, what privileges do or do you not have based off your role / authentication?

More behind the scenes is **accounting**. This logs information related to the login. Login time, data sent and received, and potential logout time.

## Practical example

A client needs to use the internet to log into a VPN server (a firewall for example) and you need to use triple AAA to access an internal file server.

This client will send his information to a firewall that the company uses, which sends this data to an AAA server. This **AAA server** is responsible for handling certain policies and protocols in relation to AAA. If the server authenticates the user, the AAA server lets the firewall know its a safe user. The user can now access the internal file server.

## Authenticating systems

In cybersecurity, you will have to manage many devices within a network. Often, you will never even be able to physical see those systems. They might be all the way across the globe in some random industrial zone.

This is why authentication is so important: **How can we verify that a computer attempting to log in to a network is authorized or allowed to access this network?** 

A **digital certificate** is used for this. A signed digital certificate is added to a device that is sent for authentication. No recognized digital certificate = no access. Other business processes will rely on this digital certificate. Management will have a way of confirming the end device.

## Certificate authentication

Organizations that utilize Digital Certificates must have a trusted **Certificate Authority** (CA). Most organizations maintain their own, but it is not required. You use this certificate authority to create certificates for devices. It can now be used as an authentication factor, with the CA's digital signature validating the certificate.

## Authorization models

Now that a user or device is authenticated, what are they allowed to do? What are their privileges? This is **authorization**. We typically want to implement models (you could consider these more like policies) to the user / device / group.

Typically, this is done through users and services -> data and applications. Note that this alone does not scale. You will have to do this individually unless you have some middleman. This is where roles / groups / organizations / attributes come in. If 46 user's have an employee role, make an employee authorization model. 

This is very common in large scale systems and is typically referred to as **abstraction**. It reduces complexity and makes a clear relationship between the user and the resource.

If new management is added to a company, adding permissions one by one would suck. Simply adding the person to a management role / model is much more efficient.