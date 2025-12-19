# WannaCry – MITRE ATT&CK Mapping

This document maps the techniques used by the WannaCry ransomware
to the MITRE ATT&CK framework based on publicly available analysis.

---

## ATT&CK Technique Mapping

| Tactic | Technique | Technique ID | Description |
|------|---------|--------------|------------|
| Initial Access | Exploit Public-Facing Application | T1190 | Exploitation of SMB vulnerability MS17-010 |
| Execution | Command and Scripting Interpreter | T1059 | Execution of malicious commands via shell |
| Persistence | Boot or Logon Autostart Execution | T1547 | Ensures malware runs after reboot |
| Lateral Movement | SMB / Windows Admin Shares | T1021.002 | Propagation across network via SMB |
| Impact | Data Encrypted for Impact | T1486 | Encryption of user files for ransom |

---

## Defensive Notes

- Network monitoring on TCP port 445 can detect exploitation attempts
- Timely patching of MS17-010 prevents initial access
- Endpoint monitoring can detect suspicious encryption activity
