# Threat Model
## Braiterman et al 2020: Threat modeling manifesto
**What is a Threat Model, and What is the Process of Threat Modeling?**

There are various methods, processes, and techniques for threat modeling, but they all share several common principles.

**Threat modeling is a structured process aimed at identifying security requirements, determining security threats and vulnerabilities, and quantifying the severity of these threats and vulnerabilities, so that preventive measures can be prioritized.**

The goal of threat modeling is to create a list that outlines the areas or services where you (or your system) are most vulnerable to attack, the risks associated with those areas being attacked, the actions you can take to mitigate those risks, and the priority order for reducing those risks. Regardless of the specific approach used, the outcome of this process is your threat model.

**Industry Standards**

In the field of cybersecurity, there is a lot of discussion about the CIA— not the one with suits and helicopters, but the CIA Triad. The CIA Triad is an acronym for the following concepts: Confidentiality, Integrity, and Availability.

For us, **confidentiality** means that our data is only accessible to authorized individuals. For privacy enthusiasts, this could mean just you, your friends, or your family.

**Integrity** refers to the completeness and accuracy of the data. It wouldn't be ideal if the data is secure, but when you need it, it's just a corrupted file.

**Availability** means that the secure system we're building or using must provide access to the data when we need it.

For example, I could store an encrypted copy of my favorite music on an external hard drive, lock it in a safe, and bury it in the backyard; it would certainly be confidential, and hopefully, the data wouldn't be lost, but it would definitely lack availability. When developing your own threat model, it is crucial to balance these three concepts. Your final model may lean more towards some of these concepts, and that's okay. What’s important is that you strive to build a personalized security model rather than adopting a “one-size-fits-all” approach.

When choosing which services to use to solve certain problems, these three characteristics should serve as guiding principles.

## Shostack 2022: Welcome to the Worlds Shortest Threat Modeling Course
**Key Acronyms in the Field of Information Security**

**STRIDE:** The STRIDE threat model, introduced by Microsoft, is an acronym used to identify security threats. It stands for Spoofing, Tampering, Repudiation, Information Disclosure (i.e., data leakage), Denial of Service, and Elevation of Privilege. These threats are faced not only by enterprise security teams but also by everyday internet users.

  Examples of spoofing include the never-ending waves of spam emails, text messages from new numbers impersonating children, and bank deposit fraud—situations encountered by millions of people daily.

##OWASP CheatSheets Series Team 2021: Threat Modeling Cheat Sheet

**OWASP:** The Open Web Application Security Project is a community of security experts and researchers who regularly publish articles, tools, and a top-ten list of security threats. The latest OWASP Top 10 list includes often overlooked dangers such as outdated software and hardware. This threat affects anyone using digital devices, especially since too many people choose to skip those annoying update notifications. OWASP has a high reputation in cybersecurity threat modeling, so their top ten list is worth reviewing.

**MITRE ATT&CK: ATT&CK** is an open knowledge base for security professionals and individuals. While many threats may not apply to the technologies you use in daily life, MITRE provides an excellent resource for accumulating security knowledge. For those of us looking to enhance online privacy, the "Reconnaissance and Collection" threat groups are particularly important.

## Infosec Scene: Darknet Diaries Podcast Episode Summary

# Episode 146: ANOM - Overview

## Key Points

### What is ANOM?
- ANOM was an encrypted messaging app used by criminals, who believed it was secure.
- In reality, the app was monitored by law enforcement.

### Operation Trojan Shield
- This was a global law enforcement operation that uncovered ANOM.
- Agencies involved included the FBI, Europol, and Australian Federal Police.
- The operation used ANOM to track criminal activities around the world.

### How ANOM Was Used
- Criminals used the app for secret communication.
- They were unaware that their messages were being intercepted by police.

### Results of the Operation
- Many arrests were made, and illegal items such as drugs and firearms were seized.
- The operation caused significant disruption to major crime networks.

### Challenges
- The operation highlighted the difficulties of monitoring encrypted communications.
- It raised issues about balancing privacy with security.

### Impact
- The case led to discussions about privacy, encryption, and law enforcement surveillance practices.


**Security and Privacy: Two Sides of the Same Coin**

Alright, let me introduce a few more terms. Security researchers Marit Hansen, Meiko Jensen, and Marin Rost published a paper that extends the CIA triad, focusing on better privacy protection in threat modeling. They proposed the concepts of "Unlinkability," "Transparency," and "Intervenability."

