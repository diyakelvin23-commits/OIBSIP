# Research Report: Common Network Security Threats

**Track:** Cyber Security --- Oasis Infobyte Security Analyst
Internship\
**Task:** Task 4 --- Research Report: Common Network Security Threats\
**Author:** \Diya Kelvin Powei
**Date:** \November 8, 2026

## 1. Introduction

Network security is essential because individuals, businesses, schools,
hospitals, and public services rely on connected systems to exchange
information and deliver services. Attackers may exploit weaknesses in
network protocols, devices, configurations, or user behaviour to
interrupt services, intercept sensitive information, impersonate trusted
systems, or redirect users to malicious destinations. These incidents
can lead to financial loss, privacy violations, reputational damage,
operational downtime, and loss of public trust. Network administrators
therefore need layered security controls, timely monitoring, secure
configurations, incident-response procedures, and user awareness to
reduce both the likelihood and impact of attacks.

## 2. Denial-of-Service (DoS) and Distributed Denial-of-Service (DDoS) Attacks

### How the attack works

A denial-of-service (DoS) attack attempts to make a system or service
unavailable to legitimate users by exhausting resources such as
bandwidth, connection capacity, memory, processing power, or application
resources. A DoS attack may originate from one system. A distributed
denial-of-service (DDoS) attack uses many systems or devices to send
traffic or requests towards a target simultaneously. Attackers may use
compromised devices (a botnet) or reflection and amplification
techniques that abuse exposed third-party services. MITRE ATT&CK
documents network DoS techniques including direct network floods and
reflection/amplification attacks \[1\].

### Real-world example

On 28 February 2018, GitHub experienced a large DDoS attack that peaked
at approximately **1.35 terabits per second (Tbps)**. GitHub reported
that the attack used exposed Memcached servers to amplify traffic and
that the service was unavailable for several minutes before mitigation
measures took effect. The attack illustrates how misconfigured
third-party systems and forged source IP addresses can be combined to
direct amplified traffic at a victim \[2\].

### Potential impact

-   Websites, APIs, DNS, email, and other network services may become
    slow or unavailable.
-   Organisations may lose sales, productivity, and customer confidence
    during an outage.
-   Emergency or business-critical services may be disrupted.
-   Incident response, traffic filtering, and additional infrastructure
    capacity may create significant costs.
-   A DDoS event may be used as a distraction while another intrusion is
    attempted.

### Three specific mitigation strategies

1.  **Use upstream DDoS protection and traffic scrubbing.** Work with an
    internet service provider or specialist DDoS-protection service that
    can identify and filter malicious traffic before it overwhelms the
    organisation's connection.
2.  **Apply network filtering and anti-spoofing controls.** Configure
    routers and firewalls to filter invalid or unexpected traffic, and
    work with network providers to implement source-address validation
    where appropriate. NIST discusses source-address validation and
    other routing-security measures in its guidance on DDoS mitigation
    \[3\].
3.  **Prepare capacity, monitoring, and an incident-response plan.** Use
    rate limiting where suitable, monitor traffic baselines and service
    health, maintain redundancy for critical services, and document who
    should be contacted and what steps should be taken during an attack.

## 3. Man-in-the-Middle (MitM) Attacks

### How the attack works

A man-in-the-middle (MitM) attack occurs when an attacker positions
themselves between two communicating parties and intercepts or alters
the data exchanged between them. This may be attempted through a
malicious or impersonated Wi-Fi access point, local network manipulation
such as ARP poisoning, rogue network configuration, or other techniques
that redirect traffic through an attacker-controlled system. If
communications are not properly protected, the attacker may read
sensitive information or change messages. Strong, correctly validated
encryption makes interception and undetected modification much harder
\[4\].

### Real-world example

MITRE ATT&CK describes the threat group Sea Turtle as having modified
DNS records at service providers to redirect traffic from legitimate
resources to attacker-controlled servers, enabling
adversary-in-the-middle activity and credential capture. This
illustrates how interference with trusted name-resolution infrastructure
can help an attacker position themselves between users and legitimate
services \[5\].

### Potential impact

-   Exposure of usernames, passwords, session cookies, or other
    sensitive data.
-   Account takeover if intercepted credentials or tokens are reused.
-   Alteration of information exchanged between users and services.
-   Redirection to fraudulent websites or malicious downloads.
-   Loss of confidentiality, integrity, and trust in the affected
    service.

### Three specific mitigation strategies

1.  **Enforce properly configured HTTPS/TLS.** Use valid certificates,
    modern TLS configurations, and strict certificate validation. Do not
    train users to ignore browser certificate warnings.
