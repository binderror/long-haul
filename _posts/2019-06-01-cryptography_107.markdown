---
layout: post
title: Introduction to cryptography
categories: [Cryptography, DataSecurity]
tags: [Encryption, Decryption, Cipher, Cryptography]
---

Cryptography is the science of secret writing so that only the intended recipient can interpret it while others may be seeing it.

### Uses of cryptography

Cryptography can be used to implement the following principles of data security

- Confidentiality that guarantees data is only interpreted by intended recipients
- Integrity that ensures that the data is not altered without permission
- Authenticity that the data was indeed created by the rightful owner
- Non-repudiation that ensures that sender cannot deny the sending of the message

### Keywords used in cryptography


<dl>
  <dt><strong>Plain Text</strong></dt>
  <dd>The data in clear that needs to be secured.</dd>
 
  <dt><strong>Cipher</strong></dt>
  <dd>The algorithm pair that transforms the plain text into Cipher text and back. Cipher examples include DES, AES, RSA, RC4 etc.</dd>

  <dt><strong>Cipher Text</strong></dt>
  <dd>The output of running the cipher encryption algorithm on the plain text.</dd>

  <dt><strong>Encryption</strong></dt>
  <dd>The process of transforming plain text to cipher text using a cipher.</dd>

  <dt><strong>Decryption</strong></dt>
  <dd>The process of reversing the cipher text back to plain text using a cipher.</dd>

  <dt><strong>Hash function</strong></dt>
  <dd>A function used to map data of arbitrary size to data of fixed size, with slight differences in input data producing big differences in output data.</dd>

  <dt><strong>Cryptographic Hash function</strong></dt>
  <dd>A hash function which exhibits the following properties – message cannot be retrieved back from the hash value, difficult to find a similar message with the same hash value and difficult to find 2 messages with the same hash value.</dd>

  <dt><strong>MAC</strong></dt>
  <dd>A short piece of information used to verify a message and to provide integrity assurances on the message. The same key is used to create and validate the MAC.</dd>

  <dt><strong>Digital Signature</strong></dt>
  <dd>Similar to a MAC, but the difference is that it uses a public/private key pair. The private key is used to create the signature and the public key is used to validate the signature. This implies that anyone having access to the public key can verify the signature.</dd>

  <dt><strong>Cryptanalysis</strong></dt>
  <dd>The science of finding weaknesses or security holes in Ciphers.</dd>

  <dt><strong>HSM (Host/Hardware Security Module)</strong></dt>
  <dd>Secure Hardware used to store cryptographic keys. In high security systems, the cryptographic keys would never leave an HSM and the plain text of cipher is passed to the HSM for encryption/decryption. HSMs can prevent the exposure of keys even if adversaries get access to them.</dd>

</dl>

### Evolution of Cryptography

**Substitution based Cipher was the earliest approach and in use from the BC era.**

- Each character of the plain text is substituted by another character to form the cipher text. 
- The cipher  text is generated using codebooks or shifting or rotating alphabets. 
- The algorithm (& codebook) is the secret and anyone with knowledge of the algorithm can decrypt the cipher text to plain text. 
- Examples: Caesar substitution, Atbash substitution, ROT13

**Evolution of Key based Cipher in the 20th century**

- The plain text is run through an algorithm which uses secret keys to form the cipher text. 
- The cipher text is generated using secret keys and greater key size generally leads to stronger cipher strength. 
- The algorithm is public knowledge and the keys are closely guarded.
- Examples: Vigenere, DES, AES, RC4, RSA 