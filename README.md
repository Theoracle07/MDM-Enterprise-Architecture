# MDM-Enterprise-Architecture
Enterprise Mobile Device Management (MDM) & BYOD Security Lab
Project Lead: Jacob (Build with Jacob Series)
Platform: ManageEngine MDM Plus (Cloud)
Focus: Cybersecurity, Data Loss Prevention (DLP), and Privacy-First Management
📌 Executive Summary
In a modern workforce, employees use personal devices to access sensitive corporate data. Without management, this creates a massive security gap. This project demonstrates a Zero-Trust, Privacy-First MDM Architecture that secures company assets on Android devices without compromising employee privacy.
----
🛠️ Implementation Scenarios
1. Secure Containerization (Work Profile)
The Problem: Traditional "Device Owner" management is too invasive for personal phones, leading to employee distrust.
The Solution: Implemented Android Enterprise Work Profiles. This creates a cryptographically separated "Briefcase" on the device.
Outcome: Corporate apps (Gmail, Drive, etc.) are managed by the IT Admin, while personal apps remain completely invisible to the organization.
2. Data Loss Prevention (DLP) & Clipboard Security

The Problem: Data leakage occurs when employees copy work-related information into personal messaging apps.

The Solution: Enforced a policy restricting the shared clipboard.
Outcome: Attempting to "Paste" work data into a personal app triggers an "Action not allowed by IT Admin" notification.

3. Session Hardening & Anti-Hijacking
The Problem: Long-lived admin sessions increase the risk of unauthorized access if a laptop is left unattended.

The Solution: Configured 8-hour session expirations to align with standard work shifts and restricted accounts to 1 active session.

Outcome: Improved security posture by ensuring re-authentication is required daily and preventing account sharing.

4. Remote Offboarding & Corporate Wipe

The Problem: Lost devices or terminated employees pose a "residual data" risk.
The Solution: Configured a "Corporate Wipe" kill-switch.

Outcome: IT can instantly delete the Work Profile and all encrypted data remotely. Personal photos, messages, and apps are unaffected.
------
⚠️ Known Platform Limitations (BYOD Mode)
Hardware Restrictions: Under BYOD (Profile Owner), certain hardware controls (like global camera disable or factory reset protection) are unavailable. These require COPE or Fully Managed enrollment.

The Analog Hole: While screenshots are blocked, physical photos taken with a second device remain a risk. This is mitigated by Acceptable Use Policies (AUP) and watermark strategies.
🚀 Why This is Essential for Business
Compliance: Meets standard data protection regulations (GDPR/NDPR).
Cost Savings: Enables a "Bring Your Own Device" (BYOD) strategy, saving companies thousands in hardware costs.
Peace of Mind: Provides a "Remote Kill-Switch" for sensitive data.
For technical implementation details and step-by-step screenshots, please refer to the files in the /Scenarios folder.