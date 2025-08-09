# Task 3 — Basic Vulnerability Scan on My PC

##  Objective
Perform a basic vulnerability scan on my own machine using a free vulnerability scanning tool to identify common security risks.

## Tools Used
- **Tool:** Nessus Essentials (Free) OR OpenVAS / Greenbone Community Edition
- **System Scanned:** [Windows 11 / Ubuntu 22.04 / Kali Linux]
- **Target:** 127.0.0.1 (localhost) or my LAN IP

## Steps Performed
1. Installed the scanner ([Nessus](https://www.tenable.com/products/nessus/nessus-essentials) / [OpenVAS](https://greenbone.github.io/docs/)).
2. Found my system’s IP address.
3. Configured the scan target with full/fast scan settings.
4. Enabled authenticated scanning (entered admin/root credentials for deeper checks).
5. Launched the scan and waited ~45 minutes.

##  Key Findings
| Severity | CVSS Score | Vulnerability Name | Evidence Summary | Suggested Fix |
|----------|-----------|--------------------|------------------|---------------|
| Critical | 9.8       | Example: OpenSSH Outdated | Version 7.2p2 detected | Update OpenSSH to latest version |
| High     | 8.2       | SMBv1 Enabled       | SMB protocol version 1 in use | Disable SMBv1 in Windows features |
| Medium   | 6.5       | Weak SSL Cipher     | TLS 1.0 supported | Disable TLS 1.0 and weak ciphers |

> **Note:** Actual vulnerabilities will differ — replace this table with your real findings.

## Remediation Summary
After reviewing the findings:
- Patched high/critical vulnerabilities.
- Disabled outdated protocols (e.g., SMBv1, TLS 1.0).
- Applied latest OS updates.

## Report
Full scan report is available in the `report/` folder.
