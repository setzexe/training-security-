# Infrastructure considerations

These are things to generally consider when handling infrastructure.

## Availability

System uptime means the ability to access data and complete transactions; this is foundational to IT. It is important to tie this into security; availability does not always mean available to everyone. You would need your data and tools to be available to whoever needs it.

Alot of money and time is spent to ensure availability. Monitoring, redundant systems, etc. This is an extremely important metric (CIA).

## Resilience

Can you recover availability quick? Can you maintain it? These are resilience and it is affected by multiple different variables. The root cause, replacement of software/hardware, etc.

The term related to this is **mean time to repair**.

## Cost

Cost is a very important consideration. Initial installation and later maintanence might vary heavily in costs, as you may have no idea how these systems work.

Maintanence also just naturally costs money as it happens. Same with replacement and repair costs, and the unfortunate tax implications.

## Responsiveness

We typically expect and want responses from a server, and the sooner the better. Humans hate delays, making responsiveness especially important for interactive applications.

Speed is a very important metric. All parts of the application contribute and there is always a weakest link.

## Scalability

How quickly and easily can capacity be increased / decreased? Services might need to experience this multiple times throughout the day. 

A lack of scalability is usally caused by resource challenges. Maybe a lack of resources or misconfigured resources. 

Scalability naturally requires monitoring / security relative to scaled content.

## Ease of deployment

Applications have many moving parts. Web servers, databases, caching servers, firewall, etc. This might be an involved process that has other factors like cloud budgets, change control, etc.

This could be very simple; automated and simple implementation. But this can go terribly wrong if even one missing detail exists. This is important to consider in the engineering phase.

## Risk transference

It is not uncommon for an organization to transfer risks to a third-party. **Insurance** is very common for this; ransomware has actually made this a lot more common. These recover internal loses including outages and business downtime.

These can also help the customer or help with risk against customers. The insurance might provide lawyers, payouts, etc.

## Ease of recovery

Recovery plans should be common and thought out. Time is money; preparation is important. Would reloading from a corporate boot image work? Would it be easy? Would it affect any other systems?

These, once again, are very important to security engineering and should be considered with the final product.

## Patch availability

Software is not usually static. Bug fixes are needed, security updates, etc. This is often the first task after installation because we naturally want to use the most up to date software. 

Most companies have regular, scheduled patch dates. But it also could be the case that some organizations might not patch often, which *is* a concern.

## Inability to patch

Perhaps patching is not even possible. This happens sometimes with embedded systems; since they do not usually work with an OS and have like one purpose, they don't get patched. These systems are not designed for user-end updates, which tends to be short sighted and growing more common. This still can lead to attacks/risks. **Additional security controls** protecting this device is a proper solution.

## Power

Modern technology requires some form of power. On the cloud, premises, does not matter-- power is essential. It is one of the most important components of technology. The amount of power that an organization can bring in is taken into account.

Backup services or secondary services can help heavily.

## Compute

An application will use heavy computing power, utilizing the compute component (a compute engine in cloud terms). These process and handle data. These are often more than just a single CPU, they are like mini systems (multiple CPUs) that work with all these tasks assigned to it.