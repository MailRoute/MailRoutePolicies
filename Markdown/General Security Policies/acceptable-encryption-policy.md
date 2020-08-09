# Acceptable Encryption Policy

**Last Update Status:** *Updated August 2020*

## Overview

See Purpose.

## Purpose

The purpose of this policy is to provide guidance that limits the use of
encryption to those algorithms that have received substantial public
review and have been proven to work effectively. Additionally, this
policy provides direction to ensure that Federal regulations are
followed, and legal authority is granted for the dissemination and use
of encryption technologies outside of the United States.

## Scope

This policy applies to all MailRoute employees and affiliates.

## Policy

1.  **Algorithm Requirements**

    1.  Ciphers in use must meet or exceed the set defined as
            \"AES-compatible\" or \"partially AES-compatible\" according
            to the [IETF/IRTF Cipher
            Catalog](http://tools.ietf.org/html/draft-irtf-cfrg-cipher-catalog-01#section-3.1),
            or the set defined for use in the United States [National
            Institute of Standards and Technology (NIST) publication
            FIPS
            140-2](http://csrc.nist.gov/groups/STM/cmvp/documents/140-1/1401val2010.htm),
            or any superseding documents according to the date of
            implementation. The use of the Advanced Encryption Standard
            (AES) is strongly recommended for symmetric encryption.

    1.  Algorithms in use must meet the standards defined for use in
            NIST publication [FIPS
            140-2](http://csrc.nist.gov/groups/STM/cmvp/documents/140-1/1401val2010.htm)
            or any superseding document, according to date of
            implementation. The use of the RSA and Elliptic Curve
            Cryptography (ECC) algorithms is strongly recommended for
            asymmetric encryption.

    1.  Signature Algorithms

        +---------------+----------------+-----------------------------------+
        | **Algorithm** | **Key Length** | **Additional Comment**            |
        |               |                |                                   |
        |               | **(min)**      |                                   |
        +===============+================+===================================+
        | ECDSA         | P-256          | Consider                          |
        |               |                | [RFC6090](htt                     |
        |               |                | ps://tools.ietf.org/html/rfc6090) |
        |               |                | to avoid patent infringement.     |
        +---------------+----------------+-----------------------------------+
        | RSA           | 2048           | Must use a secure padding scheme. |
        |               |                | [PKCS\#7 padding                  |
        |               |                | scheme](http://tools.i            |
        |               |                | etf.org/html/rfc3852#section-6.3) |
        |               |                | is recommended. Message hashing   |
        |               |                | required.                         |
        +---------------+----------------+-----------------------------------+
        | LDWM          | SHA256         | Refer to [LDWM Hash-based         |
        |               |                | Signatures                        |
        |               |                | Draft](http://tools.ietf.or       |
        |               |                | g/html/draft-mcgrew-hash-sigs-00) |
        +---------------+----------------+-----------------------------------+

1. **Hash Function Requirements**

    In general, MailRoute adheres to the [NIST Policy on Hash Functions](http://csrc.nist.gov/groups/ST/hash/policy.html).

1. **Key Agreement and Authentication**

    1.  Key exchanges must use one of the following cryptographic protocols: Diffie-Hellman, IKE, or Elliptic curve Diffie-Hellman (ECDH).

    1.  End points must be authenticated prior to the exchange or derivation of session keys.

    1.  Public keys used to establish trust must be authenticated prior to use. Examples of authentication include transmission via cryptographically signed message or manual verification of the public key hash.

    1.  All servers used for authentication (for example, RADIUS or TACACS) must have installed a valid certificate signed by a known trusted provider.

    1.  All servers and applications using SSL or TLS must have the certificates signed by a known, trusted provider. 

1.  **Key Generation**

    1.  Cryptographic keys must be generated and stored in a secure manner that prevents loss, theft, or compromise. 

    1.  Key generation must be seeded from an industry standard random number generator (RNG). For examples, see [NIST Annex C: Approved Random Number Generators for FIPS PUB 140-2](http://csrc.nist.gov/publications/fips/fips140-2/fips1402annexc.pdf). 

1.  **Policy Compliance**

    1.  Compliance Measurement

        The Infosec team will verify compliance to this policy through various
methods, including but not limited to, business tool reports, internal
and external audits, and feedback to the policy owner.

## Exceptions

Any exception to the policy must be approved by the Infosec team in
advance.

## Non-Compliance

An employee found to have violated this policy may be subject to
disciplinary action, up to and including termination of employment.

## Related Standards, Policies and Processes

[National Institute of Standards and Technology (NIST) publication FIPS
140-2](http://csrc.nist.gov/groups/STM/cmvp/documents/140-1/1401val2010.htm),

[NIST Policy on Hash
Functions](http://csrc.nist.gov/groups/ST/hash/policy.html)

## Definitions and Terms

The following definition and terms can be found in the SANS Glossary
located at:

https://www.sans.org/security-resources/glossary-of-terms/

-   Proprietary Encryption

## Revision History

August 2020 - Initial MailRoute Documentation