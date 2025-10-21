# LetsDefend-Sigma-Challenge
Detection engineering practice: Write-up and analysis of a LetsDefend challenge using a Sigma rule to detect ransomware activity leveraging bitsadmin.exe.
<br>
<br>
## 📌 Objective

Detect and analyze a ransomware infection that leveraged the Windows utility bitsadmin.exe to download additional malicious payloads, using a Sigma detection rule.
<br>
## 🧠 Skills Learned

- Understanding Sigma rules and their structure (selection, condition, tags, fields, log sources)

- Investigating ransomware behaviour with built-in Windows utilities

- Correlating malicious activity with command-and-control (C2) communication patterns

- Applying detection engineering concepts in a real-world SOC scenario
<br>

## 🛠 Tools Used

- LetsDefend Platform (challenge environment)

- Sigma Rules (YAML format)

- Windows Event Logs (proc_creation events)

- Text Editor (to review .yml rule file)

<br>

## 🔎 Steps Performed

1. Reviewed the challenge description: ransomware suspected of using bitsadmin.exe.
   ![The LetsDefend Challenge page explaining what the challenge is about](images/sigma-challenge-description.png "LetsDefend Learn Sigma Challenge page")

3. Located the Sigma rule file:
 ```
C:\Users\LetsDefend\Desktop\ChallengeFile\proc_creation_win_bitsadmin_download.yml
```

3. Analyzed the Sigma rule sections:

- Selection: defined suspicious process creation patterns involving bitsadmin.exe.

- Condition: combined selections to flag malicious usage.

- Tags & Fields: identified the rule’s focus on ransomware and C2 communications.

- Logsource: Windows process creation events.

4. Mapped how this rule would detect attempts by ransomware to use bitsadmin.exe for downloads.

5. Documented findings and uploaded screenshots for reference.

Explored the Lab Environment provided by LetsDefend
![A picture showing the lab environment of LetsDefend for the Sigma challenge](images/lab-environment.png "A picture of the lab environment from LetsDefend")

I used the Timeline Explorer for my findings
![Picture showing the Timeline Explorer window before doing any findings](images/timeline-explorer.png "A picture of the interface of the Timeline Explorer")

I discovered that the targeted executable file was the one targeted by the Sigma rule
![A picture of the executable file](images/target-file.png "The picture shows the targeted executable file")

The command line option used to indicate the file transfer in the Sigma rule
![A picture of the command-line option used to indicate a file transfer](images/file-transfer.png "A picture showing the command line for a file transfer")

The logical expression in the condition field combined the criteria to trigger the Sigma rule
![A png file of the command line expression rule for the Sigma](images/argument-http-based.png "A picture of the command line logical expression for the Sigma rule")

The specific field the Sigma rule captured shows the command being executed
![The field that shows the command being executed](images/command-line.png "The command being executed by the Sigma rule")

The single ATT&CK tactic tag listed first in the Sigma rule
![Single ATT&CK tactic tag listed first in the Sigma rule](images/ATT&CK.png "The ATT&CK tactic tag")

The primary category of events that this Sigma rule was written to monitor
![The primary category of events for monitoring the Sigma rule](images/process_creation.png "Primary category of events for the Sigma rule to monitor")

The specific command line argument the Sigma rule looked for to identify the HTTP-based downloads
![A png file of the command line expression rule for the Sigma](images/argument-http-based.png "A picture of the command line logical expression for the Sigma rule")

The command line that miust be present to create a new transfer using bitsadmin
![A picture of the command-line option used to indicate a file transfer](images/file-transfer.png "A picture showing the command line for a file transfer")

