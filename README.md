# DNS Spoofing Tool (TuDoor Attack Simulation)

This repository contains a Python script to simulate DNS spoofing and cache poisoning, focusing on vulnerabilities like the **TuDoor attack**. The script demonstrates how malformed DNS responses can be injected into a resolver’s cache by exploiting logic vulnerabilities in DNS response pre-processing.

## Features
- Simulates **DNS cache poisoning**.
- Allows the user to spoof any domain with a custom fake IP.
- Built-in demonstration of real-world CVEs like **CVE-2023-29483** and **CVE-2023-28452**.
- Includes an **About** section and metadata such as the developer information, version, and development date.

## Usage

### Command-Line Arguments:
- `--d`: Domain to spoof (e.g., `example.com`).
- `--vip`: Victim's IP address (e.g., `192.168.1.100`).
- `--dns`: DNS Server IP (e.g., `192.168.1.1`).
- `--fip`: Fake IP address to return in the DNS response (e.g., `1.2.3.4`).
- `--about`: Displays information about the script and developer.

### Example:
To simulate DNS spoofing for the domain `example.com`, targeting the victim `192.168.1.100` with a fake IP of `1.2.3.4` and using DNS server `192.168.1.1`:
```bash
python3 exploit_dns.py --d example.com --vip 192.168.1.100 --dns 192.168.1.1 --fip 1.2.3.4
