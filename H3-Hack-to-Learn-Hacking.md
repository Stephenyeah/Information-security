
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
  1. Open a terminal.
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

![2024-09-06 12_15_35-DebianZhenyu  Running  - Oracle VM VirtualBox](https://github.com/user-attachments/assets/0946679a-f62c-4a2b-9858-3227f72450f8)



---

### Bandit Level 1 → Level 2
- **Steps**:
  1. List the files in the home directory:
     ```bash
     ls
     ```
  2. Read the content of the file named `-`:
     ```bash
     cat ./-
     ```
  3. The file contains the password for Level 2.

![Screenshot 2024-09-05 221429](https://github.com/user-attachments/assets/8752d549-638c-4db2-93f2-c490f3324c88)
![Screenshot 2024-09-05 221741](https://github.com/user-attachments/assets/61f2eca4-964f-4897-9055-c4392a4d9a29)

---

### Bandit Level 2 → Level 3
- **Steps**:
  1. List the files in the home directory:
     ```bash
     ls -a
     ```
     This will show the files, including the one named with spaces in the filename.

  2. Display the content of the file using:
     ```bash
     cat spaces\ in\ this\ filename
     ```
     The backslashes (`\`) are used to escape the spaces in the filename.

  3. The file contains the password for Level 3.

![Screenshot 2024-09-05 222031](https://github.com/user-attachments/assets/cf1ba37b-2cc6-49be-9ab2-6a954621b60b)
![Screenshot 2024-09-05 222155](https://github.com/user-attachments/assets/224c48bd-f7f9-4af1-9144-c1b5dd03d071)


---

### Bandit Level 3 → Level 4
- **Steps**:
  1. Navigate to the `inhere` directory:
     ```bash
     cd inhere
     ```
  2. List all files, including hidden ones:
     ```bash
     ls -a
     ```
  3. Read the hidden file :
     ```bash
     cat ...Hiding-From-You
     ```
  4. The file contains the password for Level 4.

![Screenshot 2024-09-05 222958](https://github.com/user-attachments/assets/9e55e697-c1dd-4055-97ee-7dbe230ce0fa)
![Screenshot 2024-09-05 223019](https://github.com/user-attachments/assets/4f6db0ba-a578-46a6-9268-f7183e3ae7aa)

---

### Bandit Level 4 → Level 5
- **Steps**:
  1. Navigate to the `inhere` directory:
     ```bash
     cd inhere
     ```

![Screenshot 2024-09-05 234025](https://github.com/user-attachments/assets/53c595bb-f2da-4ab0-809c-39de4147853b)

  2. Use the `file` command to identify the human-readable file:
     ```bash
     file ./-file*
     ```
  3. Locate the file that is marked as ASCII text.
  4. Display the content of the human-readable file:
     ```bash
     cat <filename>
     ```
  5. The file contains the password for Level 5.

![Screenshot 2024-09-05 234042](https://github.com/user-attachments/assets/2895979b-4ccf-409d-9f60-cbccbc320527)

## Source

- **Wargame**: [OverTheWire - Bandit Wargame](https://overthewire.org/wargames/bandit/)

---

