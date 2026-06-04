# Encrypting Data

If the goal is to protect data (at rest) on a storage device like SSD, hard drive, cloud, etc. The primary objective would be to encrypt that stored data.

In alot of cases, much important data is already encrypted. There are multiple full disks that are encrypted via BitLocker on Windows.

File encryption is also possible, it does not have to be a whole drive. EFS exists on windows, but third party utilities also exist.

## Database Encryption

Databases handle most data that is processed online. The stored data and data in transmission needs to be protected.

- Transparent Encryption
    - Encrypts all database information with a symmetric key
- Record-level Encryption
    - Encrypt individual columns and have a seperate symmetric key for each column 

## Transport Encryption

Protecting data traversing the network is also important; modern protocols like HTTPS exist to do exactly that.

VPNs (Virtual Private Network's) also do this. They encrypt all data over a network. VPN's are similar to firewalls in a sense that they are middlemans. This middleman bridge is why you can pretend like you are in different countries when using a VPN.

## Encryption Algorithms

There are many different ways to encrypt data. This means that for encryption <-> decryption to work, the same algorithm must be used. Both sides usually know this in advance, being hidden to this algorithm.

You do not have to default to one. Some will be more secure but slower, faster but less secure, some will be weaker, etc. There will be advantages and disadvantages to any algorithm.

## Cryptographic Keys

These algorithms are usually public. They are super complex, it would be awful for every organization to have to create their own.

The thing that actually makes these algorithm work for encryption and determine an output, is a key. It all revolves around this key. You are not going to much for data without a proper key, even if you know the algorithm.

## Key Lengths

Longer keys tend to be more secure. Attackers can try every possible key combination and naturally, lesser characters mean less combinations.

A common key method are symmetric keys with 128 bits or longer.

With asymmetric keys, the calculations are very complex with prime numbers. Keys can be much larger than symmetric; it is common to see up to 3072 bits or more.

## Key Stretching

A weak password can be made strong by simply doing multiple processes to it. Hash the password. Hash that hash. And so on. Brute forcing would require reverse hashing each of these hashings.