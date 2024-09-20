# € Schneier 2015: Applied Cryptography: Chapter 1: Foundations
https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/08_chap01.html#chap01-sec001

## Terminology
- Cryptography = Art & science of keeping messages secure. 
- Cryptographers are cryptography professionals.
- Crpytanalysists break cyphertexts.
  - Cryptanalysis' point is to access encrypted messages without the key(s) 
  - Plaintext is encrypted into cyphertext which is decrpyted back into plaintext
- Cryptology encompasses the mathematics for cryptography & cryptanalysis.

- M is used to represent a binary data message to be encrpyted.
- When M is encrypted (E) to ciphertext (C), it can be represented with the equation E(M) = C
- The reverse function is D(C) = M, D = decryption.
- The process must be also valid for D(E(M)) = M, to ultimately reveal the  plaintext.

## AIN
- Authenticity
  - The receiver should be able to know who originally sent the message.
- Integrity
  - The receiver should be able to tell if the message has been tampered with.
- Nonrepudiation
  - The sender shouldn't be able to deny sending the message later on.

- These three bring similar trust to online communication as you can get in real life interactions.


## Algorithms and Keys
- A cryptographic algorithm is a mathematical function used for encryption and decryption
- A restricted algorithm bases the encryption security on the algorithms functionality itself.
- Modern algorithms use a key or keypair for encryption and decryption
  - The security lies solely in the keys which give far more flexibility in its usage.


- Symmetric algorithms utilise keys, but the key pairs are the same.
  - Cracking one key will give you a method for calculating the corresponding one as well.

- Public key algorithms or assymetric algorithms utilise two different keys.
  - A public key is used for encryption, and can feasibly be accesible to anyone.
  - A private key is the one sole key that can decrypt the message encrypted with the public key.


# Karvinen 2023: PGP - Send Encrypted and Signed Message - gpg
https://terokarvinen.com/2023/pgp-encrypt-sign-verify/

- PGP (Pretty Good Privacy) has an encryption tool called 'gpg'
  - 'gpg' is a way to manualy encrypt messages e.g. in the command line.
- To establish trust and a means for communication, both parties must give their public key to each other
  - The public keys will be used for encryption and authentication.
- "sudo apt-get install gpg micro psmisc" is ran to install 'gpg' on Linux.
- "gpg --gen-key" to generate a public key and a private key (secret key).
- For Alice to able to send a message to Tero, she need his public key which can be exported with: "gpg --export --armor --output tero.pub"
  - The key's output is shown in a block encapculated by "BEGIN PGP PUBLIC KEY BLOCK" and "END PGP PUBLIC KEY". The actual key shows in ASCII armor.
- Alice then needs to verify Tero's signature on the public key to ensure she's communicating with the right person.
  - After verification, Alice can mark Tero's key as trusted which will show as "Full".
- The same process is repeated with the roles reversed for Tero to verify it's Alice he's speaking with.
- 
  


  
