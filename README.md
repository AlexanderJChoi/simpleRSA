# RSA Encryption
This repository is to a simple implementation of the RSA algorithm. 

## Origin
The RSA Algorithm was first described by Ron Rivest, Adi Shamir, and Leonard Adleman while at MIT. It is used for secure data transmission.

## Overview
RSA employs a public-key/private-key system, in which each user has both a public key - which is accessible by any person - and a private key - which only the person knows. The public key is used to encrypt data before is is sent, and the private key is used to decrypt the information once it reaches its destination. 

## Setup

## Algorithm
Key generation takes two prime numbers as parameters; we will denote their product as n. It chooses the smallest integer (greater than 1) coprime to the totient of n to be the first part of the encryption key, e. It then computes the inverse of e mod the totient of n, and uses this as the first part of the private key, d. The full public and private keys are (e, n) and (d, n), respectively. The keys will be saved in a directory of the user's description.

Encryption takes a public key file and a plaintext file as parameters. Each character in the file will be converted into the decimal integer equivalent of its ASCII binary representation. Then, each value will be raised to the power of e mod n, and saved as whitespace separated values in a plaintext file. 

Decryption takes a private key file and a plaintext file as parameters. Each integer value in the file will be raised to the power of d mod n, and converted back from ASCII decimal representation to characters. These characters will be saved in a plaintext file.

## Proofs (For those of you which are so inclined)

