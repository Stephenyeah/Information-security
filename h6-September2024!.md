# x) Read or watch and summarize

## **Summary: Introduction to Protocols and One-Way Hash Functions**

### **Protocols**
- **Definition**: A protocol is a series of steps that involves two or more parties and is designed to achieve a specific task. 
  - The steps must be followed in a defined sequence, with each step completed before moving to the next.
  - At least two parties are required; a person alone cannot constitute a protocol.
  - The protocol must have a clear purpose or task to accomplish.

- **Characteristics of Protocols**:
  - All parties involved must know and agree on the steps of the protocol in advance.
  - The aim is to solve problems related to secrecy, authentication, integrity, and security (especially against dishonest actors).
  
### **One-Way Hash Functions**
- **Overview**: A one-way hash function is a cryptographic function that scrambles data to produce a hash value, making it unreadable without special keys. It is a form of one-way encryption.
  
- **Key Features**:
  - **Irreversible**: Once data is hashed, it cannot be decrypted back to the original form unless the algorithm and key are known.
  - **Short Output**: Hash values are usually shorter than the original data, commonly 128 bits or more, but are always unique to the input.
  - **Message Digest**: The result of the hash is called a message digest, and without knowing the algorithm, it’s virtually impossible to reverse the encryption.

- **How It Works**:
  1. A user sends information (e.g., password and ID) through a secure connection.
  2. The authentication server receives the data and finds the user's stored message digest.
  3. The server hashes the user's input and compares the result with the stored hash.
  4. If the hashes match, the user is authenticated.

- **Applications**:
  - Initially used in databases to quickly locate short strings of data.
  - Now used in encryption, digital signatures, and cryptocurrency (e.g., Bitcoin).

- **Types of Hash Algorithms**:
  1. **Folding**: Divides the hash value into parts, adds them together, and uses the last four digits as the key.
  2. **Digit Rearrangement**: Rearranges the order of digits and uses the remaining unchanged number as the key.

Hash functions are a critical tool in modern cryptography, ensuring data integrity and security in various applications.











### References

https://www.okta.com/identity-101/one-way-hash-function-dynamic-algorithms/
