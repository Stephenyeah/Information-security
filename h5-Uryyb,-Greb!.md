# x) Read and summarize

## Schneier 2015: *Applied Cryptography: Chapter 1: Foundations*

- **Cryptography Basics**: Explains how cryptography secures communication by transforming data to protect it.
- **Encryption/Decryption**: Encryption scrambles data, and decryption turns it back to the original.
- **Types of Cryptography**:
  - **Symmetric**: Same key for both encryption and decryption.
  - **Asymmetric**: Uses two keys – one public (for encryption) and one private (for decryption).
- **Cryptographic Tools**: Talks about ciphers (ways to scramble data), hashes (data checksums), and random numbers.
- **Breaking Codes**: Introduces cryptanalysis – trying to break encrypted messages.
- **History**: Mentions early ciphers and modern ones like DES (Data Encryption Standard).

---

## Karvinen 2023: *PGP - Send Encrypted and Signed Message - gpg*

- **PGP/GPG Overview**: PGP/GPG tools are used to encrypt and sign messages, keeping them private and ensuring they come from the right person.
- **Keys**:
  - **Public Key**: Shared to encrypt messages.
  - **Private Key**: Kept secret to decrypt messages or sign them.
- **Encrypting a Message**: Use the recipient's public key to encrypt so only they can read it.
- **Signing a Message**: Use your private key to sign it, proving it’s really from you.
- **Command Examples**: Provides simple GPG commands for encryption, signing, and managing keys.
- **Key Management**: Reminds users to protect their private key and share public keys securely.

Both explain how to secure communication—Schneier focuses on the basics, and Karvinen explains how to use tools like PGP/GPG.


### Summary of Commands:

- **Generate key pair**:  
  `gpg --full-generate-key`
  
![2024-09-22 01_40_16-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/f80a0acd-a474-40c5-a964-c481cbe72ae3)

- **Export public key**:  
  `gpg --armor --export your.email@example.com > public_key.asc`

  ![2024-09-22 01_39_52-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/c4974544-8769-43e9-a891-0b373dfca46b)


- **Import public key**:  
  `gpg --import recipient_public_key.asc`


- **Encrypt a message**:  
  `gpg --encrypt --armor --recipient recipient.email@example.com message.txt`

  ![2024-09-22 01_39_15-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/780ee1a4-77f0-4814-9492-e4c068483886)


- **Decrypt a message**:  
  `gpg --decrypt message.txt.asc`

- **Sign a message**:  
  `gpg --sign --armor message.txt`

- **Encrypt and sign**:  
  `gpg --encrypt --sign --armor --recipient recipient.email@example.com message.txt`

    ![2024-09-22 01_38_55-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/d1feb01f-6c8e-4243-b701-9f5b26c6afea)

