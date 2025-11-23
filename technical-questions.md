# Technical Questions

---

## General

**What is penetration testing, and can you explain the difference between vulnerability scanning and pentesting?**

A penetration test is an organized, targeted, and authorized attack that tests the security posture and defensive capabilities of IT infrastructure. Normally, there's a specific agreed-upon time frame that a penetration test will span, rules of engagement, and a clearly defined scope. In the end, the expected deliverable is a detailed penetration test report that security teams can use to mitigate any vulnerabilities that were discovered. Penetration tests are important because they are a great way to check if your security controls and processes are actually working. Without conducting penetration tests, I believe organizations can have a false sense of security. A simple comparison I keep in mind is that pentesting is like checking if the door to your home is actually locked and the alarm is armed.

The main focus of a vulnerability assessment is to identify and categorize risk associated with vulnerabilities discovered in IT assets. Typically they are conducted using automated scanning tools like Nessus or OpenVAS. They are commonly conducted as completely different assessments than penetration tests and do not focus on penetrating further into the network environment through the active use of exploits and attack chaining. That said, a vulnerability assessment is not as comprehensive as a penetration test. Organizations often have a vulnerability assessment done because they are required to for compliance reasons (PCI-DSS: page 23 of the PCI DSS v3.2.1).

**Can you describe the differences between risk analysis and penetration testing?**

Both risk analysis and penetration testing are important aspects of cybersecurity and can complement each other well.

A risk analysis is the process of studying all potential threats and faults that could lead to vulnerabilities in software. It doesn't require any scanning tools or applications, instead, a risk analysis aims to identify assets, vulnerabilities, threats, and the overall impact on the company if the vulnerability were exploited.

On the other hand, a penetration test is the act of lawfully attacking a system to identify any vulnerabilities. This tests whether existing systems and processes are actually working.

Overall, a risk analysis is more practical, identifying potential risks and impacts. Whereas, a penetration test is more technical, going beneath the surface to uncover vulnerabilities.

**Explain the difference between a black, white, and grey box test.**

In black box testing, the internal working structure of the application is unknown, whereas in white box testing, the internal working structure is known. Grey box testing combines the two, whereby the tester partially understands the application's internal working structure.

**Can you describe the different phases of a typical penetration testing engagement?**

The phases and the order in which they are done can differ depending on who you talk to. In general, these are the phases of a penetration test, many of which will be repeated as the test progresses:

0. Pre-engagement
1. Information gathering
2. Vulnerability assessment (as a phase built-in to the pentest)
3. Exploitation
4. Post-exploitation
5. Lateral movement
6. Post-engagement

**What makes a system vulnerable?**

There are various ways a system can be vulnerable, generally falling into the categories of:

1. Patch management: Running an out-of-date service or application with a known vulnerability
2. Vulnerability management: A web application that is vulnerable to web application vulnerabilities such as those covered under the OWASP Top 10
3. Configuration management: A misconfigured service (weak, default and re-used credentials, no authentication required)

**How would you handle sensitive data or information you come across during a penetration test?**

Every vulnerability discovered on a client's network can technically be considered sensitive data or information. Our job as a pentesting team is to help our clients improve security and teach them how they can do so.

As we document our findings, we must be careful and responsible with client data as we're trusted to do right by them. Suppose we are doing a test for a healthcare provider. It is not my job as a tester to go poking around a database of protected health information (PHI) out of curiosity.

Then, document this in a report and deliver it to the client. Some information will be redacted, but we, as a pentesting firm, will likely be keeping a copy of that report on our own company-owned systems. (We will want to ensure reports are stored on encrypted drives and when moved around over the network, that protocols and message systems use the strongest encryption possible.)

It is also possible that a tester can come across certain information on a system that may be considered illegal content. If this happened to me I would immediately stop the test and consult with my supervisor.

**Explain the difference between asymmetric encryption and symmetric encryption?**

Symmetric encryption uses a single shared key for both encryption and decryption and is generally faster, requiring less computing resources. It's ideal for bulk data encryption where efficiency is a key consideration (wifi - bitlocker).

Asymmetric encryption uses a public and private key pair. The public key is used for encrypting the data, while the private key is used to decrypt (or vice versa). This type of encryption is most commonly used for secure key exchange, digital signatures, and other forms of secure communication.

**How do you stay up-to-date with the latest security vulnerabilities and attack techniques?**

