# Zero Trust

Many network systems actually are relative open once you're actually past a firewall and in the network. There are not many security controls. 

**Zero trust** is an approach to network security that tries to combat this. You need to be verified at every / most steps of a network. This covers every device, process, and person. Everything needs to be verified. Multi-factor authentication, encryption, system permissions, etc. 

## Planes of operations

Like many things in life, we can make things easier by breaking things down into components. In this case, **planes of operation**. This applies to physical, virtual, and cloud components.

- Data Plane
    - Processes the frames, packets, and network data
    - Processing forwarding, encrypting, NAT

- Control Plane
    - Manages the actions of the data plane
    - Defines policies and rules
    - Determines how packets should be forwarded
    - Routing tables, session tables, NAT tables

The data plane does the processing of data. The control plane controls how thie processing happens.

Physically, a data plane can include the many ports you may see in a network box. Above that, or just wherever there is space, would be the control plane. This seperation of planes is not just limited to physical seperation, this can be virtual too.

## Controlling Trust

We also need proper trust and authentication. There are multiple factors besides just a digital signature that can be considered when seeing if someone is who they say they are. 

The source and requested resources, along with factors like relationship to the organization, physical location, type of connection, and so on, are things to look out for. Authentication systems should coorelate to this.

**Decreasing the number of entry points** also reduces the threat scope. Less attack entry paths coorelates to less possible attacks, or at least less management. 

**Policies** are very important for the to-do's and not-to-do's in both tech and organizational spaces. Having a predefined set of rules ensures people related to the company do not do things they are not authorized to do.
