# Threat Vectors

Threat Vectors (or an attack vector) is the method that an attacker uses to access your systems. A lot of work is spent finding ways to attack your systems, with some ways being more vulnerable or less maintained than others. 

Alot of time in cybersecurity involves identifying vectors. Knowing vectors = knowing how to prevent attacks in them = less prone to damage.

## Message-based vectors

This is one of the biggest (and most successful) threat vectors. Everyone has at least one important messaging system. This includes emails (via malicious link, to a download or site) or SMS (text message, same concept).

**Phishing** is extremely common in SMS. They make you think you are clicking a trustworthy link, but this link instead tries to take your info or download malware. For example, someone pretending to be a family member sends you a link via SMS to get you to do a survey. Upon opening this link installs malware. This is an extremely good entry point for the attacker because it can seem very legit. Social engineering methods like payments or crypto scams are very efficient.

### Voice call vectors

This is similar to message based but via voice, like telephone. **Vishing** is phishing over the phone. Spam over IP (spam calls) and disrupting voice calls are an issue as well.

Not as common, but still one to take note of is war dialing. Attackers will go through random phone numbers and try to access one that might give them access control.

## Image-based vectors

It is more difficult to identify these, as the actual "where is the attack?" part is not obvious. 

Some formats like SVG And XML can be threats. These, along with malicious images in general, have significant security concerns like HTML injection or javascript attack code. Browsers usually provide input validation against these images to avoid running malicious code.

## File-based vectors

This involves more than just malicious executables. Adobe PDF's, ZIP/RAR, any files that consist of many things can hold malicious objects.

Microsoft Office specifically can incorporate documents with macros along with add-on files. Be wary.

## Removable-device vectors

This involves a more physical approach with USB sticks. These are like $10 and can act as an entire computer in a stick, injecting malicious software AND/OR being its own keyboard. Basically a hacker on a stick.

This is catastrophic for data exfiltration; terabytes of data can be extracted with no bandwidth used.

## Vulnerable software vectors

As mentioned, less updates = less security. If an executable gets infected, that is an attack vector the second it is opened.

If an agentless system is involved where users interact with a proxy system to use a central system, an infection of this proxy could also infect users.

## Unsupported systems & network vectors

Relative to both systems and networks, these might be outdated at some point or just might not get the support it needs. This alone brings a massive security risks.

Specifically with network, this connects everything and most important data goes through here. 

Wired connectivity like ethernet can struggle from unsecure interfaces (No 802.1X). Bluetooth can suffer from reconnaissance.

## Open-service ports

This is a huge deal. Most network based services connect over TCP or UDP port. The more services or ports that computer is using, the more chances for something malicious to enter. Perhaps a malicious request for port 22 (SSH).

Every application is going to have its own port. This also ties to the patch thing; more apps + not up to date apps = big danger.

This does not mean block all traffic. There should be firewalls rules stating traffic allowed to any open ports.

## Default credentials

Most devices have default usernames and passwords. If someone gains access to this and there is nothing to protect that user from accessing whatever they need to access, that is an attack vector.

## Supply chain vectors

It is also possible that the supply chain could be tampered with in the supply process. This includes installing malicious codes, putting certain physical components, or the supply truck being stolen.