# Password Attacks

These are instances where passwords can be compromised, or just information regading passwords.

## Plaintext / unencrypted passwords

This is usually caused by an absolute lack of security concern. No encryption here, passwords are just in the clear. Thankfully, this is very rare.

**Do NOT do this.** Immediately use a different application if you learn the one you are using does this.

## Hashing a password

This what passwords should be stored as: a hash (a fingerprint). As mentioned in prior modules, collisions should not happen if inputs are different.

This is very common as you can not really recover the original message from a hash. The password is only verified because when you enter your password in a site, its converted to a hash and compared to the hashed password.

These hashing systems and hashing files will most likely be different from system and program.

## Spraying attack & brute forcing

**Brute forcing** is the concept of using a list of commonly used passwords, or passwords that could match the victim, and test them all at once. This is not as common nowadays as many validation systems have limits to how many passwords you can guess.

Brute forcing is much more common **offline**; they will obtain information regarding user's and password hashes and calculate a password hash that can be compared to the stored hash. This is not easy nor simple, but it it makes guessing a lot more educated.

**Spraying** is the opposite. It tries one (or a small set) of commonly used passwords on multiple accounts. If one of those accounts has access to something important, that still is a win to the attacker. This is a lot more safe than brute forcing; if a password fails, move on. No security will be set off.
 
