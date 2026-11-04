# The Importance of Patch Management

**Author:** Diya Kelvin Powei  
**Track:** Cyber Security – Security Analyst  
**Task:** Task 6 – Research Report: The Importance of Patch Management

---

## 1. Introduction

Patch management is the systematic process of identifying, assessing, acquiring, testing, deploying, and verifying software updates across an organisation's systems. These updates, commonly known as patches, are released by software vendors to fix security vulnerabilities, correct software bugs, improve performance, and maintain system stability.

Patch management plays an important role in the vulnerability management lifecycle because it helps organisations reduce security weaknesses before attackers can exploit them. Unpatched systems create opportunities for cybercriminals to gain unauthorised access, steal sensitive information, install malware, or disrupt business operations.

According to the National Institute of Standards and Technology (NIST), enterprise patch management should be treated as preventive maintenance and an essential part of organisational security management [1].

## 2. Why Security Patches Matter

Software vulnerabilities are weaknesses in applications, operating systems, or firmware that attackers may exploit to compromise systems.

When a vulnerability is discovered, it may be reported to the software vendor or a vulnerability coordination organisation. Once publicly disclosed and assigned an identifier, it may receive a Common Vulnerabilities and Exposures (CVE) identification number.

For example, CVE-2017-5638 identifies a critical Apache Struts vulnerability exploited during the 2017 Equifax data breach.

The Common Vulnerability Scoring System (CVSS) provides a standardised method of assessing the severity of vulnerabilities. It considers factors such as attack complexity, required privileges, user interaction, and potential impact.

However, CVSS severity should not be confused with overall organisational risk. Security teams should also consider whether a vulnerability is actively exploited, whether affected systems are exposed, and how important those systems are to the organisation [2].

### 2.1 Real-World Incident: WannaCry Ransomware Attack (2017)

WannaCry was a major ransomware campaign that began on May 12, 2017. It exploited vulnerabilities in Microsoft's Server Message Block version 1 (SMBv1) protocol using an exploit commonly known as EternalBlue.

Microsoft had already released security update MS17-010 on March 14, 2017, to address the relevant vulnerabilities.

Despite the availability of the security update, many systems remained unpatched. Attackers exploited these vulnerable computers, allowing the ransomware to spread rapidly across networks.

The attack affected hundreds of thousands of computers around the world and disrupted organisations in multiple sectors, including healthcare.

**Security lessons:**
- Security updates should be installed promptly.
- Organisations must maintain accurate inventories of their systems.
- Unsupported and outdated operating systems should be replaced or isolated.
- Critical vulnerabilities should receive priority attention.

**Patch management lesson:** Having a security patch available does not protect an organisation unless the affected systems are identified and the patch is successfully deployed [3].

### 2.2 Real-World Incident: Equifax Data Breach (2017)

In 2017, Equifax, a major credit reporting agency, suffered a significant data breach involving an unpatched vulnerability in the Apache Struts web application framework.

The vulnerability was identified as CVE-2017-5638. Security information about the vulnerability had been publicly disclosed in March 2017, and a patch was available.

However, the vulnerable application was not successfully identified and patched. Attackers exploited the weakness to gain access to sensitive information.

Equifax initially reported that approximately 143 million US consumers were potentially affected. Exposed information included names, Social Security numbers, birth dates, and addresses.

A subsequent US Government Accountability Office investigation identified weaknesses in vulnerability identification, patch notification, and detection processes [4].

**Security lessons:**
- Organisations need accurate asset inventories.
- Patch notifications must reach the responsible technical teams.
- Vulnerability scans should verify that affected systems are identified.
- Security monitoring should continue after patches are deployed.

**Patch management lesson:** An organisation can have a patching policy and still remain vulnerable if its processes fail to identify every affected system.

## 3. Consequences of Not Patching Systems

Failure to apply security patches can expose organisations to several serious cybersecurity and business risks.

### 3.1 Data Breaches

Attackers may exploit known software vulnerabilities to gain access to confidential information, including customer records, employee information, financial details, and business documents.

The Equifax incident demonstrates how an unpatched application vulnerability can expose the personal information of millions of people.

### 3.2 Ransomware Attacks

Unpatched systems may be vulnerable to ransomware attacks. Attackers can exploit weaknesses to install malicious software, encrypt important files, and demand payment for their recovery.

The WannaCry incident demonstrated how unpatched Windows systems could be exploited to spread ransomware across connected networks.

### 3.3 Financial Losses

Cybersecurity incidents can result in significant expenses, including:

- Incident investigation and recovery.
- System restoration and replacement.
- Legal expenses.
- Regulatory penalties and settlements.
- Customer compensation.
- Lost business opportunities.

### 3.4 Compliance Violations

Organisations that fail to maintain appropriate security controls may violate applicable regulatory or industry requirements.

Depending on the organisation and jurisdiction, inadequate vulnerability management may create regulatory exposure, contractual consequences, and legal liabilities.

### 3.5 Operational Disruption

Exploited vulnerabilities can cause system outages, interrupt business operations, reduce productivity, and affect customer confidence.

**Overall impact:** Poor patch management increases the likelihood that known vulnerabilities will become entry points for cyberattacks.

## 4. The Patch Management Lifecycle

An effective patch management programme follows a structured lifecycle consisting of five major phases.

### 4.1 Discovery

The organisation identifies its hardware, operating systems, applications, and software versions.

This phase helps security teams understand which systems require updates and where vulnerabilities may exist.

**Example:** Using vulnerability scanning tools to identify outdated software across company computers.

### 4.2 Assessment

