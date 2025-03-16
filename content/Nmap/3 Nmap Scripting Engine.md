# Note 3: Using Nmap with Plugins (NSE Scripts)

The **Nmap Scripting Engine ** allows users to write and execute custom scripts for vulnerability detection, network auditing, and exploitation...

## Scanning for Common Vulnerabilities

### Detecting Heartbleed (CVE-2014-0160)
```bash
nmap --script=ssl-heartbleed -p 443 192.168.1.1
```

### Detecting SQL Injection Vulnerabilities
```bash
nmap --script=http-sql-injection -p 80 192.168.1.1
```

### Checking for Anonymous FTP Access
```bash
nmap --script=ftp-anon -p 21 192.168.1.1
```

## Gathering More Information on Targets

### Finding Subdomains
```bash
nmap --script=dns-brute -p 53 example.com
```

### Checking for Open Telnet Services
```bash
nmap --script=telnet-encryption -p 23 192.168.1.1
```

### Finding Web Directories
```bash
nmap --script=http-enum -p 80 192.168.1.1
```

## Exploiting Services with NSE Scripts

### Attempting SMB Login with a Given Credential
```bash
nmap --script=smb-brute -p 445 192.168.1.1
```

### Checking for Default Credentials on Web Apps
```bash
nmap --script=http-default-accounts -p 80 192.168.1.1
```

### Testing for Weak SSH Algorithms
```bash
nmap --script=ssh2-enum-algos -p 22 192.168.1.1
