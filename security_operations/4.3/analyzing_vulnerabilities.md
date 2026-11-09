# Analyzing Vulnerabilities

Scanning and testing will give you a big list of security findings. The next step would be to look at this findings and make out the proper vulnerability readings. This deals with sorting out true readings from fake ones, looking at what matters most, how to fix them, etc.

## Dealing with False Information

There are two type of false results. A false positive is when a scanner reports a vulnerability that does not exists. A false alarm and usually a waste of time to chase.

The other one is a false negative; this is the dangerous one because it means the scanner is not detecting a vulnerability that actually exists. This typically happens because the scanner might not know what to look out for. This makes updating scanner signatures (the hash used to check code for vulnerabilities) very important.

## Prioritizing Vulnerabilities

Not every vulnerability should be prioritized for timesake. Some can't actually be exploited, and some are blocked by other security controls. Certain frameworks exist to rank vulnerabilities from severity, impact, and other factors like CVSS and CVE.

**CVSS (Common Vulnerability Scoring System)** gives each vulnerability a score from 0-10 based on severity. Modern models follow CVSS3.x, although CVSS2.0 can still be found online. 3.x goes as follows:

- 0.1 - 3.9 = Low
- 4.0 - 6.9 = Medium
- 7.0 - 8.9 = High
- 9.0 - 10.0 = Critical

**CVE (Common Vulnerabilities and Exposures)** is a list of publically known vulnerabilities that each get a unique ID like CVE-6769-42067. That ID lets everyone refer to the exact vulnerability. Most vulnerability scanners link its finding to specific IDs so you can look up each detail.

CVE is the tag of that vulnerability while CVSS scores it.

## Vulnerability Classification

Scanners look for a lot, but not everything. It depends on their signatures and what they know to look out for. Scans are grouped by what they target like (mobile) application, web application, or network scans.

## Exposure Factor

Exposure factor is the percentage of value or business activity you would lose if the vulnerability were exploited. It is a way to measure impact. A small DoS that slows down systems in half may have 50% exposure because the system still works, just slowly. Meanwhile, a buffer overflow that crashes an entire system would be 100% exposure.

## Environmental Variables

One thing that matters heavily with vulnerabilities is where that vulnerability is. Is it on an internal network or a public cloud? Is it on a development workstation or an employees personal computer? Is it on an isolated lab literally nothing could reach?

The things like the context of those systems matter to. Are they important systems? How many would be affected? A vulnerability that could destroy an old isolated Ubuntu server would be rendered useless on a modern Windows computer.

## Organizational Impact

Every organization weighs vulnerabilities differently, balancing how exploitable something might be and how much damage it actually could do. Two ideas tie together here.

First is risk tolerance, the amount of risk an organization is willing to accept. You can not remove all risk, so every organization decides what is acceptable. The second is timing of patches. Patching is ideal, but patching prior to testing is not effective. But testing also takes time, leaving the vulnerability exposed. Organizations need to find this balance.
