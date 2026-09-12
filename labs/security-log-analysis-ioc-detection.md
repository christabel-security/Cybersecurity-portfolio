Security Log Analysis & IoC Detection Using Regex
Project Type

Scenario-Based Cybersecurity Coursework

Focus

Log Analysis • Indicators of Compromise • Security Monitoring • SIEM Concepts

Overview

This project involved analyzing a simulated security log file to identify potential Indicators of Compromise (IoCs) using regular expressions.

The objective was to extract relevant information from logs, identify suspicious patterns, and determine which events should receive further investigation.

The findings were treated as potential indicators requiring investigation, rather than proof that a compromise had occurred.

IoCs Investigated

The analysis focused on:

Repeated or suspicious IP addresses
Failed login attempts
Unauthorized access attempts
Activity outside normal business hours
Access to sensitive records
Repeated activity involving the same users or IP addresses
Regex Analysis

Regular expressions were developed to extract several categories of information from the simulated logs.

IP Addresses

A regular expression was used to identify IPv4 addresses within log entries.

Failed Logins

A pattern was developed to detect different variations of failed-login messages and extract the associated username.

Unauthorized Access

A pattern was created to identify unauthorized access events and the associated accounts.

Timestamps

Timestamps were extracted from log entries to identify activity occurring before 9:00 AM or after 5:00 PM.

Sensitive Records

A pattern was developed to identify sensitive record IDs and the users accessing those records.

Findings

The analysis identified several potentially suspicious patterns.

Examples included:

192.168.1.100 appeared repeatedly and was associated with root-account activity, including a failed login and unauthorized access.
10.10.10.10 was associated with repeated failed login attempts involving the administrative account.
203.0.113.50 was associated with repeated access to the same sensitive record using the same account.
Multiple events occurred outside normal business hours.

These findings were treated as potential indicators requiring further investigation, rather than confirmation that a security compromise had occurred.

Analysis & Prioritization

The exercise demonstrated the importance of correlating multiple indicators rather than treating individual events as definitive evidence of malicious activity.

For example, a single failed login does not necessarily indicate an attack. However, repeated authentication failures combined with suspicious accounts, unusual timing, unauthorized access, or recurring activity from the same IP address can provide stronger justification for investigation.

The analysis prioritized:

Repeated root-account activity.
Repeated administrative login failures.
Repeated access to sensitive records.
Suspicious activity associated with recurring IP addresses.
Challenges

One challenge was that similar events appeared in the logs using different wording.

For example, failed-login events could appear as:

Failed login for user
Login attempt failed for
Login failure for

Regex patterns were therefore designed to account for variations in log formatting.

Future Improvements

The detection patterns could be expanded to support additional log formats and tested against larger datasets to evaluate false positives and false negatives.

The analysis could also be automated and integrated with a SIEM platform such as Wazuh, allowing suspicious patterns to generate alerts automatically.

Skills Demonstrated

Regular Expressions • Log Analysis • IoC Identification • Security Monitoring • Pattern Recognition • Authentication Analysis • SIEM Concepts • Technical Documentation

Key Learning

This exercise demonstrated how regular expressions can help security analysts efficiently search large volumes of log data and identify patterns that may require further investigation.

It also reinforced the importance of avoiding premature conclusions: indicators should be correlated and investigated before determining whether a security incident has actually occurred.