2.  **Secure local networks and remove unnecessary legacy protocols.**
    Use WPA2-AES or WPA3 for Wi-Fi, change default router credentials,
    segment networks, and disable unneeded protocols that can enable
    local traffic interception.
3.  **Monitor and harden network infrastructure.** Detect unexpected
    ARP/DNS changes and suspicious network configuration changes;
    restrict administrative access; and use network monitoring or
    intrusion-prevention capabilities to identify suspicious behaviour.
    MITRE ATT&CK recommends encryption, traffic filtering, network
    segmentation, and user training as mitigations for
    adversary-in-the-middle techniques \[5\].

## 4. IP Spoofing

### How the attack works

IP spoofing is the act of putting a forged source IP address into an IP
packet so that it appears to come from a different system. The source
address alone should not be treated as proof of identity. Spoofing can
be used to obscure the origin of traffic, impersonate another address in
some contexts, or enable reflection/amplification attacks. In a
reflection attack, the attacker sends requests to third-party servers
with the victim's address forged as the source, causing those servers to
send their responses to the victim \[3, 6\].

### Real-world example

During the February 2018 DDoS attack against GitHub, attackers abused
internet-exposed Memcached servers. Forged source IP addresses caused
the servers' amplified responses to be sent to GitHub. GitHub reported a
peak of about 1.35 Tbps and a short service interruption. The incident
is a documented example of IP spoofing being used as part of a
reflection/amplification DDoS attack \[2, 6\].

### Potential impact

-   A victim may receive large volumes of unwanted traffic and
    experience service disruption.
-   Investigators may initially have difficulty identifying the true
    origin of spoofed packets.
-   Third-party systems can be abused as reflectors, affecting both the
    victim and the systems involved.
-   Network logs and simple source-IP-based controls may become less
    reliable if spoofed addresses are not recognised.

### Three specific mitigation strategies

1.  **Implement source-address validation.** Network operators should
    use ingress and egress filtering, access-control lists, or unicast
    Reverse Path Forwarding (uRPF) where suitable to reduce packets with
    implausible source addresses. NIST SP 800-189 discusses
    source-address validation as a measure for preventing spoofed
    traffic \[3\].
2.  **Prevent reflection from exposed services.** Do not expose services
    such as Memcached or other UDP-based services unnecessarily to the
    public internet. Disable unused protocols and restrict access with
    firewall rules.
3.  **Use layered DDoS detection and mitigation.** Monitor traffic
    patterns, apply rate limits and filtering where appropriate, and
    coordinate with an upstream provider or DDoS-protection service to
    block attack traffic before it saturates the connection.

## 5. DNS Poisoning/Spoofing

### How the attack works

The Domain Name System (DNS) translates human-readable domain names into
IP addresses. DNS poisoning, often called DNS cache poisoning, occurs
when false DNS information is inserted into a resolver's cache so that
users are directed to an incorrect address. DNS spoofing can also
describe forged DNS responses or other manipulation of name resolution.
A victim may type a legitimate domain name but be directed to an
attacker-controlled destination. DNS tampering can affect web browsing
and other services that rely on name resolution \[7, 8\].

### Real-world example

The SANS Internet Storm Center documented a DNS cache-poisoning incident
in 2005 in which thousands of domain names were redirected to hostile
servers. Its analysis reported more than 1,300 poisoned domain names
during part of the incident and described effects involving web requests
and attempts against services including email and FTP \[8\]. Although
this is a historical case, it demonstrates how poisoned DNS data can
affect more than just web browsing.

### Potential impact

-   Users may be redirected to phishing pages or malware-hosting
    websites.
-   Credentials or other sensitive information may be exposed if users
    trust the redirected destination.
-   Email and other services may be misdirected or disrupted.
-   Organisations may suffer reputational damage and incident-response
    costs.
-   Incorrect DNS records can cause widespread service outages if
    critical names are affected.

### Three specific mitigation strategies

1.  **Deploy DNS Security Extensions (DNSSEC) where supported and
    properly configured.** DNSSEC helps validating resolvers verify the
    authenticity and integrity of DNS data; it does not encrypt DNS
    queries and is not a complete solution to every DNS attack.
2.  **Harden and monitor DNS infrastructure.** Keep DNS software
    updated, restrict who can change DNS records, secure registrar and
    DNS-provider accounts with multifactor authentication, and monitor
    unexpected record changes.
3.  **Use protective DNS and secure resolver configuration.** Use
    trusted recursive resolvers, restrict unauthorised DNS-server
    changes, review DNS logs, and consider encrypted DNS transport where
    appropriate. The Canadian Centre for Cyber Security recommends
    DNSSEC and other measures for reducing DNS-tampering risk \[7\].