Identified vulnerabilities and available patches are evaluated according to their severity and potential impact.

Security teams consider:

- CVSS severity scores.
- Evidence of active exploitation.
- Whether the affected system is internet-facing.
- The importance of the affected asset.
- Potential business impact.

**Example:** Prioritising a vulnerability listed in CISA's Known Exploited Vulnerabilities (KEV) Catalog.

### 4.3 Testing

Before widespread deployment, patches are tested in a controlled environment to identify compatibility issues, application failures, or unexpected system behaviour.

Testing reduces the possibility that an update will disrupt important business operations.

**Example:** Installing a security update on a test workstation before deploying it across the organisation.

### 4.4 Deployment

After successful testing, the approved patch is installed on the affected systems.

Deployment may be performed manually or through automated patch management solutions.

Organisations should maintain records of deployment activities and ensure that critical systems receive the necessary updates.

### 4.5 Verification

After deployment, security teams confirm that the patches were installed successfully and that the vulnerabilities have been addressed.

Verification may involve:

- Checking installed software versions.
- Reviewing update installation logs.
- Performing vulnerability scans.
- Monitoring system performance.
- Confirming that affected services operate correctly.

The verification phase ensures that patch deployment has achieved its intended security objective.

## 5. Seven Best Practices for Effective Patch Management

Organisations should follow these seven practices to improve their patch management programmes.

**1. Maintain an Accurate Asset Inventory**

Maintain an updated record of all computers, servers, applications, operating systems, and network devices. This helps identify systems requiring security updates.

**2. Monitor Vulnerability Information**

Regularly monitor trusted vulnerability databases and security advisories, including the CVE database, National Vulnerability Database (NVD), and CISA Known Exploited Vulnerabilities Catalog.

**3. Prioritise Patches Based on Risk**

Give priority to actively exploited vulnerabilities, critical security weaknesses, internet-facing systems, and assets containing sensitive information.

**4. Establish a Regular Patching Schedule**

Create a documented schedule for routine updates while maintaining a process for emergency security patches.

**5. Test Patches Before Deployment**

Test updates in a controlled environment to identify compatibility issues and prevent unnecessary disruption to business operations.

**6. Automate Where Appropriate**

Use reliable patch management tools to identify missing updates, distribute approved patches, and track installation progress.

**7. Verify and Document Every Update**

Confirm successful installation, perform follow-up vulnerability checks, and maintain records of patching activities, failures, and exceptions.

## 6. Challenges in Patch Management and Their Solutions

Although patch management is essential, organisations may encounter several challenges.

| Challenge | Explanation | Recommended solution |
|---|---|---|
| Legacy systems | Older systems may no longer receive vendor security updates. | Replace unsupported systems or isolate them and apply additional security controls. |
| Downtime concerns | Installing updates may interrupt critical business services. | Schedule maintenance windows and use phased deployments. |
| Compatibility issues | Some updates may conflict with existing applications. | Test patches in controlled environments before deployment. |
| Limited resources | Small IT teams may struggle to monitor and install updates across many devices. | Automate routine patching and prioritise high-risk vulnerabilities. |
| Poor asset management | Unknown or forgotten devices may remain unpatched. | Maintain an accurate and regularly updated asset inventory. |
| Delayed notifications | Security updates may not reach the responsible teams promptly. | Establish clear communication and patch ownership procedures. |

Organisations can overcome these challenges by developing clear patch management policies, assigning responsibilities, automating suitable processes, and regularly reviewing their security posture.

## 7. Conclusion

Patch management is a fundamental part of effective cybersecurity because it reduces the exposure of systems to known software vulnerabilities. Organisations that fail to apply security updates may become targets of ransomware, data breaches, financial losses, and operational disruptions.

The WannaCry ransomware campaign and the Equifax data breach demonstrate the serious consequences that can arise when vulnerable systems remain unpatched.

Three important takeaways are:

1. **Identify vulnerabilities early:** Organisations must maintain accurate asset inventories and continuously monitor security updates.
2. **Prioritise and deploy patches:** Critical and actively exploited vulnerabilities should receive urgent attention, supported by appropriate testing.
3. **Verify patch installation:** Applying an update is not enough; organisations must confirm that it was successfully installed and that the vulnerability has been addressed.

An effective patch management strategy helps organisations strengthen their security posture, protect sensitive information, and reduce the likelihood of successful cyberattacks.

## 8. References

[1] National Institute of Standards and Technology (NIST). (2022). *SP 800-40 Rev. 4: Guide to Enterprise Patch Management Planning: Preventive Maintenance for Technology.*  
https://csrc.nist.gov/pubs/sp/800/40/r4/final

[2] National Vulnerability Database (NVD). *CVE FAQs and Common Vulnerability Scoring System (CVSS).*  
https://nvd.nist.gov/general/FAQ-Sections/CVE-FAQs

[3] Microsoft Security Response Center. (2019). *A Reminder to Update Your Systems to Prevent a Worm.*  
https://www.microsoft.com/en-us/msrc/blog/2019/05/a-reminder-to-update-your-systems-to-prevent-a-worm

[4] U.S. Government Accountability Office (GAO). (2018). *Data Protection: Actions Taken by Equifax and Federal Agencies in Response to the 2017 Breach.*  
https://www.gao.gov/products/gao-18-559

[5] Cybersecurity and Infrastructure Security Agency (CISA). *Known Exploited Vulnerabilities Catalog.*  
https://www.cisa.gov/known-exploited-vulnerabilities-catalog

[6] MITRE. *Common Vulnerabilities and Exposures (CVE).*  
https://www.cve.org/
