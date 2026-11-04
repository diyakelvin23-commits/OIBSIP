# Social Engineering Attacks: Phishing, Pretexting and Baiting

**Author:** Diya Kelvin Powei  
**Track:** Cyber Security – Security Analyst  
**Task:** Task 5 – Research Report: Social Engineering Attacks

---

## 1. Introduction

Social engineering is a cybersecurity attack technique in which attackers manipulate people into revealing confidential information, performing unauthorised actions, or providing access to systems and networks.

Unlike attacks that rely mainly on technical vulnerabilities, social engineering exploits human behaviour, including trust, fear, curiosity, urgency, authority, and the desire to help others.

Social engineering is highly effective because even organisations with strong technical security controls can be compromised when employees are deceived into sharing credentials, opening malicious files, or approving fraudulent requests.

According to Verizon's 2024 Data Breach Investigations Report, 68% of breaches involved a non-malicious human element, such as an employee making an error or falling victim to social engineering.

This demonstrates why employee awareness and strong verification procedures are essential parts of cybersecurity.

## 2. Phishing

### Definition

Phishing is a social engineering attack in which criminals use fraudulent emails, messages, websites, or other communications to trick victims into revealing sensitive information, clicking malicious links, downloading malware, or providing access to accounts.

Attackers commonly impersonate trusted organisations, colleagues, financial institutions, or service providers.

### Types of phishing

**1. Spear phishing**

A targeted phishing attack directed at a specific individual or organisation. Attackers research their victims and use personalised information to make fraudulent messages appear legitimate.

**2. Whaling**

A form of spear phishing that specifically targets senior executives, company directors, and other high-value individuals.

**3. Vishing (Voice phishing)**

An attack conducted through telephone calls or voice communications. Attackers may impersonate bank employees, technical support personnel, or government officials to obtain confidential information.

**4. Smishing (SMS phishing)**

A phishing attack conducted through text messages. Victims may receive fraudulent delivery notifications, banking alerts, or account verification messages containing malicious links.

### How phishing works

1. **Reconnaissance:** The attacker gathers information about the target.
2. **Preparation:** A fraudulent email, message, website, or attachment is created.
3. **Delivery:** The message is sent to the victim.
4. **Manipulation:** The attacker creates urgency, fear, curiosity, or trust to influence the victim.
5. **Compromise:** The victim clicks a link, downloads a malicious file, or provides confidential information.
6. **Exploitation:** The attacker uses the stolen information to access accounts, steal data, or compromise systems.

### Real-world case study: RSA SecurID breach (2011)

In March 2011, RSA, a security company known for its SecurID authentication products, suffered a cyberattack that began with targeted phishing emails.

Attackers sent emails to a small number of employees using the subject line "2011 Recruitment Plan." One employee opened a malicious Excel attachment containing an exploit that used an Adobe Flash vulnerability.

The malicious file enabled attackers to establish access to the compromised system and steal sensitive information related to RSA's SecurID products.

The incident demonstrated how a single employee interaction with a malicious attachment could contribute to a major organisational security breach.

**Security lesson:** Organisations must combine employee awareness training, email security, endpoint protection, and vulnerability management.

### Four phishing prevention recommendations

1. **Employee awareness training:** Train employees to recognise suspicious emails, unexpected attachments, impersonation attempts, and fraudulent links.
2. **Multi-factor authentication (MFA):** Require additional authentication factors to reduce the risk of account compromise through stolen passwords.
3. **Email security solutions:** Implement spam filtering, anti-phishing protection, attachment scanning, and domain authentication controls.
4. **Verify suspicious requests:** Confirm unusual payment requests, password-reset instructions, and requests for confidential information through independently verified communication channels.

## 3. Pretexting

### Definition

Pretexting is a social engineering technique in which an attacker creates a believable but false identity, situation, or story to manipulate a victim into revealing information or performing an action.

The attacker may pretend to be an IT support employee, bank representative, manager, supplier, or another trusted individual.

### How attackers build a false scenario

