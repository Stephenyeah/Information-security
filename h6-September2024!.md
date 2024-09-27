# x) Read or watch and summarize

## **Summary: Protocols and One-Way Hash Functions**

### **Protocols**
- A **protocol** is a set of steps followed by two or more people to complete a task.
- The steps must be done in a specific order, and everyone involved must know and agree to follow the steps.
- Protocols solve problems related to security, like protecting information or verifying identity.

### **One-Way Hash Functions**
- A **one-way hash function** scrambles data into a short, fixed-length value called a **hash**.
- Once the data is hashed, it can’t be turned back into the original form.
- Hash functions are used in **password security**, **digital signatures**, and **cryptocurrencies**.
  
- **How it works**:
  1. A user enters a password.
  2. The password is scrambled (hashed) by a server.
  3. The server checks if the hash matches the stored value to verify the user.

- **Types of hash methods**:
  - **Folding**: Splits the data, adds the parts, and uses a portion as the key.
  - **Digit Rearrangement**: Changes the order of digits and uses the result as the key.

# a) Install Hashcat.

### Cracking Passwords with Hashcat

**1. Install the apps**

![2024-09-27 14_38_29-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/e6087e85-fffc-4140-b7ba-4f7b0d3a9e18)

![2024-09-27 14_42_25-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/e918a8c2-9724-4db5-963d-56c278338e8d)

**2. So many words what a hug dictionary, and Identify Hash Type**

![2024-09-27 14_44_18-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/21e39817-7b1d-493b-9842-6bf8b57f5a33)

![2024-09-27 14_46_25-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/4ee3287b-ec2e-4872-8497-4fdb164cba46)

**3. Crack the Hash use the command below**

**Command Meaning**
  ```bash
  $ hashcat -m 0 '6b1628b016dff46e6fa35684be6acc96' rockyou.txt -o solved
  ```
- `hashcat`: The hash cracking program we just installed.
- `-m 0`: Specifies the type of the hash, identified using 'hashid' or 'hashcat --example-hashes'.
- `'6b1628b016dff46e6fa35684be6acc96'`: The hash we want to crack (enclosed in single quotes to handle any special characters).
- `-o solved`: Writes the cracked hash as plain text to a new file named "solved" in the working directory.

![2024-09-27 14_50_33-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/32cc3f97-328e-417d-9d88-b9f53f53e005)

![2024-09-27 14_52_01-Cracking Passwords with Hashcat](https://github.com/user-attachments/assets/95b5339f-4ca2-4feb-81df-b66bd1d4aaba)

**let's see the Hashcat say**

![2024-09-27 14_53_03-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/0d563f5c-e456-4b7e-8e1f-3371ddf1f17b)

![2024-09-27 14_54_14-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/4d67ecca-3822-4ec5-b1d3-aeb0868c7195)

# b) Crack this hash: d595b2086532422bbe654bc07ea030df

### Refer to the above operation

![2024-09-27 14_59_10-VirtualBoxVM](https://github.com/user-attachments/assets/51b9e6d0-de77-415f-a863-3cc097eeb042)


![2024-09-27 15_00_53-VirtualBoxVM](https://github.com/user-attachments/assets/f53f633d-6ed4-42f3-9c89-7479af682d5c)



- 

### References
https://www.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec003
https://www.okta.com/identity-101/one-way-hash-function-dynamic-algorithms/
