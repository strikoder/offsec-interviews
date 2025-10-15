## General
- **How many penetration testing engagements have you completed?**  
  Answer: State a clear number and scope. Example: “I’ve completed 12 full-scope engagements and ~30 targeted assessments across web, network, and AD environments.” Keep it factual and mention roles you held and types of tests.

## Network 
COMING SOON

## Web Application Security
- **Does `eval(request.json['param'])` introduce a remote code execution (RCE) risk?**  
  Answer: Yes. Passing unsanitized user input to `eval` allows arbitrary code execution. Avoid `eval`. Use strict parsing, whitelists, or safer interpreters.

## Mobile Pentesting
- **Are Frida scripts commonly used to bypass a web application firewall (WAF)?**  
  Answer: No. Frida is a dynamic instrumentation tool for hooking and modifying code in running apps (mobile/desktop). It’s used to bypass client-side protections and inspect app internals, not to evade server-side WAFs.

## Post-Exploitation
- **Is data exfiltration considered a post-exploitation technique?**  
  Answer: Yes. Exfiltration is a common post-exploitation activity used to remove data after gaining access.

## Active Directory
- **Is BloodHound a tool used mostly by compliance teams?**  
  Answer: No. BloodHound is an Active Directory attack-path and privilege-relationship tool used by red teams and blue teams for attack simulation and remediation.

## Phishing
- **What do we call a phishing attack that targets c-suite or other high-profile individuals?**  
  Answer: Whaling  

- **Name two common types of phishing attacks.**  
  Answer: Email phishing and spear phishing  

- **What’s the term for phishing done through voice calls?**  
  Answer: Vishing  

- **What’s the attack called where someone tricks a mobile provider into transferring a victim’s number to a new SIM card?**  
  Answer: SIM swapping