1. **Information gathering:** The attacker researches the victim, organisation, employees, and internal processes.
2. **Identity creation:** The attacker chooses a believable identity or professional role.
3. **Scenario development:** A convincing situation is created, such as an account problem, security emergency, or payment issue.
4. **Communication:** The attacker contacts the victim through email, telephone, or messaging platforms.
5. **Manipulation:** The attacker uses authority, urgency, trust, or fear to influence the victim.
6. **Information collection:** The victim may disclose credentials, financial information, or other confidential data.

### Real-world case study: Twitter social engineering attack (2020)

On July 15, 2020, Twitter experienced a major security incident involving social engineering.

According to Twitter's investigation, attackers targeted employees through phone-based spear phishing. They impersonated members of Twitter's IT department and manipulated employees into providing credentials.

The attackers gained access to internal systems and tools used by Twitter's support teams.

They subsequently targeted 130 accounts. For 45 accounts, attackers were able to initiate password resets, access the accounts, and publish fraudulent tweets promoting a Bitcoin scam.

The incident demonstrated how attackers can exploit employee trust and impersonation to gain access to sensitive organisational systems.

**Security lesson:** Employees should independently verify IT support requests and never disclose passwords or authentication codes to callers.

### Three pretexting prevention measures

1. **Identity verification:** Employees must verify the identity of anyone requesting confidential information or access to internal systems.
2. **Access control:** Apply role-based access control and least privilege so that compromised employee accounts cannot automatically access every organisational resource.
3. **Independent verification:** Establish procedures for confirming unusual requests through trusted communication channels, especially requests involving money, credentials, or sensitive data.

## 4. Baiting

### Definition

Baiting is a social engineering attack that uses something attractive or desirable to trick victims into performing an unsafe action.

The bait may be a physical object, a free digital download, or an attractive online offer.

Attackers exploit curiosity, greed, convenience, or the desire to obtain something for free.

### Types of baiting

**1. Physical baiting**

Attackers leave infected USB drives or other storage devices in locations where employees or members of the public may find them.

The devices may contain malware designed to infect a computer when connected.

**2. Digital baiting**

Attackers advertise fake software, free downloads, pirated applications, games, or attractive online offers to encourage victims to download malicious files or visit fraudulent websites.

### How baiting works

1. The attacker prepares an attractive object, file, or offer.
2. The bait is placed where potential victims are likely to encounter it.
3. The victim becomes curious or interested.
4. The victim connects the USB device, downloads a file, or interacts with the offer.
5. Malware may execute, credentials may be stolen, or the device may become compromised.

### Real-world research case study: USB baiting experiment (2016)

In a 2016 research study titled *Users Really Do Plug in USB Drives They Find*, researchers investigated whether people would connect USB drives they found in public locations.

The researchers dropped 297 USB drives around a university campus.

The study estimated that between 45% and 98% of the drives were connected, demonstrating how effective physical USB baiting can be.

Researchers found that some individuals connected the drives because they wanted to identify and return them to their owners.

Although this was a controlled research experiment rather than a documented malware outbreak, it demonstrated a significant human security weakness that attackers could exploit.

**Security lesson:** Employees should never connect unknown USB devices to organisational computers.

### Three baiting prevention measures

1. **USB device restrictions:** Restrict unauthorised USB storage devices through endpoint security and device-control policies.
2. **Safe downloading practices:** Download applications and files only from trusted and verified sources.
3. **Employee awareness:** Train employees not to interact with unknown storage devices, suspicious downloads, or offers that appear too good to be true.

## 5. Quid Pro Quo

### Definition

Quid pro quo is a social engineering technique in which an attacker offers something in exchange for information, access, or an action from the victim.

The attacker promises a benefit or service to persuade the victim to cooperate.

For example, someone may impersonate technical support and offer to fix an employee's computer in exchange for their login credentials.

### How it works

1. The attacker identifies something the victim needs.
2. The attacker offers a service, reward, or benefit.
3. The victim accepts the offer.
4. The attacker requests confidential information or access as a condition.
5. The attacker exploits the information or access received.

