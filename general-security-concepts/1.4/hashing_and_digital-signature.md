# Hashes

A cryptographic hash is used to represent data as a short string of text. It is used for verification purposes-- you can not alter a fingerprint. These are sent with important data to verify integrity. If a hash is changed in the process, the data was tampered with.

These are one-way. You can not really take them back. You also can not access the original data if the only thing you are relying on is the hash itself. 

## Example

If we hash the string "Hi" we could get something like (via SHA256)

- 8dc67886b826c5141c4e04c48a723277
f84e2c34f93fa73ef6f4ce75a3770e2d
bd82eae9c23a123e0536b9de18f89201
7eefa9b3b242c2490984e5b944713f00
a95f9bbf67b8956076aa08a9385528bc
e00fd512ec8919d3c1766ab0600cc5f9
9d719f66e2c1f3f7c8836c62eb8616d5
68f181eb789a74ab3f7a81a2c891d8d1
58f9146c5f1e2b4d6b5f3909f3d959f9
d65d8ac999006e1dd3ed7713bd2c92d2

Now if we change it to "Hi!"

- 7bdfe8e18b8c84989e095de1560e8561
f779452321a73c27b0d281b55e04b690
b45fd62c6e2bf7420bf7abb17c63803f
65e9437aa1e9a33dfccdd64c788460a6
e1283bb461ba6e3187c49ac1bde1c9c4
c3600ec31f2fd87d25ae6b5f7d8059f0
38cc2aad907b4d755f7a45ddfa7704bb
0246f204909d8069382732772b143bfb
a75550fe5cd958a007b6da734fe8c8db
19e6ca475bb95bdc81239b3d6c5d6524

One change, entirely new hash.

## Collisions

We would like to avoid collisions, meaning hashes should always be unique. If two different sets of inputs create the same hash, that creates a collision (which inputs does the hash align with?) 

MD5 was a famous hashing system but has a major collision problem. It is not recommended for important stuff.

## Practical Hashing

It is ideal to verify a hash if you can. Many hashes will be available on a download page. If the hashes of the site and the file downloaded are the same, it can be assumed to be safe.

When storing passwords, hashes are the standard. Passwords are stored as salted hashes, not as plaintext. Salted just means that some extra information is added onto the hash to make it more distinctive. Whenever a password is inputted to authenticate a user, the plaintext password is hashed and compared to the database's stored hash value. The password itself is never saved.

# Digital Signatures (and Hashing)

Hashes are also used in the process of creating a digital signature. These hashes prove the integrity of data.

Digital signatures also prove the source of the message (authentication) and the hash makes sure the signature is not fake (non-repudiation).

Digital signatures are signed with a **private key**. The message does not need to be encrypted because no one else can sign or use the private key. Other parties simply verify it with the public key. If the public key does not align with the private key at the end of the process, something in the data changed.