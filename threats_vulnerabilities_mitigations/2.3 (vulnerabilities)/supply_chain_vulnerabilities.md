# Supply Chain Vulnerabilities

The supply chain is the overall process of getting the raw materials to the consumer as a finished product. The hardware, software, development, shipping, handling, distributors, alot of factors come in to play.

This is **very vital** in cybersecurity. Attackers can infect any step along the way and future parts of the supply chain might never know since we typically trust our suppliers. One exploit can infect the entire chain. There is a lot at stake.

## Service Providers

Many modern organizations rely on service providers for things like payroll and finances, network, utility, cloud, a lot of important things. This means sensitive data is being sent through this third party service provider, adding anothing layer to the supply chain, thus adding another security layer. Ongoing and consistent security audits of providers is recommended.

To put in example how random but serious a vulnerability could be, consider the Target 2013 credit card incident. A malicious email was sent to a Heating and AC Firm in Pennsylvania. A random employee clicked it, and now private credentials from HVAC techs were stolen. It turns out this HVAC company does work for Target. It also turns out for some reason that Target's AC and their credit card system were on the same network with barely any bounds. So when the malicious people enter the HVAC network and see **40 million credit cards**, that is a bit of a big deal. All from an email and a terrible configuration on Target's end.

## Hardware Providers 

These are a similar concept but moreso for digital systems and traffic like ports, servers, routers, firewalls, etc. Can you ensure you can trust these? 

It is better to have a tight control on vendors or companies you work with. Better and smaller network is better than a bigger but worse one. Similarly, strict protocols and procedures are a must. When checking over this stuff, security should be part of the design process.
