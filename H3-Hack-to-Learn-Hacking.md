
# x. Summary of Presentation on I Was Almost a Cybercriminal - Sergey Ichtchenko


**Introduction:**
The speaker, a 21-year-old cybersecurity consultant and board member of Test Ser, introduces themselves and outlines their roles, focusing on their collaboration with Coar. Test Ser is a community promoting ethical hacking among young people, encouraging them to develop their skills legally.

**Test Ser Overview:**  
Test Ser is a community that supports young people interested in programming, hacking, and cybersecurity through events, projects, and ethical guidance on vulnerability reporting. It also runs initiatives like Cyber Crime Exit to explore the reasons behind youth cybercrime.

**Survey Insights:**  
Young people often enter cybersecurity through family influence, curiosity, and gaming, starting with activities like bypassing restrictions. These enthusiasts are diverse, breaking the stereotype of being "lonely nerds."

**Motivations for Cybercrime:**  
Youth cybercrime is driven by bad influences, a desire for attention, and fun, often fueled by peer pressure, the thrill of rule-breaking, and misunderstandings about the impact of their actions.

**Personal Story:**
This is the beginning of his hacking journey. He saw an advertisement for Linnanmäki and thought about whether he could get a free season pass by redeeming an activation code. With a solid programming background, he first downloaded the Linnanmäki app and discovered a JavaScript vulnerability in it. Instead of exploiting the vulnerability for personal gain, he reported it to the Linnanmäki company. As a reward, the company gave him two tickets, which made him very happy.

