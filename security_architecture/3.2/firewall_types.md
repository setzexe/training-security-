# Firewall Types

Firewalls are the universal security control of a network. These control the flow of traffic. Everything passes through a firewall. It can block inbound and outbound traffic, allowing protection against evil.

**Host-based firewalls** are installed directly onto a single device like Windows Defender Firewall.

**Network-based firewalls** are dedicated appliances positioned at the edge of a network. All traffic entering or leaving the entire building must pass through it. This protects every device on a network.

Open-source firewalls exist. This does not make them any less secure, you just have to understand the source of that firewall.

## Stateful and Stateless

This concerns how deeply a firewall remembers what is happening.

**Stateless firewalls** inspect every individual incoming / outgoing packet in isolation, looking at things like source and destination IPs along with port number and checks these against a list of static rules (Access Control Lists, or ACLs). Packets are dropped or permitted based on this. The issue with this is that it does not remember past packets. If you request something from google, the firewall does not know it was *you*.

**Stateful firewalls** keep track of active network connections with a dynamic state table. When you perform a request to a server, the firewall logs that connection in the state table. When the server sends its respective data back, the firewall checks the table and recognizes it as a response to a conversation that already exists. The data can automatically pass.

### Extra note: Implicit Deny

Most firewalls / ACLs should have an invisible rule at the bottom stating that if traffic does not explicitly match any of the allowed rules, block it.

## Next-Gen Firewalls (NGFW) / Application-Aware

Traditional firewalls mainly look at layers 3 and 4 of the OSI model (IP addresses and port numbers). Modern attackers can bypass this by hiding malicious data in legit ports. Next-Gen or Application-Aware firewalls prevent this.

These look at the actual data itself as opposed to the port number. A traditional firewall might allow a malicious packet due to its port alone. An NGFW would flag it because of the data.

## Web Application Firewalls

While NGFW's sit inside a company network and protect internal users going out into the internet, **Web Application Firewall's** sit directly in front of a web server and protect it from attacks from the internet. It is specifically looking for application level atttacks like XSS or SQLi.
