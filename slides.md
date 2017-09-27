slide 1:

## Homomorphic Encryption

- Homomorphic Encryption (HE) refers to a special type of encryption technique that allows for computations to be done on encrypted data, without requiring access to a secret (decryption) key. The results of the computations remain encrypted, and can be revealed only by the owner of the secret key.




slide 2:


## Motivation

- While traditional encryption schemes can be used to privately outsource data storage to the cloud, the data cannot be used for computations without first decrypting it, resulting in a huge loss of utility. For example, a secure cloud service may require a user to download their encrypted data, decrypt it locally, and perform necessary computations, instead of simply returning an encrypted result to the user.

- Homomorphic encryption solves precisely this problem, as it allows the cloud service to perform the computations while protecting the customer’s data with a state-of-the-art cryptographic security guarantee. The cloud only ever sees encrypted data, and only the customer can reveal the result of the computation.

slide 3:

slide n-1:


## Seal

Simple Encrypted Arithmetic Library – SEAL is an easy-to-use homomorphic encryption library, developed by researchers in the Cryptography Research Group at Microsoft Research. SEAL is written in C++11, and contains .NET wrappers for the public API. It has no external dependencies. SEAL uses the Microsoft Research License Agreement, and is free for research use.



slide n:
## Facts
- In 2009, however, IBM researcher Craig Gentry came up with the first fully homomorphic encryption scheme.
- take 100 trillion time to do Google Search at that time
 0
## Uses in Differenet fields Content
-it could make cloud computing a lot more secure

- Homomorphic encryption has some immediate practical applications. Consider the Paillier scheme that’s used in several electronic voting protocols. Paillier is homomorphic with respect to addition. Now imagine: each voter encrypts their their ballot as a number (0 or 1) and publishes it to the world. Anyone can now tally up the results into a final ciphertext, which makes it hard for a corrupt election judge to throw away legitimate votes. Decrypting the final ciphertext reveals only the total.*




