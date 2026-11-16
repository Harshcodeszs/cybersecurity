# Module 1: Introduction to Cybersecurity
# Day 1: October 14,2026
---

## 1. Fundamental Definitions

| Term | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Cybersecurity** | The practice of ensuring confidentiality, integrity, and availability (CIA Triad) of information by protecting networks, devices, people, and data from unauthorized access or criminal exploitation. | Keeping your personal digital house locked and safe from sneaky bad guys. |
| **Threat Actor** | Any person or group who presents a security risk to an organization or system. | Anyone trying to break in or cause trouble in your digital playground. |
| **External Threat** | A security threat originating outside an organization's control (e.g., external hackers). | An unwanted intruder trying to break in through the outside fence. |
| **Internal Threat** | A security threat originating within an organization's control (e.g., employees, contractors). | Someone already invited inside the house who accidentally or intentionally breaks a rule. |

---

## 2. Social Engineering & Phishing

### Phishing Tactics (Psychological Tricks)
* **Urgency:** Creating a false sense of panic (*"Act now or lose access immediately!"*).
* **Fear:** Triggering anxiety (*"Your account has been locked due to illegal activity!"*).
* **Authority:** Impersonating a trusted figure (e.g., CEO, bank representative, manager).

### Phishing Indicators (Red Flags)
* **Technical Indicators (Definitive Signs):**
  * **Sender Email Domains:** Mismatched domains (e.g., `bank-support.co` instead of `bank.com`).
  * **Hyperlink Mismatches:** The visible text displays one address (e.g., `bank.com`), but hover text points to an entirely different site (e.g., `scam.net`).
* **Content Indicators (Suspicious Signs):**
  * Poor grammar, severe spelling errors, generic greetings (e.g., *"Dear Customer"*), or unusual requests (e.g., purchasing gift cards).

### Security Playbook
* **Playbook:** A step-by-step procedure and checklist detailing how security analysts detect, investigate, and mitigate specific security incidents.

---

## 3. Governance, Risk & Defense Concepts

| Term | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Compliance** | The process of adhering to internal standards and external regulations to avoid fines and security breaches. | Following your school or house rules so you don't get grounded or fined. |
| **Security Frameworks** | Guidelines used for building plans to mitigate risks and threats to data and privacy. | The master LEGO instruction manual showing how to build a sturdy fortress. |
| **Security Controls** | Safeguards designed to reduce specific security risks and build a strong security posture. | The individual locks, helmets, or deadbolts installed to block specific dangers. |
| **Security Posture** | An organization’s overall ability to defend critical assets and react to change. | Standing back to see how well-prepared and strong your treehouse fort is right now. |

---

## 4. Security Domains

| Security Domain | Definition | Everyday Analogy |
| :--- | :--- | :--- |
| **Network Security** | Protecting computers, servers, infrastructure, and devices within a local network from unauthorized access. | Building a heavy moat, gate, and drawbridge around your local castle. |
| **Cloud Security** | Ensuring assets, data, and infrastructure stored in remote data centers (e.g., AWS, Azure) are securely configured and protected. | Renting a high-tech safety deposit vault at a secure national bank building. |


# Day 2: October 14,2026

## 1. Transferable Soft Skills

| Skill | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Communication** | Clearly explaining technical threats and solutions to both technical experts and non-technical stakeholders to resolve issues quickly. | Being able to translate complex game tactics so both pro gamers and beginners understand the plan. |
| **Problem Solving** | Proactively identifying attack patterns and applying efficient solutions, recognizing that perfect fixes are rare and compromises are often necessary. | Figuring out how to patch a leak in a boat using whatever tools you have on hand before it sinks. |
| **Time Management** | Prioritizing urgent security alerts to minimize damage to critical assets and staying focused under pressure. | Being a firefighter who tackles the biggest fire first before checking smaller spots. |
| **Growth Mindset** | Embracing continuous learning as technology, attack methods, and security tools rapidly evolve. | Staying excited to learn new rules and strategy updates whenever your favorite video game gets a patch. |
| **Diverse Perspectives** | Valuing different viewpoints and collaborating with team members to discover better, multi-angle security solutions. | Assembling a superhero team where everyone brings a unique power to solve the puzzle together. |

---

## 2. Core Technical Skills & Tools

