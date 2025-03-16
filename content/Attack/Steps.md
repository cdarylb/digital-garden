
## 1. Reconnaissance
The reconnaissance phase involves gathering information about the target to identify potential attack vectors.

### Open-Source Tools:
- **OSINT Framework** – Collection of OSINT (Open-Source Intelligence) tools.
- **Shodan** – Search engine for discovering devices connected to the internet.
- **theHarvester** – Gathers emails, subdomains, and other information from public sources.
- **Maltego CE** – Information gathering and visualization tool.

## 2. Scanning
Scanning involves probing the target network for open ports, services, and vulnerabilities.

### Open-Source Tools:
- **Nmap** – Network scanning and port enumeration.
- **Masscan** – Fast network scanner.
- **Nikto** – Web server vulnerability scanner.
- **OpenVAS** – Comprehensive vulnerability scanner.

## 3. Gaining Access (Exploitation)
In this phase, vulnerabilities identified during scanning are exploited to gain unauthorized access.

### Open-Source Tools:
- **Metasploit Framework** – Penetration testing framework with exploit modules.
- **SQLmap** – Automated SQL injection exploitation.
- **Hydra** – Password brute-force tool.
- **John the Ripper** – Password cracking tool.

## 4. Maintaining Access
Attackers aim to maintain access to the compromised system for persistence.

### Open-Source Tools:
- **Mimikatz** – Credential dumping.
- **Empire** – Post-exploitation framework.
- **Chisel** – Port forwarding tool for maintaining access.
- **Weevely** – PHP web shell for backdoor access.

## 5. Covering Tracks
The final phase involves erasing traces of the attack to avoid detection.

### Open-Source Tools:
- **Metasploit (Timestomp)** – Modifies file timestamps to evade forensic detection.
- **ClearLogs** – Clears system logs.
- **Auditpol** – Disables event logging on Windows.
- **BleachBit** – Securely deletes traces on Linux and Windows.

## Sources
- [OWASP Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)
- [Kali Linux Tools <3](https://tools.kali.org/)
- [NIST Penetration Testing Guide](https://csrc.nist.gov/publications/detail/sp/800-115/final)

