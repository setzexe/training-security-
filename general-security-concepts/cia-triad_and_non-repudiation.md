# CIA Triad

The CIA Triad is how we remember the fundamentals of IT security. It is **not** related to the actual Central Intelligence Agency.

## The main security objectives

- Confidentiality 
    - Prevent disclosue of information to unauthorized individuals or systems
    - People's own data should be accessible only by them
    - **Encryption** encodes messages so only certain people can read it. Only certain people can decrypt it.
    - **Access controls** limits who can see certain things, including seeing other's information.
    - **Two-factor authentication** fits as well.

- Integrity
    - Messages / data can't be modified in the process. It is received exactly how it is sent.
    - **Hashing** verifies integrity in data via a hashed code.
    - **Digital signatures** is like a code sent that verifies the integrity of the data.
    - **Certificates** include a digital signature to verify sender (or any specified individual) as well.
    - **Non-repudiation** (more on that downwards) provides proof of integrity and can confirm 100% that the sender is legit.

- Availability
    - Systems and networks should be up and running.
    - Networks should be designed to always be running. If a system goes down, there should be compensating security measures.
    - Consistent **patching / updating** ensures availability does not decline.

# Non Repudiation

An important part of cryptography is the absolute assurance that data came from the sender. The sender cannot deny what was said; the data sent should be exactly how it is, by the person who made the data.

This is like a contract. It has our name with our procedures and confirms that it is authentic to me.

## Proof of Integrity

It is important to verify that data does not change. It has integrity. The data itself is accurate and consistent.

A **hash** is used in cryptography to achieve this. It is like a fingerprint for data. If the data changes, the hash changes. If the person changes, the fingerprint changes. Same logic. In the case of hashing, it is represented as a short string of random text.

Note that it does not necessarily associate data with an individual. Only if the data has changed. 

Example: Suppose you run a hash through a word document you find online.
    - It has 200 pages with thousands of words with a hash of 2x79qq...
    - Changing even one character in any of the thousands of words, saving it, and then rerunning the has, gives a different one.
    - A human probably could not spot the difference. But hashing ensures that yes, there is a difference

## Proof of Origin

This moreso focuses on authentication as opposed to integrity. This proves the source of a message.

**Digital signatures** are used for this. Using encryption, via the public-private key method, digital signatures are signed with a private key that only the sender knows. To verify that this private key is legit, the public key is used, as it is associated with the private key. 

## Creating & Verifying a Digital Signature (example)

- Alice's computer
    - Alice sends a text file saying "You're hired" to Bob.
    - She is prompted to create a digital signature. This runs a hashing algorithm. 
    - Alice will use her private key to encrypt that hash.
    - That encrypted hash is also sent with the plaintext hash as a digital signature. 
- Bob's laptop
    - Bob receives that exact message with the digital signature. 
    - He can use Alice's public key (available to anyone) to decrypt the digital signature.
    - At this point, he can hash the file to ensure that the hashes do match.

    