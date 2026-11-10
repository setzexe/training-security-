# Web Filtering

Web filtering controls which websites and web content users can reach. It's main goals are protecting organizational data (controlling sensitive material flowing in and out), blocking innaprorpiate content, and stopping malicious content.

## URL Scanning

The most basic approach is filtering by URL (Uniform Resource Locator). You keep an allow list of sites that are always permitted and a block list of sites that are never permitted.

URLs are usually done in categories because one organization can have dozens of URLs. URL filtering is limited on traditional firewalls. They work with NGFWs much better.

## Agent-based Filtering

With agent-based, client software is installed on each user's device and managed from a central console. Because the agent works locally, user's can rely on this wheerever. The downside is that updates must reach every device at around the same time.

## Proxies

A proxy sits between users and the internet. When a user makes a request, it goes through the proxy which can do several jobs before the proxy sends it to the server: caching, access control, content scanning, etc. It is basically a middle-man. Explicit proxies need configuration so the user's browser may be compatible with it. Transparent proxies are invisible to the user.

## Forward Proxy

This is for internal users going outbound the internet. It forwards traffic from your network to the outside. It usually protects / controls user access to the internet. 

A **reverse proxy** is this but the opposite side; the proxy sends the server requests coming in from the internet.

## Block Rules

Block rules can be built in two ways. The first is by specific URL. You can use '*' to say anything under a certain domain, like '*.cyberseverance.com'. The second is by content category. These services can filter based on category and have an action based on that category.

## Reputation

Reputation-based filtering decides based on how risky a site is believed to be. Sites with good reputation are allowed while bad reputation sites are blocked. Risk is usually rated on a 5-way scale: trustworthy, low risk, medium risk, suspicious, high risk.

You can have automated or manual reputation. Automated scans sites and scores automatically while manual reputations are inputted manually. Once reputations are added to the filter, it will use those for URL filtering.

## DNS Filtering

Before your computer connects to a website, it does a DNS lookup to turn the domain name into an IP address. DNS filtering looks at this moment and decides (based on public and commercial tools / resources) that if the site is malicious, it will not resolve it and give the user an IP address to access.
