Linux System Hardening & Security Configuration Assessment
Project Type

Scenario-Based Cybersecurity Coursework

Environment

Ubuntu 22.04 • Docker

Role

Junior DevOps Engineer — Simulated Coursework Scenario

Overview

This project involved a scenario-based security configuration assessment of an Ubuntu Linux workstation.

The objective was to audit the system for security weaknesses, remediate identified issues, and verify that the final configuration met the security requirements defined in the scenario.

Assessment Areas

The assessment covered:

User accounts and group memberships
Administrative privileges
Password and account settings
SSH configuration
Installed network services
Firewall configuration
System security settings
Key Findings

The assessment identified 15 security configuration flags involving areas such as:

Excessive administrative privileges
An unauthorized user account
Incorrect group configuration
Weak SSH settings
Unnecessary network services
A disabled firewall
Account and password configuration issues
Remediation
Access Control

The following access-control changes were performed:

Removed an unauthorized user account.
Removed an unauthorized user from the sudo group.
Created and configured the required voyagers group.
Verified final user and group membership.

These changes helped apply the principle of least privilege by ensuring that users had only the access required for the scenario.

SSH Hardening

The SSH configuration was hardened by:

Disabling direct root login.
Reducing the SSH login grace period.
Replacing outdated cryptographic ciphers.
Replacing weak MAC algorithms.
Verifying the resulting configuration using sshd -T.
Attack Surface Reduction

Unnecessary services, including FTP, HTTP, and CUPS, were identified and removed because they were not required for the workstation's intended purpose.

Removing unnecessary services reduced the system's exposed attack surface.

Firewall Configuration

UFW was enabled and configured with:

Default-deny incoming traffic.
Default-allow outgoing traffic.
Required SSH access permitted on port 22.

The final firewall configuration was then verified.

Tools Used
Linux command line
id
getent
passwd
chage
sshd
dpkg
apt
ufw
ss
Linux configuration files
Docker
Challenges

The lab environment presented some limitations.

The Docker environment did not have nano installed, so command-line tools were used to modify configuration files.

Additionally, systemctl could not be used because the container was not running systemd. Alternative commands were therefore used for package and configuration verification.

These limitations provided additional experience working with Linux systems in containerized environments.

Skills Demonstrated

Linux System Hardening • Access Control • Least Privilege • SSH Security • Firewall Configuration • Attack Surface Reduction • User & Group Management • Security Auditing • Remediation • Verification

Key Learning

This exercise strengthened my understanding of how seemingly small configuration issues—such as unnecessary services, excessive privileges, weak SSH settings, or an inactive firewall—can increase a system's attack surface.

It also reinforced the importance of verifying security changes after remediation rather than assuming that a configuration change was successful.
