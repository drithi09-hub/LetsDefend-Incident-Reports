# Lessons Learned

- Macro-enabled Office documents (`.docm`) can execute malicious code.
- `WINWORD.EXE` spawning `powershell.exe` is a strong indicator of malicious activity.
- Event ID 4688 helps identify newly created processes.
- Event ID 4104 records PowerShell script execution.
- Combining endpoint logs and VirusTotal helps validate malware execution.