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


# a) Pretty Good indeed. Encrypt and decrypt a message with 'gnupg'.
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

# b) Password manage 

### 1. **Password Manager Selection**:  
A good password manager that meets the criteria (no cloud, free, and open-source) is **KeePassXC**. It is an offline, cross-platform, open-source password manager that stores passwords locally in an encrypted database.

### 2. **Installation of KeePassXC on Debian**:

To install **KeePassXC** on a Debian system:

1. **Update the package list**:
   ```bash
   sudo apt update
   ```

2. **Install KeePassXC**:
   ```bash
   sudo apt install keepassxc
   ```

3. **Launch KeePassXC**:
   After installation, you can launch it from the terminal by typing:
   ```bash
   keepassxc
   ```

### 3. **Demonstrate Usage of KeePassXC**:


#### Step 1: **Create a New Database**
- When you open KeePassXC, click on `New Database`.
- You’ll be prompted to create a **Master Password**. This is the only password you’ll need to remember, so make it strong but memorable. KeePassXC will use this to encrypt and protect the entire password database.
- 

![2024-09-22 01_48_06-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/305faa33-23f1-4f7b-8d9c-91706214adcd)

#### Step 2: **Store a Password**
- Once the database is created, you can start adding your passwords.
- Click on `Add New Entry`.
- Fill in the fields for the website, username, and password. You can use KeePassXC’s built-in password generator to create a strong password.
- Save the entry. Your password is now securely stored in your database.

![2024-09-22 02_01_58-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/ae1e1859-fcc6-4561-bf86-9ce1ba72297a)

#### Step 3: **Access a Stored Password**
- Open your KeePassXC database using your Master Password.
- Locate the entry for the service/website you need. Double-click the username or password field to copy it to the clipboard (it automatically clears the clipboard after a few seconds for security).

![2024-09-22 02_04_52-Information-security_h5-Uryyb,-Greb! md at study · Stephenyeah_Information-secur](https://github.com/user-attachments/assets/3d3ad224-4476-436e-902f-98bbb02630c9)

#### Step 4: **Export/Backup Database (Optional)**
- Regularly backup your password database by exporting it to a safe location (external drive or encrypted USB).

### 4. **Why a Password Manager is Needed**

A password manager helps mitigate various security risks:

- **Password Reuse**: Many users reuse the same password across multiple accounts. If one account gets compromised, attackers can easily gain access to others. A password manager encourages using unique passwords for every service.
  
- **Weak Passwords**: Users tend to create weak or simple passwords for the sake of memorization. KeePassXC can generate strong, random passwords, significantly reducing the risk of brute force attacks.

- **Phishing Attacks**: If you manually enter credentials for every website, phishing attacks (malicious websites mimicking legitimate ones) can trick you into entering your password. A password manager only autofills passwords on the correct domains, protecting you from phishing.

- **Password Theft**: Attackers can use methods like keylogging (recording your keystrokes) to steal passwords. With KeePassXC, passwords are securely stored and encrypted, and you only need to type the master password occasionally, reducing exposure.

- **Data Breaches**: If a service you use gets hacked, hackers may obtain passwords stored on their servers. With unique, strong passwords generated by a password manager, the impact of a single breach is isolated to one account.

### 5. **KeePassXC’s Protection Against Threats**:

- **Encryption**: The entire password database is encrypted using AES-256 encryption, which is one of the most secure encryption standards available.
  
- **Offline Operation**: KeePassXC operates entirely offline, which means your passwords are not stored on cloud services that could be hacked or leaked.

- **Secure Database Access**: The database is protected by a master password, which is the only password you need to remember.

KeePassXC effectively guards against **brute force attacks**, **password theft** (keyloggers, phishing), and **credential stuffing** by enforcing strong, unique passwords for every account and reducing password reuse.

