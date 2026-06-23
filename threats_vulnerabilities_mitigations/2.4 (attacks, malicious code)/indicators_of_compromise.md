# Indicators of Compromise (IOC)

This refers to an event that indicates a possible intrusion. Confidence is high and security / management is on standby.  

These indicators can include, but are not limited to:
- Unusual amount of network activity
- Change to file hash values
- Irregular international traffic
- Change to DNS data
- Spike in read data to certain files
- Irregular login patterns

## Account lockout

This is a very common and telling indicator of compromise. This refers to you not being able to access the account, rather through someone stealing the account, or the account somehow being disabled maybe due to managerial controls. 

Sometimes if account credentials can not be obtained, attackers will intentionally act as if they're they victim and use the "Forgot Password" feature on the server, which would allow them to act as the victim and get the new password configured to their liking.

## Concurrent session usage && impossible travel

Usually, users should not be in two places at once. With web servers, it would be weird if a user from and active in New York also had an active session in Somalia. This can be an indicator of compromise.

This is not always the most telling case and often is not even compromise. Multiple desktops and devices (along with automated processes) make this alot more common without malicious intent. **VPNs** also exist. Network logs often can showcase specifics related to this usage. Device, location, etc. 

**Impossible travel** is the New York --> Somalia concept. If someone's workplace is in New York, there should not be multiple log in's and log off's from Somalia.

## Blocked content

Attackers would like to stay on a system for as long as they can. Usually they came from an unpatched error and if this were to get patched, they could lose access. Some attackers/malware implement ways to disable security features on a system. This often includes stuff related to automated updates for certain systems. This prevents potential easy fixes for that patch.

## Resource consumption

Resource consumption is a way of tracking an attackers process. File transfers and many server tools use bandwidth, which can be monitored and checked for unusual spikes. Firewall logs can show outgoing transfer including IP address and timeframes.

It is important to note that attackers could be on a system for months, but the system would not really know until an action is made / resources are consumed.

**Brute forcing** also can cause resource consumption.

## Resource inaccessibility

Servers being down can be a common IT problem. However, this can also (just like the account lockdown thing) be an indicator of compromise. Perhaps an attacker is in the server with malicious intent. Or perhaps the threat actor is attempting to exploit potential vulnerabilities but end up crashing the server regardless, which can happen. 

Server data can be infected by **ransomware** much like personal data; it can be encrypted and made completely unavailable.

## Out of cycle logging

This refers to logs that appear when they shouldn't. For example, perhaps a server uses a certain application to update services across that server. If it happens every week at the same time on Friday, there is no reason for this log to randomly pop up on a Tuesday without any information explaining it.

Firewalls log activities. Timestamps of every traffic flow, along with protocols and applications used.

## Missing logs

Attackers often will delete any traces of attack including log information. Information is everywhere; authentication logs, file access logs, firewall logs, proxy and server logs, etc.

These logs are absolutely suspicious if they need a reason to be deleted / go missing. Logs should be secured and monitored, including alerts on missing logs.

## Published / documented data made available

It is possible for threat actors to exfiltrate data from a server with the server having no knowledge of this until they find it on the internet for anyone to see. This is not an "indicator" of compromise, this just is compromise; your data is openly available. 

This is very common in **ransomware**; threat actors will exfiltrate this data and demand payment from the organization in exchange for this data to not be leaked.

Raw data often may be released without context. Researches can use this data to find the source and let them know.