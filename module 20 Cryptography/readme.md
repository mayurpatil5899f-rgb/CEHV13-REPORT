
Module 20: Cryptography

1. Introduction to Cryptography

Cryptography = protecting data using mathematical algorithms.

Goals of cryptography (CIA Triad + Non-repudiation):

Confidentiality

Integrity

Availability

Authentication

Non-repudiation

2. Types of Cryptographic Algorithms
1. Symmetric Encryption

Uses one key for encryption & decryption.

Fast, used for bulk data.

Common algorithms:

AES (most widely used)

DES / 3DES

Blowfish / Twofish

2. Asymmetric Encryption

Uses public + private key pair.

Slow, used for secure key exchange.

Common algorithms:

RSA

ECC

Diffie–Hellman (DH)

ElGamal

3. Hashing Algorithms

One-way, irreversible functions.

Used for passwords & data integrity.

Common algorithms:

MD5 (insecure)

SHA-1 (insecure)

SHA-256 / SHA-512

HMAC

4. Cryptographic Attacks

Common attacks in CEH exam:

Brute force attack

Dictionary attack

Rainbow table attack

Collision attack (MD5/SHA-1)

Birthday attack

Man-in-the-middle attack (MITM)

Replay attack

Downgrade attack

Padding oracle attack

5. Public Key Infrastructure (PKI)

PKI enables secure communication using certificates.

Components

CA (Certificate Authority)

RA (Registration Authority)

CSR (Certificate Signing Request)

CRL (Certificate Revocation List)

OCSP (Online Certificate Status Protocol)

Certificate Types

Self-signed

Domain-validated

Extended Validation (EV)

6. SSL/TLS – Web Encryption

SSL/TLS secures communication between client & server.

TLS handshake uses asymmetric encryption for key exchange and symmetric for data.

Attack Examples

SSL Strip

POODLE attack

Heartbleed (OpenSSL vulnerability)

7. Wi-Fi Encryption Standards

WEP – Weak, easily cracked

WPA – Better but outdated

WPA2 – Strong, uses AES

WPA3 – Latest, more secure

8. Cryptography in Email Security
PGP / GPG

Provides encryption + digital signing.

S/MIME

Built-in secure email standard used by enterprises.

9. Cryptographic Tools (Used in CEH Labs & GitHub Reports)

OpenSSL – Key generation, certificates

GPG / PGP

Cryptool

HashCalc

Cain & Abel (password cracking)

John the Ripper

Hashcat

10. Blockchain Basics (Included in CEH v13 Module)

Distributed immutable ledger

Uses hashing + digital signatures

Blocks linked using hash pointers

11. Cryptography Best Practices

Use AES-256, SHA-256, RSA-2048 or higher

Implement TLS 1.2+

Rotate keys frequently

Use salted hashing for passwords

Enforce strong key management

Avoid MD5 & SHA-1

Use secure random number generators
