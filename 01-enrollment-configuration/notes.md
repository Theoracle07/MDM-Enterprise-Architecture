# 01 — Enrollment Configuration & Security Decisions

## Business Problem
Before any device can be managed, the MDM system must be 
configured with the right security policies. Poor enrollment 
settings create gaps that attackers or disgruntled employees 
can exploit.

## Security Decisions Made

### 1. Account Inactivity
- **Setting:** 30-45 days
- **Business Reasoning:** Protects against orphaned accounts 
  from departed employees while accommodating staff on leave

### 2. Session Validity
- **Setting:** 1 Day
- **Business Reasoning:** Forces daily re-authentication. 
  Prevents stolen devices maintaining active sessions 
  over weekends

### 3. Session Expiration Time
- **Setting:** 8-9 hours
- **Business Reasoning:** Covers a full work shift. If a 
  laptop is stolen at 7PM the session has already expired

### 4. Concurrent Sessions
- **Setting:** 1 Session
- **Business Reasoning:** Prevents credential sharing. 
  Implements Zero Trust at session level

## Lesson Learned
Session management is not just a convenience setting
it is a Zero Trust security control. Every decision about 
how long a session lasts directly impacts the blast radius 
of a stolen credential.