### Prevention

- Verify the identity of anyone offering technical support or other services.
- Never disclose passwords or authentication codes in exchange for assistance.
- Use approved organisational support channels and procedures.

## 6. Comparison of social engineering attacks

| Attack type | Primary target | Psychological lever exploited | Best countermeasure |
|---|---|---|---|
| Phishing | Email and online account users | Urgency and trust | Email security and awareness training |
| Spear phishing | Specific individuals | Personal trust | Targeted awareness and verification |
| Whaling | Senior executives | Authority and urgency | Executive security awareness |
| Vishing | Telephone users | Trust and authority | Independent identity verification |
| Smishing | Mobile phone users | Fear and urgency | Verify links and messages |
| Pretexting | Employees and individuals | Trust and authority | Identity verification procedures |
| Baiting | Employees and public users | Curiosity and greed | USB restrictions and safe downloads |
| Quid pro quo | Employees seeking assistance | Convenience and reward | Approved support channels |

## 7. Organisational recommendations: Employee security awareness checklist

Organisations should implement continuous security awareness programmes to reduce the risk of social engineering attacks.

A recommended five-point checklist includes:

1. **Regular security awareness training:** Educate employees about phishing, pretexting, baiting, impersonation, and other social engineering techniques.
2. **Phishing simulations:** Conduct controlled phishing exercises to measure employee awareness and identify areas requiring improvement.
3. **Identity and request verification:** Establish clear procedures for verifying unusual requests involving credentials, payments, confidential information, or system access.
4. **Incident reporting procedures:** Provide employees with simple ways to report suspicious emails, phone calls, messages, and physical devices.
5. **Continuous assessment:** Evaluate training effectiveness, review reported incidents, and update security policies as attack techniques evolve.

## 8. Conclusion

Social engineering remains a significant cybersecurity threat because it targets people rather than relying exclusively on weaknesses in technology.

Phishing, pretexting, baiting, and quid pro quo attacks exploit human behaviour to obtain sensitive information, compromise accounts, and gain unauthorised access to organisational systems.

The RSA breach and Twitter incident demonstrate how manipulation can contribute to serious security compromises, while USB research shows that even seemingly harmless physical objects can create security risks.

Organisations should therefore combine technical security controls with continuous employee awareness training, identity verification, access control, and effective incident reporting procedures.

**The most important lesson is that cybersecurity is not only about protecting systems; it is also about protecting the people who use them.**

## 9. References

1. Cybersecurity and Infrastructure Security Agency (CISA). (2024). *Phishing General Security Guidance*.  
   https://www.cisa.gov/sites/default/files/2024-02/Update%20to%20Phishing%20General%20Security%20Postcard_01.01.2024.pdf

2. Verizon. (2024). *2024 Data Breach Investigations Report*.  
   https://www.verizon.com/business/resources/reports/2024-dbir-data-breach-investigations-report.pdf

3. SANS Institute. (2001). Malcolm Allen, *Social Engineering: A Means To Violate A Computer System*.  
   https://www.sans.org/white-papers/529/

4. New York State Department of Financial Services. (2020). *Twitter Investigation Report*.  
   https://www.dfs.ny.gov/reports-and-publications/other-reports/Twitter_Report

5. Tischer, M., et al. (2016). *Users Really Do Plug in USB Drives They Find*. IEEE Security and Privacy.  
   https://research.google/pubs/users-really-do-plug-in-usb-drives-they-find/

6. Dark Reading. (2011). *RSA SecurID Attack Began With Excel File Rigged With Flash Zero-Day*.  
   https://www.darkreading.com/cyberattacks-data-breaches/rsa-secureid-attack-began-with-excel-file-rigged-with-flash-zero-day

7. Federal Bureau of Investigation, Internet Crime Complaint Center (IC3). *Business Email Compromise: The $55 Billion Scam*.  
   https://www.ic3.gov/PSA/2024/PSA240911
