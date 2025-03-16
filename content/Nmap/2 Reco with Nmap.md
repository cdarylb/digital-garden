
## Passive Reconnaissance

### Using Whois Lookup
```bash
whois example.com
```

### Checking DNS Records
```bash
dig example.com ANY
```

## Active Reconnaissance with Nmap

### Discovering Live Hosts in a Network
```bash
nmap -sn 192.168.1.0/24
```

### Detecting Firewalls and IDS
```bash
nmap -sA 192.168.1.1
```

### Evading IDS/IPS with Fragmentation
```bash
nmap -f 192.168.1.1
```

### Spoofing the Source IP
```bash
nmap -S 192.168.1.100 192.168.1.1
```

### Using Decoy Scans
```bash
nmap -D RND:10 192.168.1.1
```

## Exploiting Open Ports and Vulnerabilities

### Checking for Vulnerabilities with Nmap Scripts (NSE)
```bash
nmap --script=vuln 192.168.1.1
```

### Enumerating SMB Shares on Windows
```bash
nmap --script=smb-enum-shares -p 445 192.168.1.1
```

### Brute Force Attack on SSH
```bash
nmap --script=ssh-brute -p 22 192.168.1.1
