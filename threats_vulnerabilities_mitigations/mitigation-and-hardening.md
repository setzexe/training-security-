# Mitigation

Mitigation is the process of reducing the impact of a security event or a potential security event.

Below are common techniques for this. 

## Patching 

This can mitigate attacks before they even can be conceived. These are incredibly important for system stability and security.

Incremental updates at predictable times are important for user availability as well. 

For personal updating, many third-party update tools exist to find the proper updates and driver updates for a device.

**Emergency patches**, aka patches from outside the typical interval, are common.

## Encryption

These prevent access to data files. Unless the attacker has that file key, they can not see the data within these files.

Full disk encryption (**FDE**) is common for hiding large amounts of data at important moments.

# Monitoring

Monitoring and logging information is important. These can track attacks before they happen or just show data that might lead to tracking down a threat actor.

Sensors, security cameras, firewalls, WireShark, etc.

## Least privilege

The modern safety practice is to not trust every user. This is why many organizations have rights and privileges set to only what the user needs, nothing more. Only what is needed to complete objectives. Users should not run with administrative privilege. Applications should run with minimal privileges.

## Configuration enforcement

These performs a posture assessment on devices when they access a network; is the OS, drivers, security system, certificate, and much more up to date? If these are not up to date with what the configuration enforcement wants, that device might be quarantined until it is fixed.

## Decommissiong

Not as common, but this refers to when we stop using a piece of technology. While it is easy to just store it to the side or throw it away, it is possible that these could still contain vital information that could still be accessed, especially now that it is out of maintainence. 

The data is mostoly related with storage devices; SSD, hard drive, USB drive, etc. As for the physical component / device, there are many options. Perhaps another organization could recycle and find use in it. Otherwise, destroying it is completely fine too.

