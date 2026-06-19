# Denial Of Service (DoS)

Denial of Service is when attacker forces a server to fail. This can happen either by overloading the service, or just taking advantage of a known vulnerability. These are a big deal in the corporate world; companies like Amazon or Instagram tend to lose millions in value during DoS attack.

These also can work as a smoke screen for some other exploit. While everyone is focused on recovering the server, the threat actor might be planning deeper exploits.

# "Friendly" DoS

These happen and are annoying but do not happen to malicious intent.
- Unintentional Dosing
  - Some scripts mess up. Some ping tests might go on forever.
  - Games on day one release are similar; too many players = server fault.
- Bandwidth DoS
  - Downloading a large file can cause this.
- **Server was simply powered off / restarted**
  - This happens too.

## DDoS (Distributed Denial of Service) 

This is DoS, but larger scale. This can involve multiple devices spanning across multiple networks. They try to use up all the server's resources and bandwidth.

These usually are not concentrated in one network but rather exists through **botnets**; malware is infected to victims computers and from that point on, the threat actor can coordinate an attack via all infected devices.

## DDoS reflection and amplification

Attackers may attempt to amplify or reflect data to the victim server to make the "denial of service" happen faster. This is increasingly common with DoS attackers nowadays.

Protocol abuse is a common method of this. Many servers will have open ones that do not have much security. ICMP, DNS, NTP, etc. It's important to note that some of these are not designed with security in mind; thats the point. This creates a DDoS risk.