# Public Key Infrastructure

This is broad, but usually refers to the policies, procedures, hardware, software, and people related to digital certificates. Specifically; creating, distributing, managing, storing, and revoking. This typically involves alot of planning and preparations to make this whole system work the way an organization might what it to.

This also involves binding public keys to people or devices via the certificate authority, which also handles digital certificates. 

We will go about some main forms of encryption before Public Key.

## Symmetric Encryption 

There is a single shared key between encryption and decryption. This makes it very fast. It also makes it challenging to distribute as it does not scale well. 

For this specific type, there is a shared key algorithm between both sides that they use for this key.

This is typically used with asymmetric encryption due to its speed.

## Asymmetric Encryption

This utilizes public key cryptography. There are two related keys. A public key given by a CA, and a **private key**. Only one device should have access to this. The public key is seen by anyone.

**The private key is the only key that can decrypt any data encrypted with the public key.** The math and encryption process is insane with these keys. Even if you know the public key, you will never reverse engineer to get the private key.

Both the private key and public key are built at the same time, typically with a lot of math and large numbers and randomization. 

Large random number --> key generation program --> a public & private key pair

Everyone can have the public key. Only the creator of the key has access to the private.

## Key Escrow

In organizations or systems that involve tons of private keys, there typically is a 3rd party organization that handles it so that, that organization can keep these key's maintained. But another main reason is to be able to decrypt any data needed for a company. Under suspicious use, or the need to access an employee's information for whatever reason. Perhaps they need assistence or they left the company and we need the encrypted resources.

While this is controversial, and arguably a big security factor of it's own, it has more good than bad.