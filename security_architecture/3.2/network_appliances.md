# Network Appliances

Inside a network, it is usually alot easier to manage devices inside the same network. However, for security sake, it will not be as easy or accessible from an external device.

**Jump servers** help with this. This is a highly-secured device (hardened and monitored) inside of a network that is accessible from the outside. Usually, the jumping is a two-way process. The external device will have to connect to the jump server, in which they could then use SSH or a tunnel like VPN to access internal services or devices.

This makes a significity security risk if the jump server itself is compromised, as it is internal.

## Proxies

A proxy server sits between a conversation between two devices communicating from one another. The proxy itself receives requests from the user, and requests are sent from the proxy's behalf.

There are many uses for proxy servers. Many just use them for caching, access and response control, content scanning, URL filtering, etc.

There are two types of proxies:

- Transparent
  - Users do not realize a proxy is in place, as preconfiguration would not be needed.
- Explicit
  - Some proxies require an application to know how to use it.

Most proxy's that applications used by applications as **application proxies**. These understand how the application work and usually are configured to a set of protocols or rules. A proxy might only know HTTP, while some also know HTTPS, FTP, etc.

Proxies that control outbound traffic to the internet are **forward / internal proxies**. These are inside of the network. **Reverse proxies** are the opposite concept; internet users send requests to the proxy, which gets (if non-malicious) to the web server.

**Open proxies** exist and are uncontrolled typically, they might just be third party applications that anyone could use. This is a significant security concern and is not recommended. That third party could easily add some extra malicious information that would affect both devices.

## Load Balancers

These take incoming loads of traffic and balances it across different servers. A company with multiple web / database servers can use a load balancer to ensure no individual server is being overloaded, potentially causing DoS. But even if a server connected to a load balancer were to fail, the load balancer would recognize this lack of communication and would split any loads amongst the remaining servers. Users usually never even notice if this happens. Just like a proxy, these can do caching as well.

**Active/active load balancer** means all servers under a load balancer are active so that the load balancer itself can manage the load of each one. This also helps with TCP; the load balancer can keep an individual connection with a server instead of having to make multiple constantly. Similarly, **Active/passive load balancer** means some servers are active while others are on standby. If an active server fails, a standby server can take its place.

## Sensors and Collectors

Collectors aggregate information from network devices. These are typically integrated into switches, routers, firewalls, etc. These can compile statistics and make them available to those who want them.

Network sensors work much like their physical form; they sense for any intrusions or malicious activity and alert accordingly. These can be used in IPS's, firewall logs, web server access logs, etc.
