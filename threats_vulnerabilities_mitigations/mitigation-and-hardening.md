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

# Hardening

This is the concept of making security systems (or systems as a whole) a lot more secure; like hardening them from penetration.

Below includes common hardening techniques.

## System hardening

This will vary on specifics when it comes to different OSs. But generally, how you go about system hardening is the same.

- Updates
  - Operating system updates, security patches, etc
- User accounts
  - Should have lengthy passwords and complexity. No reason for an employee's password to be 12345678
  - Account limitations (least privilege)
- Network access and security
  - Limit network access
    - Perhaps only a certain IP address range can access parts of a network.
- Monitor and secure
  - Anti-virus, anti-malware, etc

## Encryption

Encrypting any important data is easy and essential. This is very possible with encrypting file system (**EFS**) or, with **Full Disk Encryption **FDE**, using stuff like Windows BitLocker or any OSs respective FDE tool.

Encrypting network traffic when necessary is essential as well. VPNs exist for this reason, HTTPS as well.

## The endpoint

Hardening a device's endpoint so that data can leave successfully is important, making it necessary to stop attackers from both outbound and inbound attacks. 

It is important to point out that there are so many different platforms like mobile or desktop. Protection will be different and multi-faceted.

## Endpoint detection and response (EDR)

It is estimated that there are around 1 million malware varients created a day. To combat this, **EDR** is implemented. These are automated and monitor the endpoint to detect and respond to potential malware/cyber threats. 

This is different from a traditional anti-virus. Anti-virus's block known cyber threats. EDR's detect things based on behavioral analysis as well; is this traffic supposed to happen? If the EDR does not think so, it prevents the traffic from entering. The EDR can act instantly; there is no need for outside approval. This can help monitor root cause, new application processes, etc. 

## Host-based firewall

These are software-based firewalls that can allow / disallow certain traffic on a network. These can have complete visibility to what is going on behind the scenes (unknown processes, encrypted data, etc). This is managed centrally, and also has the ability to identify and block unknown processes. IT can choose to allow these processes if deemed safe manually.

## Finding intrusions

It is important to understand and consistently look out for what potential intrusions might be possible on a device so that you know what to secure. Attackers will try to attack from these places. 

**HIPS (Host-based intrusion prevention system)** is a system that is often built into endpoint protection software / EDRs. These watch for inbound traffic that could be a vulnerability. It also has the ability to secure OS and application configs, having validation security for incoming service requests like updates.

HIPS has a good bit of ways of identification. Signatures, heuristics, behavior, buffer overflows, registry updates, random writing to folders, accessing non-encrypted data, etc.

## Open ports and services

Open ports are a potential attack opportunity. Closing any that would not be necessary are essential. Limiting access / using firewalls to limit what goes into open ports is also essential.

Sometimes, applications and downloaded services open ports that lead to risks or just ask user's to open blatantly broad port ranges (0-65535; this is every port) and the user might not realize.

If you are unsure, Nmap or similar port scanners are a help. Ongoing monitoring is important.

## Default password changes

Every network device has a management interface that you can use to set up settings. These create data that ranges from "interesting to an attacker" to "DDoS incoming".

Changing the default username and password for these (and really, any major device) is important. These defaults can be predicted and there typically is not the *most* security underneath.

## Removal of unnecessary software

All software contains bugs to some degree. Maybe not huge, but there are bugs that will lead to clutter or security updates. You may have also installed tons of applications; this leads to tons of clutter or security updates. This leads to a waste in space, a waste of resources, and more potential attack surfaces.

The easy fix is just removing any unneeded software. It declutters your network and you will never have to worry about it again.