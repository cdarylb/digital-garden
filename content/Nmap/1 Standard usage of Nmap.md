# Standard Usage of Nmap

## Introduction to Nmap
Nmap means Network Mapper and is an open-source tool used for network discovery and security auditing. It is widely used by system administrators and penetration testers to map networks, identify active hosts, and detect open ports and services.

## Basic Scanning Commands

### Scanning a Single Host
```bash
nmap 192.168.1.1
```
This command performs a basic scan on the target IP address.

### Scanning a Range of IPs
```bash
nmap 192.168.1.1-100
```

### Scanning a Subnet
```bash
nmap 192.168.1.0/24
```

### Scanning a Specific Port
```bash
nmap -p 80,443 192.168.1.1
```

### Scanning All Ports
```bash
nmap -p- 192.168.1.1
```

## Service and Version Detection

### Detecting Running Services
```bash
nmap -sV 192.168.1.1
```

### Detecting Operating System
```bash
nmap -O 192.168.1.1
```

### Aggressive Scanning
```bash
nmap -A 192.168.1.1
```

## Stealth and Performance Tuning

### Using SYN Scan (Stealth Scan)
```bash
nmap -sS 192.168.1.1
```

### Fast Scan Mode
```bash
nmap -F 192.168.1.1
```

### Using Timing Options for Faster Scanning
```bash
nmap -T4 192.168.1.1