![The concept diagram](https://github.com/Stephenyeah/Information-security/blob/study/2024-08-28%2023_27_08-2024Tuta.png)

**Unlinkability** is defined as "the characteristic that privacy-related data cannot be linked across domains, which are constituted by a common purpose and context." This means it should be impossible to associate you as an individual with your online data.


**Transparency** refers to "the characteristic that all privacy-related data processing...can be understood and reconstructed at any time." This mainly means that end users have the right to know what is being done with their data. 

**Intervenability** is a service that allows "intervention in all ongoing or planned privacy-related data processing." This refers to giving users control over their own data. It stands in stark contrast to the invasive practices of big tech companies that abuse data access rights, such as Google's monopolization of the search business for profit and market control.

The text introduces the concept of the "Intrusion Kill Chain," a model adapted from military strategies for cybersecurity. This model outlines the steps an adversary takes to execute a cyberattack and provides a framework for defenders to counter these attacks effectively.

# Security Hygiene 

## For Everyone

- Use strong, unique passwords
- Enable two-factor authentication (2FA)
- Keep software up to date
- Be cautious with phishing
- Back up your data regularly
- Use a VPN on public Wi-Fi
- Practice safe browsing
- Limit data sharing
- Use antivirus and anti-malware software
- Secure your devices with passwords or biometric features
- Monitor account activity

## For Companies

- Conduct regular security audits
- Implement employee security training
- Enforce strong access controls
- Apply patches and updates promptly
- Monitor network traffic and logs
- Secure communication channels
- Develop an incident response plan
- Implement data encryption
- Conduct regular backups and disaster recovery drills


# Threat Model for TechnoServe Innovations

## Company Overview

**Company Name:** TechnoServe Innovations  
**Industry:** Technology and Software Development  
**Products:** Cloud-based project management tools, customer relationship management (CRM) systems, and data analytics solutions.  
**Key Business Requirement:** Deliver secure and reliable software solutions to clients to maintain customer trust and ensure continuous revenue.

---

## 1. What Are We Working On?

### Assets:
- **Customer Data:** Personal information, project details, and financial records.
- **Proprietary Software:** Source code and intellectual property.
- **Company Infrastructure:** Servers, databases, and network devices.
- **Employee Data:** Personal and employment information of staff.
- **Client Interaction Points:** Customer portals, support channels, and integration APIs.

### Prioritization:
- **Crown Jewel:** Customer Data
- **High Priority:** Proprietary Software
- **Medium Priority:** Company Infrastructure
- **Lower Priority:** Employee Data

### Security Supports Business:
- **Customer Trust:** Essential for business continuity and revenue.
- **Operational Integrity:** Ensures reliable service delivery.

### Customer Touchpoints:
- **Customer Portals**
- **Support Channels**
- **APIs**

### System Diagram:

+------------------+      +------------------+      +-------------------+      +-------------------+
| Customer Portals | ---> |   Web Servers    | ---> |    API Gateways   | ---> | Integration APIs  |
+------------------+      +------------------+      +-------------------+      +-------------------+
                               |                          |
                               v                          v
                      +------------------+      +-------------------+
                      | Application      | ---> | Internal Systems  |
                      | Servers          |      +-------------------+
                      +------------------+
                               |
                               v
                      +------------------+
                      |    Databases     |
                      +------------------+
                               |
                               v
                      +------------------+
                      |  Backup Systems  |
                      +------------------+

                               ^
                               |
                      +------------------+
                      |  Support Channels|
                      +------------------+



## 2. What Can Go Wrong?

### Threat Models Applied

#### STRIDE Model
- **Spoofing:** Unauthorized access to customer accounts.
- **Tampering:** Alteration of customer data or proprietary software.
- **Repudiation:** Denial of actions by users.
- **Information Disclosure:** Leakage of sensitive data.
- **Denial of Service (DoS):** Disruption of service.
- **Elevation of Privilege:** Unauthorized escalation of permissions.

#### Attack Trees
- **Goal:** Compromise Customer Data
  - **Branch 1:** Exploit Vulnerability in Web Server
    - Exploit outdated software
    - Use SQL Injection
  - **Branch 2:** Phishing Attack on Employees
    - Gain credentials
    - Access internal systems

#### CIA Triad
- **Confidentiality:** Data breaches exposing sensitive information.
- **Integrity:** Unauthorized changes to data or software.
- **Availability:** Service disruptions affecting client access.

### Identified Risks
- **High Risk:**
  - Data Breach via Web Server Exploit
  - Phishing Attack on Employees
- **Medium Risk:**
  - DoS Attack on Customer Portals
- **Lower Risk:**
  - Minor Software Bugs

### Targeted Threat Actors
- **Cybercriminal Groups**
- **Geopolitical Threats**

### COI (Capability, Opportunity, Intent)
- **Capability:** High technical skills of threat actors.
- **Opportunity:** Exploitable vulnerabilities.
- **Intent:** Financial gain or competitive advantage.

### Business Continuity
- **Risk of Service Disruption:** Must maintain customer trust and ensure high availability.

---

## 3. What Are We Going to Do About It?

### Mitigation Strategies

#### Reduce Attack Surface
- Regularly update and patch software.
- Implement strong access controls.

#### Limit Entry Points
- Use Web Application Firewalls (WAFs) and Intrusion Detection Systems (IDS).
- Secure APIs with proper authentication.

#### Mitigate
- Implement encryption for data at rest and in transit.
- Conduct regular security training.

#### Eliminate
- Remove unnecessary services and software.
- Disable outdated protocols.

#### Transfer
- Use cybersecurity insurance.
- Outsource non-core security functions.

#### Accept
- Acknowledge residual risks and manage them with controls.

---

## 4. Did We Do a Good Enough Job?

### Continuous Improvement
- **Security Audits:** Regular assessments of vulnerabilities.
- **Penetration Testing:** Simulate attacks to find weaknesses.
- **Assessments:** Ongoing risk evaluations.
- **Continuous Threat Modeling:** Update models based on new threats.

**Process:**
- Security is a continuous process, not a one-time task. Regular updates and refinements are essential.







