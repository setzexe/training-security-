# Certificates

Digital certificates act like a digital identification card. These are files that hold / bind both a public key and a digital signature. The ideal goal of this, and most of cybersecurity, is trust.

More can be added onto a digital security. PKI can use a Certificate Authority for additional trust. You do not necessarily need a CA to gain trust tho; there are some tools for trust in Windows Resource Manager, along with many 3rd party tools.

In a digital certificate, you will find stuff like serial number, public key, signature algorithm, name of the cert holder, anything useful. Every digital certificate is formatted is thee X.509 style.

## Root of Trust

Everything associated with IT security requires trust. But how do you trust something that has been unknown up to this point, with no relation to anything that has been done up to this point?

We usually rely on the **root of trust** for that. This is an inherently trusted component that exists within a system, like hardware, software, etc., that is regulated and made with the intent to form some trust. A certificate authority, security enclave, etc. 

## Certificate Authorities

Certificates signed by CA's can be used to verify a 3rd party site's legitimacy. If this is not easy to find, or it is unsure if there even is one, other open source tools exist that can scan a site for any problems as well.

Browsers come and learn about certificate authorities it can trust. There are many to choose from. If a site creates a certificate under one of these CA's, your computer from that point on will trust that site.

## Certificate Signing Request

To create a digital certificate for our server, a digital certificate would first be created with our public key along with relative organization information for application purposes. This is sent as a **Certificate Signing Request**. The CA validates this request by confirming the DNS emails and website ownerships, along with making sure the web server isn't malicious. If approved, they sign the certificate with their private key and send it back to you.

If you are on a private network where the only people using your network is people close to you (like a house), then you are your own CA and can rely on third party CA packages. This is needed also for medium - large organizations.

If we (the company) are the only one using this CA, no need to purchase trust for devices that already trust you, as long as all these devices have this CA.

## Wildcard Certificates

**SAN** (Subject Alternative Name) is an extension of X.509. If this exists, any domain under this name (if labeled like: *.ch. Note the asterisk) will have a digital certificate as long as one device holding all these names has a digital certificate.

## Key Revocation

Much like we can create certificates, we can remove certificates. Perhaps an attacker has access to them, or the devices / apps associated with them are defunct. But there are many different reasons that can change all the time.

The CA handles the revoking. You can have a folder just dedicated to revoked certificates. However, this can be ineffienct if clients need to actively see what is revoked. Instead, certificate holders cerify their own status via **Online Certificate Status Protocol**. This certificate status is handled on our web server and is "stapled" onto TLS handshakes to verify trust. The browser can check this information and is usually sent back via HTTP.

Do note that some browsers simply do not support OCSP.