# 03 — Data Loss Prevention (DLP) Policy

## Business Problem
An employee opens a confidential work email, copies 
the text, opens personal WhatsApp and sends it to 
a competitor.

Without DLP controls this happens silently with 
no trace.

## Threat
**Cross-profile data leakage**: corporate data 
moving from the secured work profile into the 
unsecured personal profile through the clipboard.

## Solution
Configured a Workspace Security policy in ManageEngine 
to block clipboard sharing between work and personal 
profiles.

## Implementation Steps
1. Click **Device Management** → **Profiles**
2. Click **Create Profile** → **Android**
3. Name it `DLP-Security-Policy`
4. Navigate to **Workspace Security** on left menu
5. Find **Allow users to cut/copy/paste managed 
   data to unmanaged apps**
6. Set to **Restrict**
7. Save and Publish
8. Assign profile to enrolled devices

## Result
When employee attempts to paste work data into 
personal WhatsApp — action is blocked with 
"Action not allowed" message.

## Business Impact
**Without this policy:** Employee can silently 
exfiltrate data in seconds with no technical trace.

**With this policy:** Cross-profile data transfer 
is blocked at OS level. Any attempt is logged.

## Lesson Learned
DLP is not one setting it is a layered strategy. 
This clipboard restriction is Layer 1. Without it, 
every other security control can be bypassed in 
seconds by copy and paste.
