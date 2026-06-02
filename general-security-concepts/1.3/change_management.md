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