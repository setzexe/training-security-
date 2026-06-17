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