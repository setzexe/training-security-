# Protecting Data

Protecting data is a primary job task. An organization will go out of business if it can not protect data. And this data is everywhere; a network, a storage device, a CPU, etc.

Encryptions, policies, and permissions are classic means of protecting data.

Hashing exists, although usually serves a different purpose of security. Encrypting data is two way and can be reversable. Hashing is moreso a fingerprint that represents the data itself, targetting integrity. These *shouldn't* have collisions, so they can be used as a digital signature / means of verification.

**Obfuscation** exists too. This is the concept of making something normally understandable and make it very difficult to understand. Perhaps this can be formatted so only the company itself even knows what it means, and psuedo code or data that works the exact same way is provided instead. If an attacker has no information about how a system works, they have less attacker information to work off of.

**Masking** is a type of obfuscation that hides some of the original data, like how only the last 4 credit card numbers are usually shown on a receipt. This primary protects PII and other sensitive data. This data may be viewable behind the scenes, this mainly just targets visibility to the user. Shuffling data, encrypting data, so on so forth exists as techniques.

**Tokenization** is similar to above; we replace sensitive data with a non-sensitive placeholder. This is actually extremely common with credit card processing. A token is used as a temporary placeholder for your financial information. The other side of the financial process usually has your information in some way or another, but its kept in a super protected and encrypted area. An attacker capturing these cards cannot use them later.

**Segmentation** can help protect large amounts of data. If all data was handled under one large database, a breach could mean all that data is leaked. This makes it very easy for the attacker to create catastrophic issues. Segmentation seperates the data and stores it into different locations. They would have to breach different databases and areas just to obtain different sets of data. Along with this, you can segment different data sets to have different security controls. More sensitive data = more security behind it.

**Permissions restrictions** are the most common form of protecting data. Based on a user's role or identity, they might be restricted to a set of policies or just general ruleset on what they can or can't do. These will vary from role to role and company to company.

## Geographic Restrictions

Network location can be used to restrict data usage or access. Identity can be based off of IP subnets, although this is difficult with mobile devices.

**Geolocation** is a better means. GPS is a primary one and is the most accurate. 802.11 works, not as accurate. IP address technically works but struggles the same issue as IP subnets.

**Geofencing** uses geolocation information to allow or restrict access when a user is in a certain location.