I use a mixture of passive and active learning to stay updated. Of course, I'm on social media sites. I'm intentional about following people who post IT and cybersecurity-focused content. I also subscribe to newsletters like SANS NewsBites & Medium blogs. And I use sites like Hack The Box & TryHackMe for active learning.

**What are the strengths and differences between Windows and Linux for web application testing?**

Windows and Linux both have strengths and weaknesses when it comes to web application testing. For beginners, Windows can be more user-friendly than Linux, which is more challenging to use.

However, Linux is much more reliable and secure in comparison to Windows. This is because inexperienced users often use Windows, making the OS more vulnerable to attackers.

In terms of usability for web application testing, Linux has a wider variety of native penetration testing tools, as well as a high degree of customization. The command-line interface in Linux is ideal for scripting and automation.

Having said this, Windows can be easier to navigate and offers many commercial tools including Microsoft Cloud Azure and AD. It's also important to consider that many organizations use Windows, meaning that pentesting from a Windows machine will much better mimic those real-world scenarios.

**Explain the CIA triad.**

Confidentiality, Integrity, Availability.

Confidentiality: means data is only accessible to authorized parties. In pentesting check for data leaks, weak auth, exposed secrets.

Integrity: means data and systems are not altered without authorization. In tests look for privilege escalation, tampered files, or replay attacks.

Availability: means systems and services remain usable when needed. In red-team exercises test for DoS risks, backup gaps, and single points of failure.

Attackers target any of the three. Defenses map to controls: encryption and MFA for confidentiality, checksums/logging and least privilege for integrity, redundancy and rate-limits for availability.

**Differences between Security Engineer, Security Analyst and Security Architecture**

Security Engineer: builds and implements security controls and tools. Focuses on firewalls, SIEMs, endpoint protection, automation, and patching. Hands-on and technical.

Security Analyst: monitors, investigates, and responds to alerts. Works in SOCs, performs log analysis, incident triage, and reporting.

Security Architect: designs overall security frameworks and policies. Defines standards, selects technologies, and ensures systems meet security requirements before deployment. Strategic and design-level role.

**Difference between Security Testing and Penetration Testing**

Security Testing: broad process to identify all vulnerabilities, misconfigurations, and risks in systems, networks, or applications. Can include code review, config checks, and compliance testing.

Penetration Testing: a subset of security testing that simulates real attacks to exploit vulnerabilities and demonstrate impact. Focuses on gaining access or privileges, not just finding issues.

**Difference between attack vector and attack surface**

Attack Vector: the specific path or method an attacker uses to exploit a vulnerability (e.g., phishing email, exposed port, SQL injection).

Attack Surface: the total set of all possible entry points an attacker can target in a system (e.g., open services, APIs, users, hardware interfaces).

**What is CVSS?**

CVSS (Common Vulnerability Scoring System): a standardized framework for rating the severity of vulnerabilities from 0 to 10 based on impact and exploitability. Scores are categorized as Low, Medium, High, or Critical.

**Difference between CVE and CWE**

CVE (Common Vulnerabilities and Exposures): unique ID for a specific publicly known vulnerability (e.g., CVE-2024-1234).

CWE (Common Weakness Enumeration): classification of underlying software flaws or coding patterns that cause vulnerabilities (e.g., CWE-79: Cross-Site Scripting).

**How many penetration testing engagements have you completed?**

State a clear number and scope. Example: "I've completed 12 full-scope engagements and ~30 targeted assessments across web, network, and AD environments." Keep it factual and mention roles you held and types of tests.

**What types of penetration testing teams are there and what are their responsibilities?**

**What are the most common types of malware?**

Viruses – attach to legitimate files and spread when those files are executed.
Worms – self-replicate across networks without user action.
Trojans – disguise as legitimate software to deliver malicious payloads.
Ransomware – encrypts data and demands payment for decryption.
Spyware – secretly monitors user activity and steals information.
Adware – displays unwanted ads and may track browsing behavior.
Rootkits – hide malicious processes or files to maintain persistence.
Botnets – networks of infected machines controlled remotely for coordinated attacks.

**How would you rate vulnerabilities during a penetration test? (risk matrix)**

Likelihood (Probability of exploitation) – how easily the vulnerability can be exploited.
Impact (Potential damage if exploited) – the effect on confidentiality, integrity, and availability.

Check TCM Security reports, they are the best explaining this.

**Why Should Penetration Testing Be Carried out by a Third Party?**

**Risk vs threat vs vulnerability**

---

## Network

**How do you scan a network?**

