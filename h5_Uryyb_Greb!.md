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
 

## Security of Algorithms
- Probable safety is attained if:
  - The encrypted information is worth less than it costs to break the encryption
  - Breaking encryption takes longer than the encrypted information needs to stay secret
  - More data is required to break a single key than you can attain from said key

- An algotithms complexity can be measured by its processing and data complexity along with storage requirements.


## Steganography
- Messages are hidden in a seemingly ordinary text or picture.
  - Classic spy tricks like invisible ink
  - Sligth changes of gradiation in image bytes

## Substitution Ciphers and Transposition Ciphers
- Susbtitution ciphers use single or groups of corresponding letters and numbers to create simple encryption.
- Transposition ciphers consist of the same plaintext characters in a different order or setting.

## Simple XOR
- XOR is a very simple yet highly used encryption method.
- Essentilly comparing two bits and returning 1 if only one of the compared is 1, and returning 0 if both are equal.

## One-Time Pads
- "The perfect encryption scheme"
  - A truly random set of key letters are used to encrypt each character of the plaintext
  - Encryption is modulo 26 of the key letter and plaintext character. E.g. O(15) + T(20) = 35 -> 35 - 26 = 9 -> I
  - After encryption the sender destroys the used pages / pad.
  - Receiver uses an identical pad / pages to decrypt, and destroys them as well.
- Downsides are attaining true randomness for key letters and never using the same key sequence again.


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

- Now both parties are able to send encrypted messages even on unsecure channels by signing the message with their private key. The recipient can decrypt the message using the public key they have verified.
  

# Pretty Good indeed
I used Homebrew on Mac OS terminal for a smoother and quicker experience.

- I had Homebrew installed already, but it can be installed by following the instructions here: https://docs.brew.sh/Installation
- First I installed 'gnupg' with the command "brew install gnupg"

After installation: 
  
![Screenshot 2024-09-21 at 13 29 57](https://github.com/user-attachments/assets/38833446-06eb-4ba5-af94-ac7aca507b92)

- Next I ran "gpg --full-generate-key" to create the keys. When prompted, I entered: 
  - Key type (1 - RSA)
  - Key size between 1024-4096, I chose 2048
  - Expiration date
  - My name & email
  - A comment
  - Confirmation
  - Passphrase
![Screenshot 2024-09-21 at 13 40 17](https://github.com/user-attachments/assets/1f7b11b4-13b7-4f04-a8fd-28642833546d)

- I created a text file with 'echo "Test secret message" > message.txt'
- I encrypted it with "gpg --encrypt --recipient bhj362@myy.haaga-helia.fi message.txt"
- And decprypted with "gpg --decrypt message.txt.gpg > decrypted_message.txt", which opened a window to input my passphrase:
![Screenshot 2024-09-21 at 13 59 28](https://github.com/user-attachments/assets/c5dd1e95-80ec-4404-b95d-1d1b61602cd6)


# Password Manager
I'm using Butterup password manager with local vault only. It has cloud capabilities, which I don't utilise. Buttercup has a desktop application where you can store passwords and files freely. 

![Screenshot 2024-09-21 at 15 00 32](https://github.com/user-attachments/assets/ef269c6c-18f7-44cd-aec9-f2613fe2b0b1)

You can add a browser extension for easy management and log ins.
![Screenshot 2024-09-21 at 15 01 44](https://github.com/user-attachments/assets/aecbeeb3-af89-437e-a7f0-cbb53f7f8803)

Password managers are an effective personal cyber security tools to protect against: 
- Phishing attacks
  - Websites won't automatically fill in log in credentials when opening the web page.
- Data breaches
  -  

