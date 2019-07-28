---
layout: post
title: HSM & Key Management
categories: [Cryptography, DataSecurity]
tags: [Encryption, Decryption, Cipher, Cryptography]
---

Secret keys should not be stored on servers, databases, file systems or in application software. They should also not be stored in memory on servers that contain other applications. Any secret key that is stored in a weak medium defeats its purpose. Organizations use HSMs to generate & store their secrets keys and for associated crypto processing.

HSM facts
- A computing appliance that can securely store keys and provide faster crypto processing.
- An HSM can generate cipher keys which can be used for encryption/decryption. 
- Each HSM stores the cipher keys encrypted using another secret key (Local Master Key, LMK) which is known only to the HSM.
- The local master key is created by the HSM and backed up into multiple smart cards during its configuration. The smart cards are held securely with the security team ensuring that not all cards are accessible to one individual.
- HSMs possess mechanisms to detect and alert tampering attempts. Some HSMs are also tamper resistant and they erase the LMK if tampered, thus rendering the HSM useless.
- Once an HSM has erased its LMK, the cipher keys in the HSM cannot be read as they are all encrypted using the LMK. The HSM can be brought back to use, by loading the LMK back into the device using the smart card backups.
- Can be connected to secure printers for printing auto-generated passwords, thus ensuring that the handling staff cannot see the generated passwords.
- They are also used as accelerators for SSL/any other cryptographic processing and can be clustered for high loads and availability.