# LetsDefend-Sigma-Challenge
Detection engineering practice: Write-up and analysis of a LetsDefend challenge using a Sigma rule to detect ransomware activity leveraging bitsadmin.exe.

## 📌 Objective

Detect and analyze a ransomware infection that leveraged the Windows utility bitsadmin.exe to download additional malicious payloads, using a Sigma detection rule.

## 🧠 Skills Learned

- Understanding Sigma rules and their structure (selection, condition, tags, fields, log sources)

- Investigating ransomware behaviour with built-in Windows utilities

- Correlating malicious activity with command-and-control (C2) communication patterns

- Applying detection engineering concepts in a real-world SOC scenario

## 🛠 Tools Used

- LetsDefend Platform (challenge environment)

- Sigma Rules (YAML format)

- Windows Event Logs (proc_creation events)

- Text Editor (to review .yml rule file)
