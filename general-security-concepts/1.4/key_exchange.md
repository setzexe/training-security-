# Key Exchange

Keys are exchanged on a network so two devices can securely share scrambled / encrypted messages. For obvious reasons like snooping network traffic, the algorithm should **never** be sent over the web. 

Instead, there are two main methods of doing this that involve math or certificates.

## PKI (Public Key Infrastructure)

When under PKI, a computer has a public key that anyone can use. It also has a private key, although this is more like a lock. Only this private key can open whatever needed data.

Your computer uses the public key to lock a message. Since the server with the private keys has the private key to this public key, the server can open it.

## Diffie-Hellman Key Exchange

This is the default for insecure cases where there might not be some CA. Its quite complex with heavy math. This just creates a temporary key used for a single session.

Both devices agree on a set shared key that. Both devices will mix their own private key with this public key and send it to each other. At this stage, anyone sniffing traffic can see the public key and the 2 scrambled keys. They have no clue what exactly each side did to the public key.

Now both sides add their own private key and adds it the scrambled results and both sides reach the same key. It is never revealed across a medium, it is solved by each side.
