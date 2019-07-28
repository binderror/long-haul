---
layout: post
title: Symmetric v/s Asymmetric Cipher
categories: [Cryptography, DataSecurity]
tags: [Encryption, Decryption, Cipher, Cryptography]
---

There are pros and cons with each key cipher type and so we cannot just choose to use one type over another.

#### Disadvantages of Symmetric Ciphers
- Symmetric ciphers expect both the communicating parties to share a secret key ahead of securely transmitting data. It is not very easy to securely share a secret key over an unsecured network. 
- Symmetric ciphers do not provide a mechanism for identifying the communicating parties.

#### Disadvantages of Asymmetric Ciphers
- Asymmetric ciphers require lot more computing power than symmetric ciphers and so can be a significant overhead.
- It is difficult to use asymmetric ciphers for huge data volumes as the data has to be smaller than the key size. However, we can definitely split the data into blocks and secure each block using an asymmetric cipher.
- For practical purposes, we need to use a combination of symmetric and asymmetric ciphers and this is known as a Hybrid Crypto System.

#### Hybrid Crypto System

Hybrid Crypto systems combine the efficiency of a symmetric key system with the features of an asymmetric key system.
- Generates a random secret key for symmetric cipher usage
- Uses an asymmetric key system for sharing the secret key between the communicating parties.
- Uses the shared secret key to encrypt/decrypt the actual data that needs to be transferred securely.

![Hybrid Crypto System](/assets/images/HybridCryptoSystem01.png){:class="img-responsive"}
