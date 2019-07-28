---
layout: post
title: Asymmetric Key Cipher
categories: [Cryptography, DataSecurity]
tags: [Encryption, Decryption, Cipher, Cryptography]
---

Asymmetric key ciphers use a mathematically linked key pair(public/private key) for encryption/decryption. Data encrypted using the public key can be decrypted only using the corresponding private key. Data encrypted using the private key can be decrypted only using the corresponding public key. The following sections should give you a logical view of how it works.

#### Asymmetric Cipher

Apart from the algorithm, the main difference between symmetric and asymmetric ciphers is in the key being used. Bob will encrypt the data using Alice’s public key so that only the owner of the corresponding private key (i.e. Alice) can decrypt it. Alice will have to ensure that the private key is stored securely.

![Asymmetric Cipher](/assets/images/AsymmetricKeyCipher01.png){:class="img-responsive"}

If Alice wants to send a response to Bob’s message, she will have to use Bob’s public key for encryption and Bob will use his private key for decryption. Alex can alter the message in transit and a mechanism is required to detect tampering. A mechanism is required to verify the sender identity as well.

#### Digital Signatures (Detect tampering)

Digital signatures are typically created by generating a hash of the message and then encrypting the hash with the private key of the sender.

![Asymmetric key for digital signatures](/assets/images/AsymmetricDS01.png){:class="img-responsive"}

- There are many other algorithms for signature creation and verification apart from RSA – Lamport, Rabin, GMR DSA etc. 
- Digital signatures help in detecting data tampering, similar to a MAC.
- Digital signatures also help to verify **sender identity and non-repudiation**. Only the owner of the private key can generate the signature thus proving the sender authenticity. If a message has been signed by a private key, the owner of the private key cannot claim that they did not sign the message while also claiming that their private key is secure.


#### Asymmetric Cipher with tamper Detection

Bob will encrypt the data using Alice's public key and generate a digital signature using his private key.

![Asymmetric cipher with tamper detection](/assets/images/AsymmetricKeyWithDS01.png){:class="img-responsive"}

Alice will use her private key to decrypt the message and Bob’s public key to verify the signature. If the digital signature is valid, Alice can ascertain that the message was not tampered and that it was indeed sent by Bob. Alex can view the digital signature and validate it with Bob's public key but he cannot interpret the data as he does not have access to Alice's private key.

**How can Alice be sure that Bob’s public key that has been published is actually the right key?**
