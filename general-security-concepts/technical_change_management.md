# Change Management 

When making a change to your local network, the scope of the change is usually on one computer. In a organizational world, changes often apply to entire systems. Upgrading software, patching applicatons, firewall configuration, etc. This also means that **changes can and will affect whatever is involved with what you are changing.**

Changes like updates are extremely important for keeping up with growing trends like security. Less updates / patches = more suspectibility to newer attacks. 

This **does not** mean to always do changes. Too many updates that could be compressed into one bigger one will probably have effects on other systems or server availibility. This is why **clear policies** for updates, frequency, duration, installation, rollback, and so on are important and very recommended.

## Change approval process

There is a formal process for managing change to ideally avoid downtime, confusion, and mistakes.
- Typically, people involved complete request forms that determine the purpose and scope of the change.
- Schedule a date and time for that change
- Determine what systems will be affected & the risk associated
- Get approval & get end-user acceptance

The owner of the system is the one who decides on what to change. However, they are not the ones to really do the change itself. They manage the process. They get process updates and ensure the process is followed and acceptable.

Suppose a companies address label printer needs to be upgraded. Although shipping and handling own the printer-- thus they control the process-- IT handles the actual change.

## Stakeholders

Stakeholders (unfortunately) have a big say in changes. A single change can include from one person to an entire company. 

If we upgraded the label printer and got better & faster labels, shipping / receiving is positively boosted, accounting reports rise --> CEO visibility due to increased revenue due to faster product delivery.

## Impact Analysis

Changes come with impact. It is important to understand the potential risk of this impact. It can be minor or far reaching. The fix might not fix anything and just end up breaking something else. But it is also important to understand the risks of NOT making a change. Outdated software = potentially more attacks.

## Testing

Testing is heavily recommended to see how a change might result. Virtual environments or sample data as examples. This should not include any real world data. This is used heavily to gain insight before making a change or an update. 

Documentation is important too. Not even for testing, but for the change process as a whole.

## Backout Plan

This is like a backup plan in case the absolute worst happens. If a change causes catastrophic damage, you should have a way prepared to back out / revert this change. Always have backups.

## Maintenance Window

You need a time window to actually implement this game. Like most online games, there are moments of downtime once a week to implement a change or update. This is the same process. You ideally need to plan this out based off usage and availability. Overnights usually are best for this reason.

# Technical Change Management

When the actual change is implemented, it is usually relied on the technical staff. This is a bit more complex as we are dealing with systems that span across multiple devices. The technical team is moreso concerned with how to make a change happen.

A common change example is an access / deny application list for an organization. You can have a list that has both, or just an access list (only sites on allowed list can be accessed. Very restrictive) or a deny list (anything can be accessed besides stuff on the deny list).

## Restricted Activities

You should only really do changes on what you are required to do. If you have to tinker / change other things a bit to reach that primary change, that is ok within limits. But even if you have extra time and resources, unless allowed or properly stated by the owner, there is no reason to make change to other systems.

## Downtime

This is just when services are unavailable due to change. If possible, downtime should be prevented. A secondary system or backup is often recommended. Similarly, the less downtime events, the better. If possible, downtime and maintanence should be automated and within a fixed schedule.

It is also important to let anyone affected know, via direct communication, banner, alert, etc, that a downtime will happen in the future.

## Restarts

Updates usually require a restart. This applies in different forms; maybe powering on & off or a switch for physical, stopping and restarting a process / service, restarting an OS, etc.

## Legacy Applications

There are many such cases of organizations using applications that may not be very relevant today or even worse, have no support from the developer. You are the one who has to document and understand the system from that point.

## Dependencies

This is that concept that some services might not work or do things without the current status or work of another service. If you wanna complete A, you must complete B. Modifying one component may require changes to another component. This can happen across systems.

## Documentation

Like with most tech based stuff, documentation is extremely important. It helps with understanding the system in the long run and being able to identify strengths and weaknesses. Updating diagrams, modifying network configurations, addressing updates, etc.

## Version Control

This is just to track changes to a file or system over time. Like a very detailed log for changes. This is like with GitHub commits.