# Misconfiguration Vulnerabilities

Leaving doors open is very common in cybersecurity. Specifically, its very common to see data just in an open area on the internet. If attackers find this, thats bad. This is especially common on the cloud considering how not very up to date security is despite how popular cloud is nowadays.

## Unsecured admin accounts

These refer to accounts that can do most things on a computer. On your home network, its typically you (which if unsecured is a risk). In an organizational operating system, badly configured root / administration accounts might have intentionally easy to access passwords like 123456 so that organization can use them easily. These are way too easy to brute force. **It is important** to disable direct access to the root account. And similary, these root or administrative accounts should be protected heavily. There should not be a big scope of these for less attack way.


## Insecure protocols and ports

Protocols and ports are very common attack vectors. Some protocols are not up to date and secure despite still being used; Telnet, FTP, IMAP for example. The traffic sent with this stuff is usually sent in the open and is not encrypted. Ideally, using encrypted protocols should be a default. A firewall is essential too, but watching out for what information goes to what port is crucial. HTTPS shouldnt enter a SSH port. 

Verifying stuff with packet capturing is essential too to see exactly what you are receiving.