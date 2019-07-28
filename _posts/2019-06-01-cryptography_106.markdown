---
layout: post
title: Key Based Cipher Types
categories: [Cryptography, DataSecurity]
tags: [Encryption, Decryption, Cipher, Cryptography]
---

There are 2 broad types of key based Ciphers - Symmetric and Asymmetric Key based ciphers

#### Symmetric/Private Key based
- The same secret key is used for both encryption and decryption
- Fast and efficient, the only pre-requisite is that the secret keys have to be exchanged between both the parties in a secure way (Asymmetric Key Ciphers can help with key exchange).
- There are 2 types of symmetric key algorithms
   - **Block Ciphers** encrypt data in blocks of bytes, padding the plain text to make it a multiple of the block size. Typical block sizes are 8 or 16 bytes. E.g. DES, AES
   - **Stream ciphers** encrypt data as a sequence of bytes/digits, one byte/digit at a time. E.g. RC4, A5


#### Asymmetric/Public Key based (eg. RSA)
- There is a mathematically linked key pair(private key and public key) where one  key cannot be derived from the other.
- Data encrypted using the public key can be decrypted only using the corresponding private key. 
- Data encrypted using the private key can be decrypted only using the corresponding public key.
- The public key is distributed and accessible by everyone and the private key is a closely guarded secret.
- Key generation, encryption and decryption are more computing intensive than symmetric cryptography in general.
- The data size should be less than the key size in Assymetric key cryptography
- This is mostly used for establishing a symmetric key, for digital signatures and for non-repudiation.