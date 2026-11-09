# Penetration Testing

A penetration test goes beyond a vulnerability scan; it stimulates an attack and starts when vulnerabilities are discovered / scanned to see if they actually can be exploited.

Pentests are often required, usually due to compliance mandate along with legal requirements. The PCI DSS (payment carrd industry standard) requires both internal and external pentests once a year.

## Rules of Engagement

Before any testing starts, everyone signs off a rules of engagement document. This seperates this legal testing from an actual attack. It describes the purpose and scope of the test.

It covers the type of test. This could be an on-site physical breach, an internal / external test, a mix, etc. It also covers the schedule and when this test may happen, along with the actual rules of the test. This includes emergency contacts if something breaks, how to handle sensitive information found during testing, IP addresses in scope, etc.

## Exploiting Vulnerabilities

This is the actual attack phase. Do be careful; attack too hard (like with buffer overflow) and the entire system might go through denial-of-service. Testers usually try different attacks like brute-forcing, social engineering, database injections, so on so forth. Part of the goal is often privilge escalaton.

Attackers often operate through a similar sequence:

- Initial exploitation: getting into the network in the first place.
- Lateral movement: the inside of many networks are unguarded once you are in. You can move from one system to the other usually.
- Persistence: making sure you can get back in later, even after reboot. This could mean setting a backdoor, entering a registry, setting authenticated credentials, etc.
- Pivoting: using a compromised system as a proxy to reach systems you normally could not access. This is similar (but not the same) to lateral movement; a normal computer may not be able to access another part of internals, but your compromised system might.
  
## Pentest Aftermath (Cleanup)

When the test is done, the tester has to leave the network exactly as they found it. Removing any temporary files, backdoors, user accounts, etc. If a backdoor was left behind, that is a legitimate vulnerability that the company would face.

## Responsible Disclosure and Bug Bounties

Not all security testing is done by hired pentesters. Outside researchers find vulnerabilities too. But this begs the question; how is this information disclosed? An attacker may find it first and utilize the exploit.

Bug bounties are popular. Organizations allow researchers to ethically look through their system for vulnerabilities and documenting them, which are given to the company privately through responsible disclosure. Once fixed, the vulnerability information goes public and the researcher gets their reward.
