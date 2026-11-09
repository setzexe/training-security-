# Security Tools

These are tools for general security monitoring. These can do different jobs, like checking if a system is configured correctly (SCAP, benchmarks, agents), collection of data (SIEM), stopping threats (antivirus's), etc.

## Configuration and Compliance Tools

Organizations run lots of security tools from different vendors, meaning each may evaluate tools differently and make things messy. **SCAP (Security Content Automation Protocol)**, maintained by NIST, gives all tools a common standard and criteria: validating security configurations, confirming a patch was installed, or scanning for breaches. It is especially useful in large organizations with many tools. It benefits heavily from automation.

**Benchmarks** are a set of best security pratices for a type of system, like the bare minimum security settings a system should have.

For compliance checks comes **agent-based / agentless checking**. Agent-based checking installs a small agent that can always run and send real time notifications to ensure compliance. Agentless only checks that device at the moment of the check.

**SIEM's (Security Information and Event Management) provides centralized log aggregation with advanced reporting; very handy.

## Threat-stopping and Network Tools

**Anti-virus** and **anti-malware** are similar, but anti-virus refers to a specific type of malware (trojan, worms, viruses) that can ideally spread. Anti-malware is anything malicious.

**DLP (Data Loss Protection)** is about protecting sensitive real-world information like credit card numbers or SSNs. The goal is to stop this data (wherever its living) from being able to exit organizational reach. DLP refers to the entire process and this usually involves multiple parts (cloud-systems, endpoints, etc).

**SNMP (Simple Network Management Protocol)** is how network devices report their status to a monitoring system through polling; each device has a MIB (manageable information base) of everything that can be monitored, along with an OID (object identifier). It then asks each device for its statistics using UDP port 161. The downside of polling is that devices may already be damaged and only respond when asked. **SNMP traps** exist for this; they can be configured and if the system were to go through something malicious, it sends a response without waiting to be asked. This happens on UDP port 162.

**NetFlow** gathers traffic statistics about the flows of your network. It has two parts: a probe that watches network traffic and creates summary records, and a collector that stores those records. A seperate recording application makes the data readable.

**Vulnerability scanners** identify systems and test networks from both the inside and outside, gathering as much detail as possible with filtering done later.
