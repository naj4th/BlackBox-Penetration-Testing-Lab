BlackBox Penetration Testing Lab

End-to-End Exploitation: From Initial Access to Root Compromise

📌 Project Overview

This project documents a full black-box penetration testing engagement conducted against a deliberately vulnerable virtual machine in a controlled Capture The Flag (CTF) environment.

The assessment simulates a real-world external attacker scenario with no prior credentials or internal knowledge. The objective was to identify vulnerabilities, exploit them responsibly, escalate privileges, and demonstrate full system compromise while maintaining structured methodology and professional reporting standards.

The engagement successfully demonstrated a complete attack chain from weak authentication to root-level privilege escalation.

🎯 Objectives

Perform external black-box reconnaissance

Identify exposed services and attack surface

Exploit authentication weaknesses

Achieve remote code execution

Conduct credential harvesting and lateral movement

Perform privilege escalation

Document findings using professional penetration testing standards

🛠 Tools & Technologies Used

Nmap – Network reconnaissance & service enumeration

Hydra – Brute-force authentication testing

Burp Suite – Web request interception & analysis

Metasploit Framework – Reverse shell handling

Msfvenom – Payload generation

John the Ripper – Offline hash cracking

SSH – Remote access & lateral movement

Linux CLI – Post-exploitation enumeration

🧪 Attack Chain Summary

The penetration test followed a structured methodology:

1️⃣ Reconnaissance

Identified live hosts

Enumerated open ports (HTTP, SSH)

Service fingerprinting

2️⃣ Initial Access (Flag 1)

Discovered weak authentication controls

Performed brute-force attack

Gained administrative access

3️⃣ Remote Code Execution (Flag 2)

Exploited insecure file upload functionality

Uploaded malicious PHP reverse shell

Established interactive shell access

4️⃣ Credential Harvesting (Flag 3)

Identified exposed authentication files

Extracted password hashes

Performed offline cracking

Gained SSH access as developer user

5️⃣ Credential Leakage via Shell History (Flag 4)

Enumerated user directories

Discovered plaintext credentials in .bash_history

Performed lateral movement to higher privilege account

6️⃣ Privilege Escalation (Flag 5)

Identified writable script executed by root via cron

Modified script to create SUID binary

Achieved root-level access

Confirmed full system compromise

🚨 Key Vulnerabilities Identified

Weak authentication with no rate limiting

Insecure file upload leading to remote code execution

Improper file permissions exposing credential hashes

Credential leakage via shell history files

Privilege escalation through misconfigured scheduled task

📊 Security Impact

The vulnerabilities chained together allowed:

Unauthorized administrative access

Remote command execution

Credential compromise

Lateral movement

Root-level system takeover

This demonstrates how multiple medium-to-high vulnerabilities can combine to create critical business risk.

🔐 Security Recommendations

Implement strong password policies & MFA

Apply rate limiting and account lockout mechanisms

Enforce strict server-side file validation

Restrict permissions on sensitive files

Prevent credential exposure in shell history

Audit cron jobs and enforce least privilege

Conduct regular penetration testing and configuration audits

📁 Repository Contents

Penetration Testing Report.pdf – Full structured report

Testing methodology

Command logs

Evidence screenshots

Risk assessment & remediation plan

📚 Methodology Reference

The engagement follows structured penetration testing principles aligned with:

NIST SP 800-115

Black-box external threat modelling

Controlled exploitation methodology

Ethical security assessment practices

👤 Author

Najath Najeem
Cybersecurity Undergraduate
ISC2 Certified in Cybersecurity (CC) – Certification in progress
