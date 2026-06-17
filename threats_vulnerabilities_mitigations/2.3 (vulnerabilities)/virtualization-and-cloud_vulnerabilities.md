# Virtual Vulnerabilities

Since cloud infrastructure is super popular nowadays, it becomes very easy to build virtual machines in a moments notice.

VM's will be a bit more challenging to manage than your average desktop; not because it's not a computer, but because these VM's shut down and turn on often and different VM's have different resources configured to them. If you're managing multiple, they might not all be the same.

That being said, many attacks and similarities will exist from physical machines onto digital machines. The complexity of the machine only changes the setup of the attacker. These vulnerabilities are standard and include stuff like privilege escalation, command injection, and information disclosure if it is possible to access on that VM.

## VM Escape Protection

Although VM's are technically self contained, they have a host that can be used in the case of needing to escape (not just exit) the VM. The host OS or hardware has great control; this controls all of the other VM's and their configurations.

If this was somehow accessed by a malicious source, that would be a huge exploit. The attacker could figure this virtual universe to their liking.

## Resorce Reuse

The **Hypervisor** manages the relationship between physical and virtual resources. This includes RAM, cpu availability, storage space, etc. 

Although the resources are managed by the hypervisor, they can be shared and split between VMs. If a hypervisor has 4 GB of RAM and is managing 3 VM's with 2 GB configurations, as long as it doesn't go over 4 GB then it will split that 4 GB across these VMs. 

This also means data can inadvertently be shared across VMs. This is a risk if it is perhaps data you do not want the user seeing. An attacker seeing even simple configuration might get a better understanding of attack surface.

# Cloud Vulnerabilities

Cloud is relatively new but now extremely utilized in the modern world. Most organizations use cloud in one form or another. This cloud typically handles very sensitive information; attackers absolutely want this information. Unfortunately, at the current moment, many organizations do not end up using the right protections. 76% of organizations do not have proper central management security or authorization. Not only that but a lot of cloud code is unpatched.

## Attack the Service

If you have an application in a cloud, anyone around the world can attempt to connect to it. This also means anyone can try to take it down.

**DoS** is fundamental. This is based on a singular network and not really heavy traffic like **DDOS**, although that is possible too. **Authentication Bypass** is also common. Again, the security on alot of these systems are not too patched. **Traversing directories** or attempting to access further things within a server works. **Remote code execution** in particular takes heavy advantage of unpatched systems.

## Attack the Application

The cloud code is often unpatched or not that standard. Because cloud deals with extremely sensitive data, the fact that this stuff is relatively easy to exploit gives way more of an incentive to attack it.

Protecting against **XSS (Cross site scripting)** is essential. If scripts get in that affect how other users see the service, that could be catastrophic on the cloud. **Out of bounds write** too. This writes to unauthorized memory areas like the buffer or memory (buffer overflow is a type of out of bounds write). This can cause data corruption, improper script running, or crashing. The classic **SQL injection** is a huge risk too. Especially with the fact that a lot more sensitive data is stored.