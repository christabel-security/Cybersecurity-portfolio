Operation Silent Shadow — Cyber Threat Intelligence Analysis
Project Type

Scenario-Based Cybersecurity Coursework

Focus

Cyber Threat Intelligence • MITRE ATT&CK • TTP Analysis • Threat Actor Assessment

Overview

Operation Silent Shadow was a scenario-based cyber threat intelligence exercise involving a fictionalized multi-stage attack against a government organization.

The objective was to analyze the attack scenario, identify attacker behaviors, map them to the MITRE ATT&CK framework, assess the most likely threat actor, and recommend appropriate defensive measures.

Objectives
Analyze the different phases of a simulated cyberattack.
Identify attacker tactics, techniques, and procedures (TTPs).
Map observed behaviors to MITRE ATT&CK techniques.
Assess potential threat-actor attribution.
Recommend defensive and mitigation strategies.
Attack Analysis

The simulated attack was analyzed across several stages.

Initial Access

The scenario described targeted phishing emails containing malicious attachments. Employees who opened the attachments allowed malicious files to execute and establish a backdoor.

MITRE ATT&CK techniques identified:

T1566.001 — Phishing: Spearphishing Attachment
T1204.002 — User Execution: Malicious File
Persistence & Privilege Escalation

The simulated attackers established persistence through a Windows service and used credential dumping to obtain additional credentials.

Techniques identified:

T1543.003 — Create or Modify System Process: Windows Service
T1003 — OS Credential Dumping
Defense Evasion & Credential Access

PowerShell was used to execute commands and scripts, while compromised credentials were used to access additional systems.

Techniques identified:

T1059.001 — Command and Scripting Interpreter: PowerShell
T1078 — Valid Accounts
Exfiltration & Impact

The scenario described sensitive information being transferred to a command-and-control server and critical files being encrypted to disrupt operations.

Techniques identified:

T1041 — Exfiltration Over C2 Channel
T1486 — Data Encrypted for Impact
Threat Actor Assessment

Based on the combination of TTPs presented in the scenario, Sandworm Team (APT44) was assessed as the most likely threat actor.

This assessment was not considered conclusive attribution. The techniques described in the scenario, including phishing, PowerShell execution, credential theft, valid-account abuse, and data exfiltration, are used by multiple threat groups.

The exercise therefore reinforced the importance of distinguishing between evidence supporting a threat-actor assessment and evidence that can establish attribution with confidence.

Mitigation Recommendations

The following defensive measures were recommended:

Improve email filtering and phishing-awareness training.
Implement endpoint controls to prevent unauthorized files from executing.
Monitor Windows service creation and modification.
Protect and regularly review privileged accounts.
Enable PowerShell logging and monitoring.
Implement multi-factor authentication for privileged and remote-access accounts.
Monitor network traffic and implement data-loss prevention controls.
Maintain protected and regularly tested backups.
Skills Demonstrated

Cyber Threat Intelligence • MITRE ATT&CK • TTP Analysis • Threat Actor Assessment • Security Research • Risk Analysis • Defensive Security • Technical Reporting

Key Learning

This exercise strengthened my ability to analyze an attack as a sequence of related activities rather than as isolated events.

It also reinforced the importance of distinguishing between evidence that supports a threat-actor assessment and evidence that can conclusively establish attribution.
