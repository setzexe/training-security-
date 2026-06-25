# Other Infrastructure Concepts

Attacks can happen anywhere. You can ask anyone in IT and they may give you two seperate answers on where data might be more secure: the cloud, or on-premises.

- Cloud
  - This is centralized and costs less since a third-party handles everything. However, that is also it's main issue. Users may not focus on how to securly implement these systems because they may expect the third party to do all the work, or the third party gets compromised.
- On-premises
  - This is alot more direct and you have more control over the data. While security and costs might generally be more, this allows much more personalized security.
  - An on-site IT team can manage security better, although these local teams may be expensive. But the tradeoff is more flexible uptime and availability.

Cloud or on-premises regardless, attackers want this data.

## Centralized vs. decentralized

Most organizations run a physically decentralized model; there may be many locations, cloud providers, operating systems, etc. It can be difficult to manage all these and protect so many diverse systems.

IT teams can **centralize** these systems to make them more manageable; correlate alerts, make them comprehensive with one another, consolidate log analysis, etc. Although it is difficult to perfect these; a single point of failure could lead to many implications.

## Virtualization

Virtualization runs many different operating systems on the same hardware (VMs). Each VM gets it's own operating system, which adds overhead, complexity, and generally is just more expensive.

## Application containerization

To shy away from the problems that virtualization might bring, organizations might use containered environments. This allows multiple applications to run simultaneously from one piece of hardware. These containers have everything needed to run an application except for stuff revolving around the operating system. Since many of these containers can use the same OS, they are seperate from each other yet can use the same power. Very much more efficient. 

Containers are usually configured for one OS. You might have a different set of containers for another operating system.

## IoT (Internet of Things)

These are things that connect to a network and can be used for day for day business. Sensors, doorbells, lighting, heating and cooling, etc. This also includes smart watches, health monitors, temp / lighting checkers, etc. It is important to mention that IoT manufacturers are **not typically security professionals.** 

## SCADA / ICS

SCADA **(Supervisory Control and Data Aquisition System)** is a large scale, multi-site **industrial control system (ICS)**. These are control systems / sites that manage equipment like power generation, refining / manufacturing equipment, facilities like industrial, energy, logistics, etc. This allows real-time information and security controls.

This should be segmented heavily from the outside public. Access to this could provide terrible consequences to real world needs like power.

## RTOS (Real-time Operating System)

Windows, Linux, and most main used OS are non-deterministic operating system. There is no single process that can take use of all the resources from the machine at once for whatever purposes. Sometimes systems need this **RTOS (Real-time operating system)** to do certain things. Take breaking your vehicle suddenly; crashes would be alot more common if this was not possible. 

Because these have real world use, these need to be properly available and maintained. These are extremely sensitive to security problems.

## Embedded systems

It might be difficult to access an OS running on an embedded sytem. This is hardware/software designed for a specific function or to operate as part of a larger system. These typically only have one main purpose. Traffic light controllers, digital watches, medical imaging systems, etc.

## High availability

Availability is a core of the CIA triad. The more availability = the less likely for attacks. High availability is the concept of always being on and available. These may include multiple components to make work. 

Higher availibility does not always mean higher costs. There is always another contingency you could add; upgraded power, high-quality server components, etc.