| Skill / Tool | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Programming Languages** | Writing code (e.g., Python, Bash) to automate tedious tasks, search through logs, and analyze threat patterns automatically. | Building a toy robot to sort all your LEGO bricks by color so you don't have to do it by hand. |
| **SIEM Tools** | Security Information and Event Management software that collects, correlates, and analyzes log data across an entire organization to spot anomalies. | A master control tower receiving live video feeds from every camera in the city to spot weird activity. |
| **Intrusion Detection Systems (IDS)** | Monitoring system and network activity for suspicious behavior, policy violations, or unauthorized access attempts. | A smart door sensor that beeps whenever someone opens a window or door without permission. |
| **Incident Response** | Following established playbooks and procedures to investigate, contain, and remediate active security threats (like malware infections). | The step-by-step drill a fire crew follows when an alarm trips in a school building. |

---

## 3. Data Privacy: PII vs. SPII

| Data Type | Definition | Examples | Handling Guidelines |
| :--- | :--- | :--- | :--- |
| **PII** *(Personally Identifiable Information)* | Any non-sensitive data point that can be used alone or combined to infer an individual's identity. | Full Name, Home Address, Email Address, Phone Number. | Standard internal protection; restricted to authorized personnel. |
| **SPII** *(Sensitive PII)* | A specific high-risk subset of PII that poses severe harm or identity theft if exposed. | Social Security Number (SSN), Biometric Data, Passport Number, Financial Records. | Stricter legal handling; requires high-level encryption at rest and in transit. |

---

## 4. Key Duties in Keeping an Organization Secure

- **Analytical Thinking:** Carefully evaluating network metrics, defining user access privileges, and identifying subtle anomalies to mitigate operational risk.
- **Cross-Team Collaboration:** Partnering with software engineering, IT, and business leadership during an active breach to isolate systems and restore safe operations.
- **Malware Prevention:** Installing, configuring, and updating endpoint defense software (AV/EDR) to proactively stop malicious code before execution.
- **Documentation & Reporting:** Creating formal incident reports and security audit documents detailing vulnerabilities, remediation steps, and system improvements.
- **Periodic Security Audits:** Conducting systematic reviews of organizational records and log archives using **SIEM tools** to uncover hidden vulnerabilities.

# Day 3: October 16, 2026
# Module 2: Cybersecurity Attacks, Malware & Social Engineering

---

## 1. Core Threat Definitions

| Term | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Cybersecurity Attack** | Any malicious attempt to disrupt, damage, steal, or gain unauthorized access to computer systems, networks, or data. | A sneaky ninja trying to pick the lock or break the windows of your clubhouse. |
| **Malware** | Software explicitly designed to harm devices, steal data, or exploit users. | A monster toy packed inside a box that wrecks your room the second you open it. |
| **Social Engineering** | Manipulation techniques that exploit human error, trust, or psychology to gain private information or access. | A smooth-talking trickster trading fake magical beans for your real video game items. |
| **Phishing** | The use of digital communications (email, chat) to trick individuals into revealing sensitive data or installing malware. | Leaving a fake treasure map in your mailbox that leads straight into a trap. |

---

## 2. Common Phishing Attacks

| Attack Type | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Business Email Compromise (BEC)** | An attack where a compromised or spoofed email address impersonates a known source to request financial actions or sensitive files. | A fake note written in your teacher's handwriting asking you to hand over all your candy stash keys. |
| **Spear Phishing** | A targeted phishing attack directed at a specific individual or small group using customized pretexting. | A prankster who studies your exact favorite hobbies to trick *only* you into trusting them. |
| **Whaling** | A specialized form of spear phishing specifically targeting high-level corporate executives or VIPs. | Trying to trick the king or queen of the castle instead of the regular guards. |
| **Vishing** | Voice phishing; using electronic phone communications or VoIP to impersonate trusted entities and steal data. | A scammer calling on the telephone pretending to be the bank manager asking for your secret password. |
| **Smishing** | SMS phishing; using text messaging to trick users into clicking malicious links or giving up private information. | A suspicious text message claiming you won a free gaming console if you click a shady link. |

---

## 3. Common Malware Attacks

