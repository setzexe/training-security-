# Encryption Technologies

On modern motherboards exist a **TPM**, or **Trusted Platform Module**. This is a specification for cryptographic functions. Basically cryptography hardware on a device. If you wanna do anything cryptographic like keys or random numbers, you use the TPM.

The memory is also persistent. Unique keys are burned in during manufacturing. The memory is also versatile. You can store storage keys, BitLocker keys, hardware configuration information, etc.

The TPM is password protected and has restrictions which prevent brute force or dictionary attacks.

## Large Scale Systems

In large environments, **HSM (Hardware Security Module)** is used. It can be seen like a huge storage and security system, like a physical box, that securly stores thousands of cryptographic keys. This includes key backups as well.

It is not what does the actual encryption. It is recommended to have a different hardware device or plug in card that handles this stuff.

## Key Management System

There are alot of services out there for key management. On premises, cloud, etc. Many different keys for many different services. These are managed from a centralized manager, often provided as third-party software. Encryption keys are seperated from the data.

From this one console, you can log keys and use, associate keys with users, create keys for specific services, rotate keys, etc.

## Security Enclave

These systems usually are seperate from the data itself. The private data that is important is typically only closest to us, like our phone.

Devices have a protected area for private data that is usually referred to as a **Security Enclave**. It is typically implemented as a hardware processor but is isolated from the main processor. As devices vary, the technology and names used for the security enclave can vary.

These provide extensive security features. It has its own boot ROM that monitors its own boot system, it can provide real time encryption, and much more.