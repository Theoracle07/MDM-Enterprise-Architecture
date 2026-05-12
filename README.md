# Mobile Device Management (MDM) Policy Implementation
### Enterprise Mobile Security Framework using ManageEngine MDM Plus

## Overview
This project documents the design and implementation of a 
Mobile Device Management framework simulated across 3 real 
Android devices using ManageEngine Mobile Device Manager Plus 
(Cloud).

The goal was not just to configure a tool — but to solve real 
enterprise security problems that IT administrators face daily 
when managing corporate and personal mobile devices.

---

## The Business Problem
Organizations face three critical mobile security challenges:

1. **Uncontrolled personal devices** accessing company data 
   (BYOD risk)
2. **Data leakage** between personal and work profiles
3. **Lost or compromised devices** exposing sensitive 
   corporate information

Without MDM, a single lost phone or disgruntled employee 
can expose an entire organization's data.

---

## Environment
- **Tool:** ManageEngine Mobile Device Manager Plus (Cloud)
- **Devices:** 3 real Android devices
- **Enrollment Type:** BYOD (Bring Your Own Device)
- **Integration:** Managed Google Play (Non-Workspace)

---

## Scenarios Covered

| # | Scenario | Status |
|---|---|---|
| 01 | Enrollment Configuration & Security Decisions | ✅ Done |
| 02 | BYOD Work Profile Setup & Android Enterprise | ✅ Done |
| 03 | Data Loss Prevention (DLP) Policy | ✅ Done |
| 04 | The Analog Hole Problem & Solutions | ✅ Done |
| 05 | Managed Google Play & App Distribution | ✅ Done |
| 06 | Dynamic Grouping & Policy Automation | ✅ Done |
| 07 | COPE vs BYOD — Device Ownership Comparison | ✅ Done |

---

## Key Security Decisions Made

### Account Inactivity Policy
- **Setting:** 30-45 days
- **Reasoning:** Protects against orphaned accounts from 
  departed employees while accommodating vacation periods

### Session Validity
- **Setting:** 1 Day / 8-9 hour expiration
- **Reasoning:** Forces daily re-authentication. Prevents 
  stolen devices from maintaining active sessions over 
  weekends

### Concurrent Sessions
- **Setting:** 1-2 sessions
- **Reasoning:** Prevents credential sharing. Implements 
  Zero Trust principles at the session level

---

## Critical Problems Solved

### Problem 1 — Data Leakage (DLP)
**Threat:** Employee copies confidential work data and 
pastes into personal WhatsApp

**Solution:** Configured Workspace Security policy to 
restrict clipboard sharing between work and personal profiles

**Result:** Cross-profile data transfer blocked at OS level

---

### Problem 2 — The Analog Hole
**Threat:** Employee photographs screen with a second device

**Solution (3 layers):**
1. Screenshot restriction — forces use of second device, 
   reduces quality and speed
2. Dynamic Watermarking — overlays employee identity on 
   all documents, destroys incentive to leak
3. Acceptable Use Policy (AUP) — legal deterrent backed 
   by termination and legal action

---

### Problem 3 — BYOD vs COPE Camera Control
**Threat:** Employee uses camera to capture sensitive data

**Finding:** BYOD enrollment creates "Profile Owner" status 
— camera can only be disabled within the work sandbox, 
not globally

**Solution:** COPE enrollment creates "Device Owner" status 
— camera disabled globally across entire device

**Business recommendation:** High-security environments 
should use COPE not BYOD

---

## What I Learned
- BYOD and COPE are not just enrollment types — they define 
  the legal and technical boundary of IT control
- DLP is not a single setting — it's a layered strategy 
  combining technical controls, watermarking and legal policy
- The "Analog Hole" cannot be fully solved technically — 
  it requires a combination of technology, policy and law
- Zero Trust principles apply even at the session 
  management level
- MDM is only as strong as the policies behind it — 
  a lazy admin creates a false sense of security

---

## Tools Used
- ManageEngine Mobile Device Manager Plus (Cloud)
- Managed Google Play (Non-Workspace)
- Android Enterprise
- Real Android devices (×3)

---

## Repository Structure
MDM-Policy-Implementation/
├── README.md
├── 01-enrollment-configuration/
├── 02-BYOD-android-enterprise/
├── 03-DLP-policy/
├── 04-analog-hole-solutions/
├── 05-managed-google-play/
├── 06-dynamic-grouping/
├── 07-COPE-vs-BYOD/
└── screenshots/

---

## Author
**Jacob John**
Federal University of Technology Akure (FUTA)
Aspiring IT Support & SOC Analyst
[LinkedIn](#)
