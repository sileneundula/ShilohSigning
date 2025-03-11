# ShulginSigning

## Abstract

In terms of keeping data secure and tamper-resistant, there comes a time when a new solution must be made to address previous and future concerns in regards to cryptography. Many digital signature algorithms have been used to keep data protect but in this paper, we present ShulginSigning, a hybrid digital signature mechanism for signing data with high-integrity/security for the prolonged future that is post-quantum secure based on the hardness of hash function collision resistance using SPHINCS+ (SHAKE256), and classically secure based on elliptic curves using Ed25519 or the better version Ed448, as specified in RFC 8032. It promotes security by also making concerns regarding how it should be implemented, with an approach that allows cryptographic randomness to be generated for ecc keypairs on top of the determinstic approach called **hedged signatures**.

This paper is easy to understand and presents this signing scheme to be used in places where high-integrity is desired.

## 1. Introduction

Digital Signatures are a technique is cryptography that allow a user to sign data with a cryptographic signature using public key cryptography. These allow one to verify the validility of the data/message against that of the public key and signature to see if it is really valid.

## 2. ShulginSignatures

`ShulginSignatures` are a hybrid digital signature scheme that use post-quantum cryptography with classical cryptography to guarantee the integrity of the signature. They are based on strong security assumptions and use the following algorithms:

* SPHINCS+ (SHAKE256)
* Ed448 (SHAKE256) (with hedged signatures)

They are long-term solutions to signing in certain situations where high-integrity is needed. Both offer short public keys and private keys, while SPHINCS+ offers a large signature, that can be valid in certain situations. Due to the security assumptions behind SPHINCS+, we believe this will stand as a high-integrity signing mechanism.
