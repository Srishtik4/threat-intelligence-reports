# WannaCry – Indicators of Compromise (IOCs)

This document lists representative Indicators of Compromise (IOCs) associated with
the WannaCry ransomware attack analyzed in this repository. These indicators are
derived from publicly available threat intelligence sources and align with the
technical analysis presented in the report.

---

## File Based Indicators

| Indicator Type | Value | Description |
|---------------|-------|-------------|
| Encrypted file extension | `.WCRY` | Extension appended to encrypted files |
| Ransom note | `@Please_Read_Me@.txt` | Ransom message displayed to victims |
| Ransom UI | `@WanaDecryptor@.exe` | Graphical ransom interface |
| Malware executable | `tasksche.exe` | Main WannaCry ransomware binary |
| Malware executable | `taskdl.exe` | Downloader / support component |

---

## Network Indicators

 Indicator Type | Value | Description |
|---------------|-------|-------------|
| Protocol | SMBv1 | Vulnerable Windows file-sharing protocol |
| Port | TCP 445 | Used for lateral movement and exploitation |
| Traffic Pattern | SMB scanning | Scanning for vulnerable hosts |
| Exploit Used | EternalBlue | Remote code execution exploit |
| Kill-switch behavior | HTTP GET request | Checks availability of a hardcoded domain |

---

## Vulnerability & Exploitation Indicators

| Indicator | Value |
|---------|-------|
| CVE ID | CVE-2017-0144 |
| Microsoft Patch | MS17-010 |
| Vulnerable Component | SMBv1 |
| Affected Systems | Unpatched Windows systems |

---

## Cryptographic Indicators

| Indicator Type | Value |
|---------------|-------|
| Symmetric Encryption | AES |
| Asymmetric Encryption | RSA-2048 |
| Key Storage | Private key retained by attackers |

---

## Process & Behavioral Indicators

| Indicator | Description |
|---------|-------------|
| Execution of `tasksche.exe` | WannaCry ransomware process |
| Sudden mass file encryption | Rapid encryption of user data |
| High CPU utilization | Cryptographic operations |
| Unauthorized service creation | Persistence mechanism |
| Lateral SMB connections | Worm-like internal spread |

---

## Defensive Use Cases

These indicators may be leveraged for:
- SIEM correlation rules
- Endpoint detection alerts
- Network traffic monitoring
- Threat hunting exercises

---

## Notes

- Hash values are excluded due to multiple WannaCry variants.
- Live malicious domains and IP addresses are intentionally omitted.
- Refer to VirusTotal and vendor intelligence feeds for validated samples.
