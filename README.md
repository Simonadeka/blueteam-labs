# Blueteam-Labs
My 30-day journey from attacker view to defender view. Documenting Nmap, vuln analysis, detection, and defense hardening.

## Nmap Script Analysis

## Objective:
To use Nmap scripts to identify vulnerabilities and weaknesses in a target system (Metasploitable 2) and analyze the findings from a defensive perspective.

## Findings:
1. FTP 21/tcp: vsftpd 2.3.4 backdoor (CVE-2011-2523) → Root access confirmed
2. SSH 22/tcp: Password auth enabled → Brute-force surface
3. Telnet 23/tcp: Clear-text login → Credential exposure
4. SMTP 25/tcp: Weak ciphers → MITM risk

!screenshot.png


## Defender Takeaway:

Kill Telnet. Use SSH with keys only.
Patch outdated services + disable anonymous ciphers.
Monitor for --script vuln scans. That’s recon in your logs.


# Next:Day 12: Detecting Nmap scans and writing SIEM alerts
# Tools Used:NmapMetasploitable 2Kali Linux