![Screensho](https://github.com/Stephenyeah/Information-security/blob/aa3b109a82ab6a02eb915f0ed40289e178bc801f/Image/h3/%E7%A6%8F%E6%98%95%E6%88%AA%E5%B1%8F20240906000724133.PNG)

![Screensho](https://github.com/Stephenyeah/Information-security/blob/aa3b109a82ab6a02eb915f0ed40289e178bc801f/Image/h3/%E7%A6%8F%E6%98%95%E6%88%AA%E5%B1%8F20240906000754036.PNG)

The most important part was that his parents praised his actions. Rather than criticizing him for engaging in hacking, they encouraged him. This positive reinforcement set him on the path of ethical hacking and inspired him to pursue cybersecurity with integrity.

**Good vs. Bad Interventions:**
Negative responses, such as punishment or legal threats, can drive young people further into cybercrime. Instead, positive reinforcement, support, and guidance can nurture their skills and direct them toward ethical paths.

**Advice for Parents and Corporations:**
Parents should recognize and cultivate their child's skills, finding constructive outlets like bug bounties or educational resources. Corporations should be welcoming to vulnerability reports, offer rewards, and provide contact points for ethical reporting.

**Support for Young People:**
Young people should seek communities like Test Ser or Next Gen Hack and access resources for learning, such as CTF competitions or online tutorials. Mental health support is also crucial, as many young hackers may struggle with personal challenges.

**Conclusion:**
The speaker emphasizes the importance of community and positive reinforcement in guiding young people's skills in cybersecurity. Supporting young hackers and providing clear pathways for ethical hacking can help prevent them from veering into cybercrime.
## source
Presentation: [I Was Almost a Cybercriminal by Sergey Ichtchenko](https://www.youtube.com/watch?v=Nh7OrFVyDo0).

# Summary of "Command Line Basics Revisited" by Tero Karvinen


### Overview: 

- The guide covers fundamental command-line skills with practical advice.

### Key Topics:

- Essential commands for directory navigation, file viewing, and file system management.
- Using SSH for remote access and secure file transfers.
- Guidelines on package management, including software installation and removal.


Source
Article: [Command Line Basics Revisited by Tero Karvinen](https://terokarvinen.com/2020/command-line-basics-revisited/)

# a) Bandit Oh-Five (Levels 0-4)


### Bandit Level 0
- **Steps**:
  1. Open a terminal from your computer could be anywhere is avilable to the internet. (Not windows CMD, some keys are different. Powershell is okay)
  2. Use the following SSH command to connect:
     ```bash
     ssh bandit0@bandit.labs.overthewire.org -p 2220
     ```
  3. Enter the password: `bandit0`.
     
![2024-09-06 12_12_55-VirtualBoxVM](https://github.com/user-attachments/assets/1d7b8443-469a-4fa6-8a7a-37e49f0a7bee)

---

### Bandit Level 0 → Level 1
- **Steps**:
  1. List the files in the home directory:
     ```bash
     ls
     ```
  2. Read the content of the file named `readme`:
     ```bash
     cat readme
     ```
  ![2024-09-06 12_13_55-VirtualBoxVM](https://github.com/user-attachments/assets/85a5c4cf-448f-413a-ac18-df564c6ef6a6)
  
  3. The file contains the password for Level 1.
  

  ![2024-09-06 12_12_55-VirtualBoxVM](https://github.com/user-attachments/assets/cfdde901-e5c9-4f9f-8f3f-d6aac505e277)


### tips

    - Use the password to login the Bandit1. (Ctrl+shift+C) and (Ctrl+shift+V) Maybe you can use for the copy and paste the password.
---

![2024-09-06 12_49_55-VirtualBoxVM](https://github.com/user-attachments/assets/f7d12ab9-b312-4555-99ea-864545e4385c)


![2024-09-06 12_21_47-VirtualBoxVM](https://github.com/user-attachments/assets/77a874b4-0379-4900-95a3-7e73412f1b23)

## I have past all the steps from lever0-4. It is not hard, If you have any question feel free to ask.

## Fast reach the lever 4.

---


![2024-09-06 12_24_34-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/a5269c78-6f68-4cbb-8486-9d7bb3eb8c16)


---

### Bandit Level 4 → Level 5
- **Steps**:
  1. Navigate to the `inhere` directory:
     ```bash
     cd inhere
     ```
  2. Use the `file` command to identify the human-readable file:
     ```bash
     file ./-fi*
     ```
     // You could understand * can be anything.
  3. Locate the file that is marked as ASCII text.
  4. Display the content of the human-readable file:
     ```bash
     cat <filename>
     ```
     ![2024-09-06 12_29_14-h3](https://github.com/user-attachments/assets/841f308f-9402-4c73-943f-031763b3ec8b)

  5. The file contains the password for Level 5.
     
![2024-09-06 12_52_03-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/17d85680-71e2-4f12-995b-ce0a81db8cda)
![2024-09-06 12_52_25-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/7b80d0ce-25bf-4a53-ae43-76c3acd17b86)

### Source

- **Wargame**: [**OverTheWire - Bandit Wargame**](https://overthewire.org/wargames/bandit/)

---
# b) Can't fish.

Using the ping command, I checked the network connection between my computer (named @miau) and two DNS servers: Cloudflare's (1.1.1.1) and Google's (8.8.8.8). The command sent echo requests using the Internet Control Message Protocol. Each response line showed that packets (64 bytes each) were successfully sent and received, including the sequence number (from 1 to 4), the time-to-live value, and the round-trip time in milliseconds. All eight packets were transmitted and received without any loss, confirming that my system is properly connected to these DNS servers.

![2024-09-06 14_27_51-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/bb927aba-0119-4a20-8e8f-2223680dc279)

![2024-09-06 14_27_29-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/d5a90b51-b67f-4c1b-ade5-110cb531d160)

### Now I try to dig something from the webname.

![2024-09-06 14_25_57-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/8ac7db66-2d2d-4f4b-987f-593c2a9bddd0)

![2024-09-06 14_26_36-Settings](https://github.com/user-attachments/assets/892aa76a-93ed-463b-b071-c6a21ac1c7d8)

## It is wired I can't see any in the NAT of VMWare.
**But I can see something in my local Ubuntu**

![2024-09-06 14_23_57-stephenyeah@LAPTOP-LKMBT68D_ ~](https://github.com/user-attachments/assets/e847926e-d3c0-4454-8e2e-0ebbda050c67)

**Let me try some other command**

![2024-09-06 14_25_18-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/2a58955a-d183-45ed-86ed-70da5dcf900d)

## Yes, I can see something. Yeah! At list I fished a shose.

# c) Local only.

![2024-09-06 14_43_35-VirtualBoxVM](https://github.com/user-attachments/assets/8ffdf077-401b-4991-a539-738ef9bb57a4)

![2024-09-06 14_44_09-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/5d426855-a898-41c5-802a-ec02f069fd73)

### Sources: Karvinen. 2024. https://terokarvinen.com/information-security/



