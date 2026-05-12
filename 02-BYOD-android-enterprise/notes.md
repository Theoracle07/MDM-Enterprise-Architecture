# 02 — BYOD Setup & Android Enterprise Configuration

## Business Problem
Employees want to use personal devices for work. 
The company needs to secure corporate data without 
invading employee privacy.

## Solution
Enrolled devices under BYOD using Android Enterprise. 
This creates a secure "Work Profile" sandbox — a digital 
briefcase on the personal device.

## What BYOD Enrollment Creates
- A separate **Work Profile** controlled by IT
- Personal data completely untouched by MDM
- Work apps marked with a blue briefcase icon
- Two separate worlds on one device

## Android Enterprise Setup Steps
1. Navigate to **Enrollment** in ManageEngine dashboard
2. Under Android — click **Android Enterprise**
3. Select **Register without G Suite**
4. Sign in with dedicated Gmail account
5. Name your organization and complete registration
6. ManageEngine can now officially manage Android devices

## BYOD vs COPE — Key Difference

| | BYOD | COPE |
|---|---|---|
| Who owns phone | Employee | Company |
| MDM control level | Work profile only | Entire device |
| Camera control | Work apps only | Global |
| Privacy | High | Low |
| Security | Medium | High |
| Best for | Flexible workforce | High security environments |

## Lesson Learned
BYOD is not just an enrollment type — it defines the 
legal boundary of IT control. An admin cannot touch 
what they do not own. COPE gives full device ownership 
to the company — BYOD gives only sandbox ownership.
