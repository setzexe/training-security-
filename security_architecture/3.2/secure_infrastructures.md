# Secure Infrastructures

Different sectors of life will hold tech infrastructures that are very different from one another. These will be configured according to specific goals and wants. However, the underlying infrastructure is typically the same across systems despite these differences.

**Firewalls** are very common throughout any good infrastructure to help filter in what comes in and out of certain parts of a network. Of course, this is not the only thing. Honeypots, jump servers, sensors, etc can exist across infrastructures.

## Security Zones

When creating a secure infrastructure, one thing to keep in mind is security zones. These differ from subnet or IP ranges. Security zones logically allow devices to be seperated by use / access type.

Each area of a network can be associated with a zone. Typically, some zones can allow certain traffic / protocols / policies while other zones do not. These can have any name and are not limited to trusted / untrusted areas. You can base this off use (databases, internet servers, etc) too.

This helps simplify policies. We can simply add a policy rule indicating that information from the trusted zones should not go into the untrusted zones. Similarly, internal data should not be accessible by outsider zones.

Firewalls usually help seperate these.

## Attack Surfaces

We need to know how many possible ways that an attacker could enter. A lot can cause a vulnerability; application code / injection, open ports, bad authentication, or human error. Finding ways that attackers could insert themselves is essentials. 

The less methods on an attack surface = less potential attacks. Audit code, block ports on a firewall, and monitoring helps mitigate these.

## Connectivity

Everything contributes to security, including how devices or systems are connected. Data being connected to travel across networks, devices connecting to an internet router, etc.

Physically, it is very common for cables to be laying around even in professional spaces. This is a hazard and should be protected.

Application-wise, encryption and authentication checks help alot. Encryption (IPsec tunnels, VPN, etc) ensures that attackers can not just watch data between devices, and authentication helps prevent attackers from doing this in the first place.