| Malware Type | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Computer Virus** | Malicious code that interferes with operations and damages data. Requires a user action (like opening an infected file) to spread and attach itself to host programs. | A sneaky gremlin hiding in a wrapped present that only wakes up and breaks things when you open the box. |
| **Worms** | Self-replicating malware that duplicates and spreads across networks on its own without requiring user downloads or file execution. | A magical multiplying slime that crawls through the air vents to infect every computer in the house by itself. |
| **Ransomware** | Malware that encrypts an organization's critical data, locking users out until a financial ransom is paid to the attacker. | A villain putting a heavy digital padlock on your toy chest and demanding allowance money before handing over the key. |
| **Spyware** | Secretive software that monitors device activity, records keystrokes, and steals private logs, media, and location data without consent. | A tiny invisible spy camera hidden behind your bedroom poster watching everything you do. |

---

## 4. Common Social Engineering Attacks

| Attack Type | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Social Media Phishing** | Harvesting personal details, interests, and connections from public social media profiles to craft hyper-targeted attacks. | A thief reading your public diary on the front porch to learn your secrets before knocking on your door. |
| **Watering Hole Attack** | Compromising a specific website frequently visited by a target group to infect their devices when they browse the site. | Spreading sticky slime on the exact slide at the park that you and your friends play on every single day. |
| **USB Baiting** | Leaving a physical USB flash drive loaded with malware in a public or corporate space, hoping an employee will plug it in out of curiosity. | Dropping a mysterious USB drive labeled "Secret Loot" on the floor, hoping someone plugs it into their computer. |
| **Physical Social Engineering** | Impersonating an employee, vendor, or repair technician to bypass physical security controls and enter a restricted building. | Wearing a fake clipboard and hard hat to walk right past the security guard into a movie studio. |

---

## 5. Psychological Triggers in Social Engineering

Threat actors exploit human psychology using specific behavioral triggers:

* **Authority:** Impersonating powerful figures because people are conditioned to obey authority without questioning.
* **Intimidation:** Using bullying tactics, threats, and aggressive persuasion to force compliance.
* **Consensus / Social Proof:** Pretending others have already complied (*"Everyone else in your department already gave me access"*).
* **Scarcity:** Creating artificial limits or deadlines to induce panic (*"Only 2 spots left!"*).
* **Familiarity:** Establishing a friendly, casual connection to lower your guard over time.
* **Trust:** Building deep, long-term rapport or emotional relationships to exploit victims later.
* **Urgency:** Pressuring victims to act immediately without stopping to think or verify instructions.

# Day 4: October 17, 2026
# Module 2: CISSP Domains, Advanced Attacks & Threat Actor Types
---

## 1. The Eight CISSP Security Domains

| Domain | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Security and Risk Management** | Defines security goals, risk mitigation, compliance, business continuity, and legal regulations. | Sitting down with your club to write down the official bylaws and disaster backup plans. |
| **Asset Security** | Secures physical and digital assets, covering storage, maintenance, retention, and secure data destruction. | Keeping your prized trading cards in a locked box and shredding old secret drawings. |
| **Security Architecture and Engineering** | Optimizes data security by ensuring effective tools, systems, and engineering processes are in place. | Building an awesome treehouse fortress with solid wood walls, padlocks, and trapdoors. |
| **Communication and Network Security** | Manages and secures physical networks, cables, and wireless communications against eavesdropping. | Scrambling your walkie-talkie channel with a secret code so bullies can't listen in. |
| **Identity and Access Management (IAM)** | Ensures users follow established policies to control and manage physical spaces and logical assets/apps. | A club bouncer checking ID cards at the door so only official members get in. |
| **Security Assessment and Testing** | Conducting security control testing, security audits, and data analysis to monitor risks and vulnerabilities. | Shaking your treehouse door hard to see if it pops open before rivals try to break in. |
| **Security Operations** | Conducting security investigations, monitoring alerts, and implementing active preventative measures. | Sitting in the security control room watching camera feeds to stop intruders instantly. |
| **Software Development Security** | Uses secure coding practices and guidelines to create safe applications and services from the ground up. | Following strict safety rules when building a toy car so the wheels never fall off. |

---

## 2. Advanced Attack Vectors

| Attack Type | Professional Definition & Domain Mapping | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Adversarial Artificial Intelligence** | Manipulating AI and machine learning technologies to conduct automated attacks more efficiently. *(Maps to: Communication/Network Security & IAM)* | Teaching a robot guard dog how to pick its own master's locks. |
| **Supply-Chain Attack** | Targeting third-party software, hardware, or vendors to inject malware into a product before it reaches the final target. *(Maps to: Security & Risk Management, Architecture, Operations)* | Sneaking a tiny glitch into a factory-made toy box so it breaks right after you buy it. |
| **Cryptographic Attack** | Compromising encryption mechanisms that protect secure communications between senders and recipients. | Stealing the decoder ring that lets you read secret spy messages. |