## 6. Comparison of the Four Threats

  ---------------------------------------------------------------------------------------------------
  Threat               Typical attack vector      Who is at risk? Difficulty to   Ease of mitigation
                                                                  execute         (general estimate)
                                                                  (general        
                                                                  estimate)       
  -------------------- -------------------------- --------------- --------------- -------------------
  DoS/DDoS             Flooding a service or      Public          **Medium to     **Medium to
                       network; botnets;          websites,       high** for a    difficult** during
                       reflection/amplification   online          large,          a large attack;
                                                  services, DNS   effective       strongest results
                                                  providers,      attack; lower   often require
                                                  businesses, and for small-scale upstream/provider
                                                  users relying   disruption      support
                                                  on them                         

  Man-in-the-Middle    Traffic redirection, rogue Users on        **Medium**;     **Medium**; TLS,
                       Wi-Fi, ARP/DNS             untrusted       depends on      secure
                       manipulation, or weak      networks and    network         configuration,
                       encryption/validation      organisations   position and    segmentation, and
                                                  with weak       the target's    monitoring reduce
                                                  network         protections     risk substantially
                                                  controls                        

  IP Spoofing          Forged source IP address   Networks and    **Low to        **Medium**;
                       in packets; often used for services        medium** to     source-address
                       reflection/amplification   targeted by     forge packets   validation helps,
                                                  spoofed         in some         but requires
                                                  traffic, and    environments;   coordination across
                                                  third-party     exploiting it   networks
                                                  servers abused  effectively     
                                                  as reflectors   depends on      
                                                                  network         
                                                                  conditions and  
                                                                  filtering       

  DNS                  Forged or altered DNS      Users and       **Medium to     **Medium**; DNSSEC
  Poisoning/Spoofing   responses, poisoned        organisations   high**; varies  validation, access
                       resolver cache, or         relying on      with the method controls, secure
                       unauthorised DNS-record    affected        and DNS         resolver
                       changes                    resolvers or    protections in  configuration, and
                                                  domains         place           monitoring help
                                                                                  reduce risk
  ---------------------------------------------------------------------------------------------------

**Note:** Difficulty and mitigation ratings are qualitative estimates,
not universal measurements. They vary with the attacker's capabilities,
target architecture, exposure, security configuration, and available
defensive resources.

## 7. Conclusion: Three Key Takeaways for a Network Administrator

1.  **Use layered defences.** No single security control prevents every
    attack. Combine secure configuration, encryption, access control,
    network filtering, monitoring, and service resilience.
2.  **Protect foundational network services.** DNS, routing, and
    internet-facing services can affect many systems at once. Keep them
    updated, limit unnecessary exposure, protect administrative access,
    and validate traffic and DNS data where possible.
3.  **Prepare to detect and respond.** Establish normal traffic
    baselines, monitor for unusual changes, maintain an
    incident-response plan, and coordinate with internet service
    providers and specialist security services before an outage occurs.

## 8. References

1.  MITRE ATT&CK. (n.d.). *Network Denial of Service (T1498).*
    https://attack.mitre.org/techniques/T1498/
2.  Kottler, S. (2018, March 1). *February 28th DDoS Incident Report.*
    GitHub Engineering.
    https://githubengineering.com/ddos-incident-report/
3.  Sriram, K., & Montgomery, D. (2019). *Resilient Interdomain Traffic
    Exchange: BGP Security and DDoS Mitigation* (NIST SP 800-189).
    National Institute of Standards and Technology.
    https://doi.org/10.6028/NIST.SP.800-189
4.  National Institute of Standards and Technology. (n.d.).
    *Man-in-the-middle attack --- CSRC Glossary.*
    https://csrc.nist.gov/glossary/term/man_in_the_middle_attack
5.  MITRE ATT&CK. (n.d.). *Adversary-in-the-Middle (T1557).*
    https://attack.mitre.org/techniques/T1557/
6.  Cloudflare. (2018, March 6). *The real cause of large DDoS --- IP
    Spoofing.*
    https://blog.cloudflare.com/the-root-cause-of-large-ddos-ip-spoofing/
7.  Canadian Centre for Cyber Security. (2023). *Domain Name System
    (DNS) tampering.*
    https://www.cyber.gc.ca/en/guidance/domain-name-system-dns-tampering-itsap40021
8.  SANS Internet Storm Center. (n.d.). *DNS Poisoning.*
    https://isc.sans.edu/presentations/dnspoisoning.html
9.  Rose, S., Liu, C., & Gibson, R. (2026). *Secure Domain Name System
    (DNS) Deployment Guide* (NIST SP 800-81 Rev. 3). National Institute
    of Standards and Technology.
    https://doi.org/10.6028/NIST.SP.800-81r3