Depending on the breadth of the network you are pentesting, you want to keep your scans to the --top-ports or perhaps being more surgical naming individual ports of high importance, maybe the top 25–50 most important ports with -p. Mention you need the --exclude flag for scoping restrictions.

**What is the difference between TCP and UDP?**

**What are some of the most common services and what ports do they run on?**

**What is DNS?**

**What is ARP?**

**What is RDP?**

**What is a MAC address?**

**What is a firewall and how does it work?**

**What is the difference between an IDS and an IPS?**

**What are honeypots?**

**What is the difference between encoding, hashing and encrypting?**

**Name a few types of encoding, hash and encryption**

**What is salting and what is it used for?**

**What is the fastest way to crack hashes?**

**Difference between symmetric and asymmetric encryption**

**In what format are Windows and Linux hashes stored?**

**Where are Windows and Linux hashes stored, how can you retrieve them?**

**What are cron jobs/scheduled tasks?**

**Where are cron jobs stored in Windows and Linux?**

**What are the different package managers used in Linux and where are they used?**

**Describe the permission system used in Linux file systems**

**What are SUID and sudo?**

**What is Kerberos and how does it perform authentication?**

**What is the difference between WEP, WPA and WPA2?**

**What is WPS? Why is it insecure?**

**How can DNS and ARP be exploited by attackers?**

**What types of attacks is the Diffie-Hellman (DH) exchange potentially vulnerable to?**

**How would you remotely access a service that can only be accessed from within an internal network?**

**How would you allow regular users to run bash scripts as root and which way is most secure? (cron jobs)**

**If you were able to obtain an NTLM hash but could not decrypt it, how would you use this knowledge to obtain access to the target host? (PTH)**

**What measures would you put in place to prevent brute forcing?**

---

## Web Application Security

**Write a few points about SEH Overwrite Exploits?**

**What is POP POP RET in penetration testing?**

**Can you explain the main categories of HTTP status codes and give examples from each (e.g., 301, 404, 500)?**

Informational responses (100 – 199)
Successful responses (200 – 299)
Redirection messages (300 – 399)
- 301: moved permanently
- 307: temporary redirect
Client error responses (400 – 499)
- 400: bad request
- 401: unauthorized
- 403: forbidden
- 404: not found
- 405: method not allowed
Server error responses (500 – 599)

**Describe an XSS vulnerability in high-level terms. Ideally, as if you were explaining it to someone with only high-level technical knowledge.**

**What are the 3 types of XSS attacks? (Stored, Reflected, DOM-Based)?**

Stored XSS is when malicious script (usually JavaScript) is stored on the web server in a database, forum, log or comment field then executed when a victim user accesses the stored data.

Reflected XSS is when malicious script is reflected off the web server in the form of a pop-up or error message which executes immediately when a victim user accesses the URL.

DOM Based XSS is when a malicious script exploits a vulnerability in the client side JavaScript code, modifying the DOM (Document Object Model) of the web page, leading to execution in the browser.

**What is XSS, what types of XSS are there, what are the consequences of a successful attack and how do you prevent XSS?**

**Does `eval(request.json['param'])` introduce a remote code execution (RCE) risk?**

Yes. Passing unsanitized user input to `eval` allows arbitrary code execution. Avoid `eval`. Use strict parsing, whitelists, or safer interpreters.

**What is DDoS?**

**What is SQL Injection, different types and examples, how to prevent?**

**Secure and HTTPOnly flags**

**What is JWT token?**

**What is CSRF, what does it entail and how can it be prevented?**

**What is IDOR, what are its consequences and how can you prevent it?**

**What are LFI and RFI and what are the consequences of these attacks? How can they be prevented?**

**How can you secure data in transit?**

**Which cookie security flags exist?**

**What is XXE and what can it be used for?**

**What is XPath Injection in penetration testing?**

**Explain Web Application Scanning with w3af in pen-testing?**

**What is Hijacking Execution in pen-testing?**

**Path Traversal vs File Inclusion Vulnerability! How to Tell the Difference?**

Path Traversal: This vulnerability occurs when an application uses user-supplied input to construct filenames or paths without proper sanitization. An attacker can manipulate the input to move outside the intended directory, accessing arbitrary files on the server. For example, using "../" (dot dot slash) to navigate up the directory tree.

File Inclusion: This vulnerability occurs when an application dynamically includes files or scripts based on user-supplied input without proper validation. An attacker can manipulate the input to trick the application into including and executing a malicious file. There are two types: Local File Inclusion (LFI) and Remote File Inclusion (RFI). LFI is similar to Path Traversal, but it leads to code execution, while RFI allows the inclusion of remote files.