---

## 3. Threat Actor Types & Motivations

| Threat Actor | Professional Definition | Primary Motivations / Goals |
| :--- | :--- | :--- |
| **Advanced Persistent Threats (APTs)** | Highly skilled, well-resourced threat actors who infiltrate networks and remain undetected for long periods. | Sabotaging critical infrastructure (power grids) or stealing intellectual property and trade secrets. |
| **Insider Threats** | Employees, contractors, or trusted individuals who abuse their authorized access to harm an organization. | Sabotage, corporate espionage, unauthorized data leaks, or financial corruption. |
| **Hacktivists** | Threat actors driven by political agendas, social causes, or ideology who disrupt digital tech. | Public demonstrations, propaganda campaigns, social change, or notoriety. |

---

## 4. Categories of Hackers

| Hacker Category | Professional Definition | Motivation & Role |
| :--- | :--- | :--- |
| **Authorized Hackers** (Ethical Hackers) | Security professionals who hack legally with explicit permission to evaluate organizational risk. | Safeguarding people and organizations by finding weak spots before bad actors do. |
| **Semi-Authorized Hackers** (Researchers) | Independent researchers who search for vulnerabilities and report them without exploiting them. | Discovering system flaws out of curiosity or to help patch public software. |
| **Unauthorized Hackers** (Unethical Hackers) | Malicious actors who break the law to gain unauthorized access to systems and data. | Stealing and selling confidential data or malware deployment for financial gain. |

# Day 5: October 21, 2026
# Module 3: Introduction to Security Frameworks, Controls & Compliance
---
## 1. Core Framework & Governance Definitions

| Term | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Security Frameworks** | Guidelines used for building plans to help mitigate risks and threats to data and privacy. | The master LEGO instruction manual showing how to build a fortress piece by piece. |
| **Security Life Cycle** | A constantly evolving, continuous set of policies, standards, and updates. | The ongoing cycle of updating your video game with new patches and security fixes. |
| **Security Controls** | Safeguards designed to reduce specific security risks and build a strong defense. | Putting a deadbolt on a door or wearing a bicycle helmet to block a specific danger. |
| **Compliance** | The process of adhering to internal standards and external laws or regulations. | Following your school or house rules so you don't get grounded or fined. |
| **Asset** | Any item, physical or digital, perceived as having value to an organization. | Your rarest trading cards, favorite toys, or secret piggy bank. |

---

## 2. Purpose & Components of Security Frameworks

### Purpose of Security Frameworks
* **Protecting PII:** Safeguarding Personally Identifiable Information from unauthorized eyes.
* **Securing Financial Information:** Ensuring money records and bank data stay secure.
* **Identifying Security Weaknesses:** Finding flaws before malicious threat actors exploit them.
* **Managing Organizational Risks:** Spotting and reducing potential business hazards.
* **Aligning Security with Business Goals:** Ensuring security rules help the organization grow safely.

### Components of Security Frameworks
1. **Identifying Security Goals:** Determining what needs protection and what success looks like.
2. **Setting Guidelines:** Establishing the step-by-step rules to achieve security goals.
3. **Implementing Processes:** Putting strong security tools and workflows into active practice.
4. **Monitoring & Communication:** Regularly reviewing results and sharing updates with the team.

---

## 3. The CIA Triad

| Pillar | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Confidentiality** | Ensuring only authorized users can access specific assets, files, or data. | Only sharing your secret clubhouse password with your best friend. |
| **Integrity** | Guaranteeing data is correct, authentic, reliable, and free from unauthorized tampering. | Making sure nobody scribbled or changed the score on your game board while you were away. |
| **Availability** | Ensuring data and systems are accessible to those who are authorized whenever they need them. | Making sure your toy box is unlocked and open whenever you want to play. |

---

## 4. Key Regulations, Standards & Frameworks

