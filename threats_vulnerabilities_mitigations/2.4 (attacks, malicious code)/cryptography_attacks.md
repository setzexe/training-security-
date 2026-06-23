# Cryptographic Attacks

When you encrypt data and send it to another user, how can you certain it will truly end up secure? Even if attackers do not have access to the key, they could always attempt to attack the safe; or in this case, the cryptography.

Cryptographic algorithms are often publically posted meaning that anyone can find vulnerabilities and choose to not use it. However, modern encryption (AES is the big one) is very protective and virtually impossible to break through. Instead, attackers will focus on *how* that cryptography is implemented.

## Birthday Attack

This is related to hash collisions but uses birthday analogy. If 21 people are in a room together, the odds of any of them having the same birthday as another student (ANY student with ANY other student) is 50%. Similarly, the larger amounts of things to hash, the higher chance of 2 of those things getting the same hash code.

Attackers can brute force these hashes and compare their results to real hashes. If they make stuff that can create the same hash, this means that people will trust anything this person sends as if they are the original person with the original hash.

This is not common and ideal; different text *should* create different text.

## Downgrade Attack & SSL Attack

As mentioned earlier, the implementation of cryptography is often where the attacks happen. Instead of attacking perfect encryption, maybe downgrade the victim's security. Perhaps make them use a weaker encryption algorithm, or no algorithm at all.

**SSL Stripping** is the big one. This combines an on-path (watches/hijacks data when its *on-path* to its victim. Man-in-the-middle) with a method of downgrading security. It is difficult to implement, but can be huge for tha attacker. You are sitting in the middle of the conversation and need to make the victim user send HTTP information as opposed to HTTPS information to the attacker.

Say there is a victim, a server, and an attacker. The victim wants to connect to the web server. The attacker is in the middle. The victim sends the web server an HTTP request instead of an HTTPS one, which gets intercepted on-path. Modern browsers usually redirect/guide you to an HTTPS version of the page due to encryption (the S in HTTPS), but you can bypass this. The middle man will bypass this, making it unknown to the victim that HTTPS was never turned on. Now when the web server gets information from the user, it goes to the attacker as plain.