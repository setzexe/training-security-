# Authentication, Authorization, and Accounting

Identification on a network or system usually follows the AAA framework. Take your typical log-in on a website for example.

You **identify** yourself. This is who you claim to be and it is typically a username. This is paired with a password to **authenticate** you, verifying that it actually is who you identified as.

After you are authenticated, you are **authorized** to do whatever privileges you have access to do. Essentially, what privileges do or do you not have based off your role / authentication?

More behind the scenes is **accounting**. This logs information related to the login. Login time, data sent and received, and potential logout time.

## Practical example

A client needs to use the internet to log into a VPN server (a firewall for example) and you need to use triple AAA to access an internal file server.

To authenticate 