| Standard / Law | Sector / Scope | Core Purpose |
| :--- | :--- | :--- |
| **NIST CSF** *(Cybersecurity Framework)* | U.S. / Universal Standards | A voluntary framework of standards, guidelines, and best practices to manage cybersecurity risk. |
| **FERC-NERC** | Power & Electricity / North America | Regulations applying to organizations working with electricity and the North American power grid. |
| **FedRAMP** | U.S. Federal Government | Standardizes security assessment, authorization, and monitoring for cloud service providers. |
| **CIS Controls** | Universal Network Security | A prioritized set of guidelines and controls to safeguard systems and networks against cyber attacks. |
| **GDPR** | European Union (E.U.) | Protects E.U. residents' personal data and their strict right to privacy in and out of E.U. territory. |
| **PCI DSS** | International Financial Standard | Ensures organizations storing, processing, or transmitting credit card information do so securely. |
| **HIPAA** | U.S. Healthcare (Est. 1996) | Protects patients' health info from unauthorized sharing. Governed by **Privacy**, **Security**, and **Breach Notification** rules. |
| **ISO Standards** | International / Global Business | Establishes international standards for technology, manufacturing, and operational management. |
| **AICPA Standards** | U.S. Accounting & Auditing | Auditing and accounting standards developed to evaluate organizational controls and financial integrity. |

# Module 3: Security Ethics, Governance & Architecture
# Day 6: October 23, 2026
---

## 1. Security Ethics & Core Principles

* **Security Ethics:** Guidelines and moral principles for making appropriate, responsible, and professional decisions as a cybersecurity professional.

### Key Ethical Pillars
* **Confidentiality:** Respecting sensitive information and keeping private data protected from unauthorized disclosure.
* **Privacy Protection:** Ensuring individuals' personal details (PII/SPII) are handled with care and collected only with proper consent.
* **Law:** Adhering to all applicable local, national, and international laws, regulations, and industry standards.

---

## 2. Security Governance & Architecture Definitions

| Concept | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Security Architecture** | A security design composed of multiple integrated components (tools, hardware, software, and processes) used to protect an organization from threats. | The architectural layout of a fortress—combining walls, moats, watchtowers, and security doors into one strong system. |
| **Security Governance** | Operational practices, policies, and leadership controls that help support, define, and direct an organization's overall security efforts. | The principal and teachers setting the ground rules, schedules, and safety policies for the entire school. |
| **Security Frameworks** | Structured guidelines and standards used to build comprehensive security plans that mitigate risks to data and privacy. | The master LEGO blueprint showing step-by-step how to construct a sturdy, safe structure. |
| **Sensitive PII (SPII)** | A high-risk subset of Personally Identifiable Information that requires stricter handling guidelines due to potential severe harm if exposed. | The key to your secret diary or your Social Security card—items that need double locks and extra-special care. |


# Module 4: Cybersecurity Tools and programming languages
# Day 7: November 05, 2026
---

## 1. Common Cybersecurity Tools

| Tool / Concept | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **SIEM** *(Security Information and Event Management)* | An application that collects and analyzes log data (records of system events) to monitor critical activities and alert analysts to threats. | A master security control room with an automated computer screen that flashes red whenever a strange camera feed trips. |
| **Network Protocol Analyzer** *(Packet Sniffer)* | A tool designed to capture, record, and analyze data traffic passing through a network. | A cosmic net catching every little paper airplane flying across the playground to check what's written on them. |
| **Security Playbook** | A structured manual providing detailed operational instructions on how to handle specific security tasks or incidents. | The emergency instruction booklet hanging on the wall telling you exactly what steps to follow if the fire alarm goes off. |

---

## 2. Incident Response Playbook Guidelines

When responding to an active security incident or collecting digital evidence, analysts must strictly follow these protocols:

* **Chain of Custody:** The rigorous process of documenting who has possession, control, and custody of digital evidence throughout its lifecycle. Every time evidence is transferred, it must be officially logged.
  * *Kid Analogy:* Passing a heavy trophy around a room where everyone has to sign a guestbook the second they hold it, so everyone knows who had it last.
* **Protecting and Preserving Evidence:** Safely handling fragile and volatile digital data without altering or destroying it. This relies on the **Order of Volatility**, which defines the exact sequence in which data must be preserved—from most fragile (like RAM and active network connections) to most permanent (like hard drive storage).
  * *Kid Analogy:* Carefully scooping up melting ice cream with a special spoon in a spec


  # Module 4: Core Cybersecurity Knowledge, Tools & Portfolio

---

## 1. Operating Systems & Programming Languages

| Technology | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Linux** | An open-source operating system widely used for server administration, security analysis, and specialized tooling. | An open-source workshop where anyone can inspect, modify, and build their own custom tools. |
| **SQL** *(Structured Query Language)* | A programming language used to create, interact with, query, and manage relational databases. | Asking a super-smart librarian to pull a specific index card out of millions of filing cabinets instantly. |
| **Python** | A versatile programming language used to automate repetitive, time-consuming tasks with high accuracy. | Building an automated Lego machine to sort all your bricks while you go outside to play. |

