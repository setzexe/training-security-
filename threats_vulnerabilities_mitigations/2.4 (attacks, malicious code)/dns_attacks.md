# Domain Name System

Domain Name System is just the protocol that devices use to access servers via URL's. Instead of looking up a server's IP, we look up the URL. Attackers try to find ways to make victims go to malicious pages based on this.

## DNS Poisoning

- Modifying the DNS server itself
  - These are very secure. These are not typically how DNS attacks happen.
- Modify the host file
  - The victim device might have cookies or its own local DNS system. Editing this is possible.

## Domain Hijacking

This involves getting access to the actual domain itself. This does not regard the actual server; perhaps a misconfigured porkbun account allowed for DNS access. Now that attacker can make that domain lead to whatever they want.

There are many ways to attempt to get the domain. The usual stuff; brute force, social engineering, email access, etc.

## URL Hijacking

It is very common for mistakes to happen when typing in a URL. Perhaps theres a missing letter or a mispell.

Attackers use this to their advantage; they will buy domains of URLs that they know people will accidentally type in because they think it is the main thing they actually want. This also includes using the wrong top level domain (.org instead of .com).

For instance, if a user wants to use Google but looks up Googel which has a keylogger inside of it, the user might have no idea until its too late. The site might pretend its real (phishing!), or it might just make the user install something malicious. 

### Competitor lense

It is also possible to do this to redirect mispellings to a competitors server instead. However, this can come with legal issues.