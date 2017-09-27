slide 0:
 Homo

slide 1:

## Homomorphic Encryption

- Homomorphic Encryption (HE) refers to a special type of encryption technique that allows for computations to be done on encrypted data, without requiring access to a secret (decryption) key. The results of the computations remain encrypted, and can be revealed only by the owner of the secret key.


slide 2:


## Motivation

- While traditional encryption schemes can be used to privately outsource data storage to the cloud, the data cannot be used for computations without first decrypting it, resulting in a huge loss of utility. For example, a secure cloud service may require a user to download their encrypted data, decrypt it locally, and perform necessary computations, instead of simply returning an encrypted result to the user.

- Homomorphic encryption solves precisely this problem, as it allows the cloud service to perform the computations while protecting the customer’s data with a state-of-the-art cryptographic security guarantee. The cloud only ever sees encrypted data, and only the customer can reveal the result of the computation.

- Consequently, people tend to remove useful documents from safe storage at the first chance they get. This exposes them to all the usual threats, and explains why so few cases of document theft involve safecracking. Typically the same principle holds for encryption. People decrypt their data so they can use it.


slide 3:

## previos techniques

-  In fact, cryptographers have put a lot of effort into removing the homomorphic properties from common public-key schemes like Elgamal and RSA. Without those protections, both schemes are homomorphic with respect to (modular) multiplication. This means you can multiply together any two Elgamal ciphertexts, and upon decryption you’ll find that the (single) resulting ciphertext now embeds the product of the two original plaintexts. Neat!

slide 4:

## Fully HomoMorphic Enryption vs Partial HomoMorphic Encryption vs SHE


----

# slides 5 -7 Mathematics


slides 5:

## key generation


slide 6:

## encryption
slide 7:

## decryption
slide 8:
 







slides misc:

## Can Homomorphic Encryption be Practical?

The prospect of outsourcing an increasing amount of data storage and management to cloud services raises many new privacy concerns for individuals and businesses alike. The privacy concerns can be satisfactorily addressed if users encrypt the data they send to the cloud. If the encryption scheme is homomorphic, the cloud can still perform meaningful computations on the data, even though it is encrypted.

In fact, we now know a number of constructions of fully homomorphic encryption schemes that allow arbitrary computation on encrypted data. In the last two years, solutions for fully homomorphic encryption schemes have been proposed and improved upon, but it is hard to ignore the elephant in the room, namely efficiency – can homomorphic encryption ever be efficient enough to be practical? Certainly, it seems that all known fully homomorphic encryption schemes have a long way to go before they can be used in practice. Given this state of affairs, our contribution is two-fold.

First, we exhibit a number of real-world applications, in the medical, financial, and the advertising domains, which require only that the encryption scheme is “somewhat” homomorphic. Somewhat homomorphic encryption schemes, which support a limited number of homomorphic operations, can be much faster, and more compact than fully homomorphic encryption schemes.

Secondly, we show a proof-of-concept implementation of the recent somewhat homomorphic encryption scheme of Brakerski and Vaikuntanathan, whose security relies on the “ring learning with errors” (Ring LWE) problem. The scheme is very efficient, and has reasonably short ciphertexts. Our unoptimized implementation in magma enjoys comparable efficiency to even optimized pairing-based schemes with the same level of security and homomorphic capacity. We also show a number of application-specific optimizations to the encryption scheme, most notably the ability to efficiently convert between different message encodings in a ciphertext.



slide n-2:
## Application
- Banking
- Voting
- Cloud
 
> slides n-2 to n +1 contains about applications
 

slide n+2:

## libraries

# phe

- A Python 3 library for Partially Homomorphic Encryption using the Paillier crypto system.

The homomorphic properties of the Paillier crypto system are:

Encrypted numbers can be multiplied by a non encrypted scalar.
Encrypted numbers can be added together.
Encrypted numbers can be added to non encrypted scalars.


## Seal

Simple Encrypted Arithmetic Library – SEAL is an easy-to-use homomorphic encryption library, developed by researchers in the Cryptography Research Group at Microsoft Research. SEAL is written in C++11, and contains .NET wrappers for the public API. It has no external dependencies. SEAL uses the Microsoft Research License Agreement, and is free for research use.



slide n+3:
## Facts
- In 2009, however, IBM researcher Craig Gentry came up with the first fully homomorphic encryption scheme.
- take 100 trillion time to do Google Search at that time
 0
## Uses in Differenet fields Content
-it could make cloud computing a lot more secure

- Homomorphic encryption has some immediate practical applications. Consider the Paillier scheme that’s used in several electronic voting protocols. Paillier is homomorphic with respect to addition. Now imagine: each voter encrypts their their ballot as a number (0 or 1) and publishes it to the world. Anyone can now tally up the results into a final ciphertext, which makes it hard for a corrupt election judge to throw away legitimate votes. Decrypting the final ciphertext reveals only the total.*


slide n + 4 -> n +5:
## demo slides



