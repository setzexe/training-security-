# Secure Communications

Secure communication is an important aspect of cybersecurity. Unencrypted or visible data, especially with important information, should never be something a random user could see.

**VPNs (Virtual Private Networks)** exist and allow for encrypted data traversing on a public network. You may also find **VPN Concentrator's.** These allow for multiple uses on a VPN server / connection. This is often found at the edge of a firewall. The VPN concentrator is responsible for decrypting the data and getting it to the corporate network.

There are many deployment options. Third party options exist, but you can easily find specialized cryptographic hardware. Sometimes, software for this purpose could be incorporated into a device's OS itself.

## Encrypted Tunnel

Encryption makes this secure communication possible. The original packet contains an IP Header and Data, which are the very valuable parts. But once this is encrypted, how does the network know where the destination IP is now? This is why we create other headers that will be publically available, and encrypt the original data within these new tunneled headers. The other side is responsible for decrypting this information.

## SSL/TLS VPN (Secure Sockets Layer VPN)

Devices like laptops, desktops, mobile end devices, etc, use a SSL/TLS VPN. **TLS is the modern and secure SSL, but both terms are still used.** TLS is the protocol (Tcp/443) used to encrypt web traffic. This allows for almost no firewall issues.

This is primarily more used for single devices and use remote access configuration, mainly through some app that allows this. Like IPSec, users can be authenticated through these means. Digital certifications or shared passwords usually have no requirements.

This is a very native process and usually can be run from a browser. This allows for on-demand access from a remote computer. The software would connect to the VPN concentrator.

## Site-to-site IPsec VPN

These are extremely common and usually are always on. These allow very specific site to site encryption. In this case, the firewalls typically have the VPN concentrator.

## SD-Wan

Software Defined Networking in a Wide Area Network (SD-Wan) is a newer way to connect devices, information, or parts of a network to each other. It used to be based on cables and everything being in a set area. The cloud changes this and allows for a smart router (the SD-Wan) to encrypt and allow data to be traversed across wide parts of a network.

## SASE (Secure Access Service Edge)

SASE follows the exact same process as an SD-Wan except it is often larger scale and usually allows outsider people to see cloud data. SASE adds extra security next to any important data. Security technologies already exist within the cloud. These typically include protection from malicious links, authentication controls, etc.

## Selection of Effective Controls

Organizations need to utilize some form of secure communication. Some will use one form while others will use multiple forms. Choosing different forms is based on what your needs are or what you already have.

**VPNs** are essential. SSL/TLS for user access, and IPsec for site-to-site.

SD-WAN's allow network connectivity via cloud, but does not address any security concerns. SASE exists to combat this, but this would require planning and implementation.
