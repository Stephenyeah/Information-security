# Treat Model
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



## Did we do a good enough job?
Once you have identified the main threats to your privacy, you can start choosing solutions to protect yourself and your data.

**Step 1: Choose a Secure Email Provider**  
The first step to protecting your online privacy should be selecting a secure email provider. Almost all online accounts will require an email address, so it is essential to start with strong defenses.

**Step 2: Secure Your Logins**  
Protecting these accounts requires strong passwords and two-factor authentication (2FA).

By following these steps, you can begin to address your personal threat model. Privacy protection is a marathon, not a sprint, but you can pat yourself on the back because if you have created a secure email account and used a password manager to create strong and unique passwords for each account, you will significantly reduce the risk in the event of a data breach. Quickly changing passwords for specific services and staying alert to phishing emails will also make a big difference.

**Step 3: Don’t Stop Learning**  
Engaging with the broader privacy community through articles, forums, podcasts, and books is a great way to continue improving your privacy knowledge. By working together and sharing experiences, we can all enhance our online privacy and security.

Stay safe, and happy encrypting!





