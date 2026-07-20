# Case 05 - Malicious Macro has been executed

## Alert Summary

| Field | Value |
|------|------|
| Alert Name | SOC205 - Malicious Macro has been executed |
| Event ID | 231 |
| Severity | Medium |
| Date | February 28, 2024 |
| Event Type | Malware Execution |

---

## Investigation Summary

A malicious macro execution alert was investigated on the endpoint **Jayne**.

Log Management revealed that a ZIP file (`edit1-invoice.docm.zip`) containing a macro-enabled Word document was downloaded. The document was opened using `WINWORD.EXE`, which spawned `powershell.exe`. PowerShell executed a `DownloadFile()` command and performed a DNS query to `www.greyhathacker.net`. VirusTotal identified the file hash as malicious (28/63 detections), confirming the document as malicious.

---

## Indicators of Compromise

- File: `edit1-invoice.docm`
- ZIP Archive: `edit1-invoice.docm.zip`
- Domain: `www.greyhathacker.net`
- IP Address: `92.204.221.16`
- SHA256 File Hash

---

## Verdict

**True Positive**

---

## MITRE ATT&CK

- T1566.001 – Phishing Attachment
- T1204.002 – Malicious File
- T1059.001 – PowerShell

---

## Skills Practiced

- Malware Investigation
- Log Correlation
- PowerShell Analysis
- Threat Intelligence
- VirusTotal Analysis
- IOC Identification

---

## Investigation Files

- IOC.md
- Timeline.md
- Lessons-Learned.md

---

## Screenshots

- Alert Details
- Log Management
- Endpoint Details
- VirusTotal