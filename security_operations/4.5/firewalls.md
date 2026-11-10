# Firewalls

The most basic security control is a firewall. It sits an a boundary or an **ingress/egress** point (where your network meets the outside world). The firewalls takes this traffic and decides what can come in and out.

## Network-based Firewalls

Firewalls usually sit at the edge of a network and filters traffic by port number / application. Most firewalls operate on layer 3 (the network layer), so they can act as other devices like routers, VPNs, and **NAT (Network Address Translation)** which translates private IP's to public internet accessible IP's.

## Next-generation Firewalls (NGFW)

While network-based firewalls mainly work based on ports / IP addresses, NGFWs work on layer 7 (the application layer) so it can see all the packet data. Because it understands applications, it can control traffic by application even if they were to come from the same port. These firewalls usually include IPS and content filtering. The tradeoff is that analyzing packets in detail is more resource consuming.

## Ports and Protocols

Traditional firewalls make decisions based on the protocol (TCP or UDP) and the port number. NGFWs use that too, along with the application-level checks. Some common port + protocol combinations:

- TCP 80 (HTTP) and TCP 443 (HTTPS)
- TCP 23 (SSH)
- TCP 3389 (Remote Desktop)
- UDP 53 (DNS)
- UDP 123 (NTP)

## Firewall Security Policies (Rules, ACLs)

Firewwall decisions come from a list of rules called an ACL (Access Control List). Each rule allows or denies traffic based on a set of criteria, often called tuples.

The firewall reads rules top to bottom, and acts on the first rule that fits the packet. Specific rules should be at the top and general at the bottom.

A golden rule of most firewalls is that, by default, they will automatically deny that traffic if it does not follow any of the rules.

## Screen Subnet

A screened subnet (used to be known as DMZ) is a seperate network section that sits between the internet and your internal network. This is where you put things the public would actually use, and this is seperate from that network.

If this web section were to be compromised, they may have to go through extra means (like a firewall) to enter the rest of the network.

## IPS Rules

An IPS (Intrusion Prevention System) is usually built into a NGFW. It watches traffic as it passes through and looks for any malicious data. It finds threats in two ways:

- Signature-based detection looks for perfect matches to known attack patterns. It is very accurate for known threats, but can not catch anything new / it has no signature for.
- Anomaly-based detection builds a baseline of what normal traffic is supposed to look like, then monitors and flags and traffic that looks out of the ordinary to this baseline. This could lead to more false positives, as weird traffic can easily be human nature.

Administration decides from there what to do with that traffic (block, allow, alert, etc).
