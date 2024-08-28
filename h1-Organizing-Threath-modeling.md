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

**Key Acronyms in the Field of Information Security**

**STRIDE:** The STRIDE threat model, introduced by Microsoft, is an acronym used to identify security threats. It stands for Spoofing, Tampering, Repudiation, Information Disclosure (i.e., data leakage), Denial of Service, and Elevation of Privilege. These threats are faced not only by enterprise security teams but also by everyday internet users.

  Examples of spoofing include the never-ending waves of spam emails, text messages from new numbers impersonating children, and bank deposit fraud—situations encountered by millions of people daily.

**OWASP:** The Open Web Application Security Project is a community of security experts and researchers who regularly publish articles, tools, and a top-ten list of security threats. The latest OWASP Top 10 list includes often overlooked dangers such as outdated software and hardware. This threat affects anyone using digital devices, especially since too many people choose to skip those annoying update notifications. OWASP has a high reputation in cybersecurity threat modeling, so their top ten list is worth reviewing.

**MITRE ATT&CK: ATT&CK** is an open knowledge base for security professionals and individuals. While many threats may not apply to the technologies you use in daily life, MITRE provides an excellent resource for accumulating security knowledge. For those of us looking to enhance online privacy, the "Reconnaissance and Collection" threat groups are particularly important.

**Security and Privacy: Two Sides of the Same Coin**

Alright, let me introduce a few more terms. Security researchers Marit Hansen, Meiko Jensen, and Marin Rost published a paper that extends the CIA triad, focusing on better privacy protection in threat modeling. They proposed the concepts of "Unlinkability," "Transparency," and "Intervenability."





