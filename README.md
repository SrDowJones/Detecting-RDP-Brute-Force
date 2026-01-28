Project Overview
This project documents a real-world Remote Desktop Protocol (RDP) brute-force attack detected by Microsoft Sentinel against a publicly accessible Windows virtual machine hosted in Microsoft Azure

To support this project, I built a controlled lab environment consisting of:
  - Microsoft Sentinel
  - A single Windows virtual machine exposed to the internet via RDP

The purpose of this lab was to gain hands-on experience with SIEM alerting, log analysis, and incident investigation by monitoring real authentication activity against the VM.

Detection Logic
A custom analytics rule was created in Microsoft Sentinel to detect potential brute-force activity. The rule triggers when five or more failed RDP authentication attempts occur within a five-minute window.

No additional security controls (such as IP allow lists, MFA, or network restrictions) were implemented in order to observe raw attack behavior.

The virtual machine was left running for approximately 24 hours, during which Microsoft Sentinel generated:
  - 2 security incidents
  - 46 related alerts

For this project, a subset of these alerts was selected and investigated in detail.

Detection Source
Microsoft Sentinel analytics rules identified abnormal authentication patterns consistent with RDP brute-force activity targeting the virtual machine. The alerts were generated based on repeated failed logon attempts originating from external IP addresses.
