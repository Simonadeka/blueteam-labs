# blueteam-labs
My 30-day journey from attacker view to defender view. Documenting Nmap, vuln analysis, detection, and defense hardening.

Nmap Script AnalysisO

bjective:To use Nmap scripts to identify vulnerabilities and weaknesses in a target system (Metasploitable 2) and analyze the findings from a defensive perspective.

Findings:
FTP 21/tcp: vsftpd 2.3.4 backdoor (CVE-2011-2523) → Root access confirmed
SSH 22/tcp: Password auth enabled → Brute-force surface
Telnet 23/tcp: Clear-text login → Credential exposure
SMTP 25/tcp: Weak ciphers → MITM risk

!screenshot.png


Defender Takeaway:

Kill Telnet. Use SSH with keys only.
Patch outdated services + disable anonymous ciphers.Monitor for --script vuln scans. That’s recon in your logs.What's 


Next:Day 5: Detecting Nmap scans and writing SIEM alertsTools Used:NmapMetasploitable 2Kali Linux
