# Cloud Vulnerabilities

Cloud is relatively new but now extremely utilized in the modern world. Most organizations use cloud in one form or another. This cloud typically handles very sensitive information; attackers absolutely want this information. Unfortunately, at the current moment, many organizations do not end up using the right protections. 76% of organizations do not have proper central management security or authorization. Not only that but a lot of cloud code is unpatched.

## Attack the Service

If you have an application in a cloud, anyone around the world can attempt to connect to it. This also means anyone can try to take it down.

**DoS** is fundamental. This is based on a singular network and not really heavy traffic like **DDOS**, although that is possible too. **Authentication Bypass** is also common. Again, the security on alot of these systems are not too patched. **Traversing directories** or attempting to access further things within a server works. **Remote code execution** in particular takes heavy advantage of unpatched systems.

## Attack the Application

The cloud code is often unpatched or not that standard. Because cloud deals with extremely sensitive data, the fact that this stuff is relatively easy to exploit gives way more of an incentive to attack it.

Protecting against **XSS (Cross site scripting)** is essential. If scripts get in that affect how other users see the service, that could be catastrophic on the cloud. **Out of bounds write** too. This writes to unauthorized memory areas like the buffer or memory (buffer overflow is a type of out of bounds write). This can cause data corruption, improper script running, or crashing. The classic **SQL injection** is a huge risk too. Especially with the fact that a lot more sensitive data is stored.