To tell the difference, look at the impact of the exploit:
- If the exploit allows access to arbitrary files but does not execute them, it's likely a Path Traversal vulnerability.
- If the exploit results in the execution of a file (either local or remote), it's likely a File Inclusion vulnerability.

**Difference between IDOR (Insecure Direct Object References) and BAC (Broken Access Control)**

**How do you handle WAF bypass?**

Encoding techniques, alternative payloads, timing analysis.

**What measures would you put in place to prevent brute forcing?**

Brute forcing can be prevented with account lockout mechanisms, CAPTCHA, IP-based restrictions, and multi-factor authentication.

**Could you list the OWASP 2022 Top 10 (2025 not out yet)?**

1. Broken Access Control
2. Cryptographic Failures
3. Injection
4. Insecure Design
5. Security Misconfiguration
6. Vulnerable and Outdated Components
7. Identification and Authentication Failures
8. Software and Data Integrity Failures
9. Security Logging and Monitoring Failures
10. Server-Side Request Forgery (SSRF)

---

## Network Pentesting

**Is BloodHound a tool used mostly by compliance teams?**

No. BloodHound is an Active Directory attack-path and privilege-relationship tool used by red teams and blue teams for attack simulation and remediation.

**What is the method of Finding the Attack String in Memory?**

**What is packet inspection?**

**What is privilege escalation? Provide a few examples**

**What is the difference between bruteforce and dictionary attacks?**

**What is a golden ticket attack?**

**What is a common misconfiguration of FTP and SMB? (anonymous login / null session)**

**Scenario: Wireless network assessment**

WiFi security, rogue access points, encryption

**What is SSL Stripping in penetration testing?**

**How would you remotely access a service that can only be accessed from within an internal network?**

Set up a VPN server that is accessible from the public network. A common method of an attacker gaining access to a local service is to find a way to gain control over a local machine and use that to access other local services/machines.

**Explain Cryptographic Failures in penetration testing?**

**What is Insecure Design Vulnerability?**

---

## Post-Exploitation

**Explain Incognito attacks with Meterpreter?**

**Is data exfiltration considered a post-exploitation technique?**

Yes. Exfiltration is a common post-exploitation activity used to remove data after gaining access.

**What is buffer overflow?**

**What is privilege escalation and how do you handle it?**

---

## Mobile Pentesting

**Are Frida scripts commonly used to bypass a web application firewall (WAF)?**

No. Frida is a dynamic instrumentation tool for hooking and modifying code in running apps (mobile/desktop). It's used to bypass client-side protections and inspect app internals, not to evade server-side WAFs.

---

## Phishing

**What do we call a phishing attack that targets c-suite or other high-profile individuals?**

Whaling

**Name two common types of phishing attacks.**

Email phishing and spear phishing

**What's the term for phishing done through voice calls?**

Vishing

**What's the attack called where someone tricks a mobile provider into transferring a victim's number to a new SIM card?**

SIM swapping

**What is an open redirect?**

Open redirect is a vulnerability that allows a user to control a redirect or forward to another URL, which is very common in phishing attacks.

---

## Deep Knowledge

**What is the OSI model and what are its layers?**

The OSI (Open Systems Interconnection) model explains how data travels from one device to another through a network. It divides the communication process into seven interconnected layers, each performing a specific role and relying on the one below it while serving the one above it.

**1. Physical Layer (Layer 1)**

Function: Transmits raw bits (0s and 1s) over the physical medium.
Examples: Ethernet cables, fiber optics, Wi-Fi radio waves, hubs, repeaters.
Connection:
- It provides the hardware means for the Data Link Layer (Layer 2) to send and receive data frames.
- It converts digital data from the Data Link Layer into electrical, optical, or radio signals for transmission.
- On the receiving end, it converts those signals back into bits for the Data Link Layer to interpret.

**2. Data Link Layer (Layer 2)**

Function: Packages bits into frames and provides error detection and correction between directly connected nodes.
Examples: Ethernet (IEEE 802.3), ARP, PPP, MAC addresses.
Connection:
- Takes raw bits from the Physical Layer and organizes them into frames.
- Ensures data integrity over a single hop (local network).
- Passes the correctly received frames up to the Network Layer (Layer 3).
- On the sender side, it adds headers (e.g., MAC address) before sending frames to the Physical Layer.

**3. Network Layer (Layer 3)**

