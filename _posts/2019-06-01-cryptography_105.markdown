---
layout: post
title: Symmetric Key Cipher
categories: [Cryptography, DataSecurity]
tags: [Encryption, Decryption, Cipher, Cryptography]
---

Symmetric key ciphers use the same secret key for both encryption and decryption. The following sections should give you a logical view of how it works.

#### Symmetric Cipher

Bob wants to sent a confidential message to Alice over a network. They have securely shared a secret key with each other and will use the same key for encryption and decryption.

![Symmetric Cipher Image](/assets/images/SymmetricCipher01.png){:class="img-responsive"}

Alex is able to read the message within the network, but unable to interpret the data as he does not possess the shared secret key. However, he can alter the message in transit. How can Alice validate message integrity? MACs to the rescue

#### Message Authentication Codes (Detect Tampering)

Hash generation is one of the approaches to detect data tampering

![Symmetric MAC](/assets/images/SymmetricMAC01.png){:class="img-responsive"}

- **Note** Anyone can generate the hash with the message, as the function is public knowledge.
- Introduce the usage of a secret key in the function so that only parties with knowledge of the secret key can generate the hash. A hash generated with a secret key can be used as a message authentication code and prove data integrity.
- However, both the parties who have the shared key can create or verify the MAC. Hence this cannot be used for non-repudiation

#### Symmetric Cipher with tamper detection

Bob wants to sent a confidential message to Alice. They have securely shared a secret key with each other and will use the same key for encryption and decryption. Bob sends a Message Authentication Code along with the message so that Alice can detect tampering.

![Symmetric Cipher with tamper detection](/assets/images/SymmetricCipherWithMAC01.png){:class="img-responsive"}

Alex is able to read the message within the network, but unable to interpret the data as he does not possess the shared secret key. If Alex tampers the cipher data, he will be unable to generate the MAC for the changed data(as he does not possess the secret key) and so Alice is able to detect tampering. There are many approaches to make the MAC even more stronger. 