---

## 2. Automation & Programming Concepts

* **Programming:** Creating a specific set of instructions for a computer to execute complex tasks automatically.
* **Automation:** Using technology to reduce manual human effort in repetitive workflows, which drastically lowers the risk of human error.
  * *Kid Analogy:* Setting up a toy conveyor belt so your blocks clean themselves up instead of putting them away one by one.

---

## 3. Defense Tools & Vulnerabilities

| Term | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Web Vulnerability** | A unique security flaw in a web application that attackers can exploit to gain unauthorized access or steal data. | A loose window latch on a treehouse that someone forgot to lock up. |
| **Antivirus Software** *(Anti-Malware)* | A security program used to scan memory, files, and system behavior to detect, prevent, and eliminate malware and viruses. | A guard dog trained to sniff out hidden monsters before they wake up. |
| **Intrusion Detection System (IDS)** | An application that monitors system and network traffic activity to alert security teams on possible unauthorized intrusions. | A smart tripwire bell that rings the second someone walks past the perimeter fence. |

---

## 4. Cryptography & Testing

| Concept | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Encoding** | Using a public conversion algorithm to transform data into another format so different systems can share information. | Translating English into Morse code using a public rulebook anyone can read. |
| **Encryption** | Converting readable data into a secure, scrambled format using a secret cryptographic key so only authorized users can read it. | Locking your secret diary inside a titanium box that only opens with your secret decoder ring. |
| **Penetration Testing** *(Pen Testing)* | Participating in a legal, simulated cyber attack to evaluate systems, networks, and applications for vulnerabilities before bad guys find them. | Hiring a friendly stunt crew to test your castle walls by trying to climb them so you can fix the weak spots. |

---

## 5. Cybersecurity Portfolio Outline

To showcase your technical expertise to future employers or collaborators, your portfolio should feature:

* **Professional Statement:** A concise summary of your background, technical skills (Linux, Python, SQL), security domains, and career objectives in cybersecurity.
* **Professional Exemplar:** Highlighted project modules (such as your Security Journal, incident response playbooks, or lab write-ups) demonstrating your hands-on problem-solving abilities.


## Quick Reference Glossary

| Term | Professional Definition | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **Antivirus Software** | A software program used to prevent, detect, and eliminate malware and viruses. | A guard dog trained to sniff out hidden monsters before they wake up. |
| **Database** | An organized collection of information or structured data stored electronically. | A massive digital filing cabinet with labeled folders for easy searching. |
| **Data Point** | A single, specific piece of information or recorded fact. | One single LEGO brick out of a massive bucket. |
| **Intrusion Detection System (IDS)** | An application that monitors system activity and alerts security teams on possible intrusions. | A smart tripwire bell that rings the second someone walks past the perimeter fence. |
| **Linux** | An open-source operating system widely used for server administration and security tooling. | An open-source workshop where anyone can inspect, modify, and build their own custom tools. |
| **Log** | A chronological record or audit trail of events that occur within an organization’s systems. | A CCTV guestbook tracking every person who enters or leaves a building. |
| **Network Protocol Analyzer** *(Packet Sniffer)* | A tool designed to capture and analyze data traffic passing within a network. | A cosmic net catching every paper airplane flying across the playground to read what's on them. |
| **Order of Volatility** | A strict sequence outlining the exact order in which digital data must be preserved—from most fragile to most permanent. | Scooping up melting ice cream with a special spoon in a specific order before it disappears. |
| **Programming** | A process used to create a specific set of instructions for a computer to execute tasks automatically. | Writing a detailed recipe for a robot baker so it can make cookies by itself. |
| **Protecting and Preserving Evidence** | The specialized process of properly handling fragile and volatile digital evidence without tampering or data loss. | Handling a delicate fossil with soft brushes and special containers so it doesn't crumble. |
| **SIEM** *(Security Information and Event Management)* | An application that collects and analyzes log data to monitor critical activities and alert analysts to threats. | A master control tower receiving live feeds from every camera in the city to spot weird activity. |
| **SQL** *(Structured Query Language)* | A query language used to create, interact with, and request information from a relational database. | Asking a super-smart librarian to pull a specific index card out of millions of files instantly. |
