# Application Security

Development becomes a balance between time and quality. If there are deadlines to push out an application, quality might compromise a bit, and security might become a secondary or weak factor. This is why a real QA (Quality Assurance) process matters. If a vulnerability exists, someone will eventually find it. The goal would be to catch this vulnerability prior.

## Input Validation

The most important part of secure coding is input validation. Every place an application accepts data is a potential way in. Step one is to document every input method and learn what data it would process.

Actual inputs should be compared against expected inputs. If an input wants a phone number, it should only take numbers. Everything else should be rejected. This process is called **normalization**: putting data into a standard, expected format that the application uses.

Attackers might use tools called **fuzzers** to throw malformed input into an application to see what breaks.

## Secure Cookies

A cookie is a small piece of information the browser stores on your computer for a website. Cookies are used for tracking, personalization, and most importantly session management (how a site remembers you're logged into it). Cookies are not a risk of their own, but it becomes a risk if an unauthorized user gets their hands on another user's cookies.

Secure cookies have the secure attribute set, stating that these cookies should only be sent over HTTPS and not HTTP. Additionally, cookies should never even hold super sensitive information.

## SAST (Static Application Security Testing)

SAST means analyzing source code without running it. A static analyzer reads through code, flagging insecure patterns. It is ideal for checking things like buffer overflow and injection flaws because those are recognizable attack patterns.

These have limits, especially when it comes to authentication logic and insecure cryptography (SAST often does not know code context and might completely miss stuff like this) and also the fact they can throw out false positives. SAST should be accompanied with real human verification.

## Code Signing

Code signing helps answer two questions with an application: Has the code been modified since it was released? And did it really come from a trusted source?

Code signing is done through public keys and certificates. A trusted CA (Certificate Authority) signs the developer's public key, vouching for the developer. The developer then can sign code with their own private key. When a regular use checks this, the system checks the signature with the developer's public key. If the code was changed, the signature will not match and the user gets a warning.

The developer signs with the private key, everyone else verifies with a public key.

## Sandboxing

This means running applications in an isolated space away from other resources. If the application is compromised, it is less likely to grow large in scale.

This is very common. Virtual machines for whole operating systems, mobile device sandboxes, etc.

## Monitoring

Monitoring is essential because it gives real time information about how an application is being used. You can see legitimate data, potential threats, blocked attacks, etc. Similarly, audit logs are saved from monitoring and can be used for later investigation.

The concept of trying to find outliers from legitimate behavior in case of a threat is called anomaly detection.
