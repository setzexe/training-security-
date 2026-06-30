# Intrusion Prevention

**Intrusion Prevention Systems**, or **IPS**, watch network traffic. If it notices an intrusion, it can block it immediately. These intrusions usually are triggered due to known exploits against OSs, applications, etc. This also is triggered due to known attacks in general like buffer overflow, XSS, etc.

**IDSs** exist too **(Intrusion Detection System)**, but this only detect and alert. They do not prevent attacks themselves.

## Failure modes

Sometimes, devices or systems fail. We aim for 100% uptime, but that is not always realistic. So what happens to network traffic when that device or system fails?

**Fail-open** refers to traffic still being sent to the network, but the security is just down. **Fail-closed** means both security stuff is down and the connection to the network as a whole is down.

## Active Monitoring

We ideally want **fail-open** to be the case. This is why IPSs is very common; it is simply a security system streamlined between the internet and the core switch (what splits traffic between subnets). In this case, while the IPS is up, it will prevent common threats and attacks.

## Passive Monitoring

Some people might have a concern that the IPS might prevent too much. In this case, **passive monitoring** is also possible. A copy of the network traffic is examined by the IPS, as the main traffic gets sent like normal. The problem is that this would not prevent any legitimate threats. This makes passive monitoring moreso an IDS even tho it uses an IPS.