Function: Handles routing and addressing, determining how data moves between different networks.
Examples: IP, ICMP, IPSec, routing protocols (OSPF, BGP).
Connection:
- Receives frames from the Data Link Layer, extracts packets, and adds logical addressing (IP).
- Chooses the best route to reach the destination network (routing).
- Sends the packet to the next router or destination host via the Data Link Layer.
- Provides the foundation for the Transport Layer (Layer 4) by ensuring the data can reach the correct device.

**4. Transport Layer (Layer 4)**

Function: Provides end-to-end communication, reliability, and flow control between devices.
Examples: TCP, UDP, SCTP.
Connection:
- Uses the IP address from the Network Layer to reach the destination, and port numbers to reach the correct application.
- For TCP: establishes a connection (3-way handshake), segments data, handles retransmission, and ensures ordered delivery.
- For UDP: sends datagrams without connection, suitable for real-time traffic.
- Passes reassembled, error-free data to the Session Layer (Layer 5).

**5. Session Layer (Layer 5)**

Function: Manages sessions—the setup, coordination, and termination of communication between applications.
Examples: NetBIOS, RPC, PPTP, session tokens in web communication.
Connection:
- Uses the reliable data stream from the Transport Layer to maintain logical communication sessions.
- Ensures that communication is kept alive and can be resumed if interrupted.
- Coordinates dialog control between local and remote applications.
- Passes session data to the Presentation Layer (Layer 6) for proper encoding and formatting.

**6. Presentation Layer (Layer 6)**

Function: Translates data between the application format and the network format. It handles data encoding, compression, and encryption.
Examples: SSL/TLS, ASCII, JPEG, MPEG, JSON, XML.
Connection:
- Takes raw data from the Application Layer and converts it into a standard format suitable for transmission.
- At the receiver's end, it reverses the process: decrypts, decompresses, and decodes data so the application can use it.
- Works as a translator between the Application Layer (Layer 7) and the lower layers.

**7. Application Layer (Layer 7)**

Function: Provides network services directly to end users or applications. It enables processes like web browsing, email, file transfer, and DNS queries.
Examples: HTTP, HTTPS, FTP, SMTP, DNS, SSH.
Connection:
- Interacts directly with the end-user software (like browsers or mail clients).
- Passes user-generated data down to the Presentation Layer, which prepares it for transmission.
- Receives data from the Presentation Layer and delivers it to the user in a readable form.

**How They Work Together (Data Flow Example)**

When you open a web page:

Application Layer: Your browser sends an HTTP request.
Presentation Layer: The request is encrypted with TLS.
Session Layer: A session is established with the web server.
Transport Layer: TCP segments the data and manages retransmissions.
Network Layer: IP determines the route from your device to the server.
Data Link Layer: The IP packet is encapsulated into an Ethernet frame with source and destination MAC addresses.
Physical Layer: The frame's bits are converted into electrical or optical signals and transmitted.

On the receiving end, each layer reverses this process — stripping its respective header and passing the remaining data upward — until the web server's application layer receives the original HTTP request.

**What happens when you request google.com with a browser?**

Your browser queries for DNS resolution in the following order to resolve 'google.com' to its IP address: browser cache -> operating system cache -> DNS cache -> ISP DNS servers. Most likely you have browsed to google.com before and the DNS data is already in your browser cache.

After the IP is gathered, your browser creates a TCP connection (skimming over the TCP handshake) to the web server over port 443 for HTTPS traffic.

Your browser and the web server then establish a TLS handshake, negotiate encryption protocols, exchange keys, to establish a secure connection.

Next your browser sends an HTTP GET request to the web server. If you were logging in to Google it'd be an HTTP POST request containing your credentials and other authentication data.

The web server will process your request and respond with HTML, CSS, JavaScript and images to render the web page on your browser, displaying the google.com homepage.

**How does encryption work in HTTPS?**

HTTPS uses TLS to encrypt data transmitted between your browser and the web server to secure your web traffic.

A TLS Handshake starts, during which, the browser and web server negotiate encryption algorithms (cipher suites and max TLS version) and exchange keys.

The web server verifies its identity by providing the browser with a digital certificate, containing information about the website but most importantly the certificate's public key and digital signature.

The browser checks if it can trust the digital certificate using a Certificate Authority, completing the TLS Handshake.

Then the browser and the web server agree on a symmetric key using the server's public/private (asymmetric encryption) keys.

Finally the HTTP data can be exchanged between browser and web server using this symmetric encryption, securing the web traffic.

---

## Tools

I will not provide questions for this category as there are endless questions regarding them.
