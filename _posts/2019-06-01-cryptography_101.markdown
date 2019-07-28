---
layout: post
title: SSL/TLS - a hybrid cryptosystem
categories: [Cryptography, DataSecurity]
tags: [Encryption, Decryption, Cipher, Cryptography]
---

SSL is used to secure network communication. It uses a hybrid cypto model leveraging symmetric and asymmetric ciphers.

SSL( Secure Sockets Layer) is the standard technology for securing data transmission between systems/users. It does so by making sure that any data transferred is encrypted. TLS (Transport Layer Security) is the latest and more secure version of SSL. HTTPS (Hyper Text Transfer Protocol Secure) is an extension of HTTP where the data is communicated over TLS.

The following diagram should give you a logical view of how the SSL handshake works.

![SSL handshake](/assets/images/SSL01.png){:class="img-responsive"}

SSL leverages PKI for operations. The server certificate in the diagram above is signed by a trusted Certifying authority. The client can trust the server certificate only if it can verify the signature (by the CA) on the server certificate using the CA public certificate. All CAs will publish their public key certificates and get them bundled with the operating systems(OS) so that their certificates are pre-trusted by the system. 

If a client receives a server certificate that is signed by a CA and if the CA cert is not included as part of the OS, it would not trust the CA and reject the SSL handshake. This is a familiar problem when we use a really old OS and try to connect to a server that has a certificate signed by a relatively new CA. 