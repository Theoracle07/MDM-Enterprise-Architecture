# 06 — User Groups & Policy Automation

## Business Problem
A company has employees across different departments 
— Sales, IT, HR, Finance.

Each department needs different apps and security 
policies.

Manually assigning policies to each user one by one is:
- Time consuming
- Error prone
- Unscalable

## Solution
Implemented User Groups to automate policy deployment 
based on department and role.

When a new employee enrolls their device — they are 
added to their department group and automatically 
receive the correct apps and security policies 
immediately. Zero manual IT intervention.

## What User Groups Enable
- Automatically assigns policies based on who the 
  user is — not just what device they have
- One user can have multiple devices — all receive 
  the same group policies
- Department change = update user group = all devices 
  update automatically
- Eliminates manual per-device configuration

## Example Group Structure

| Group | Users | Apps Pushed | Policies Applied |
|---|---|---|---|
| Sales | Sales staff | CRM, Email, Teams | Standard DLP |
| IT Admin | IT team | Network tools, MDM console | Full access |
| HR | HR staff | HRIS, Email | Strict DLP |
| Finance | Finance staff | Accounting software | Strictest DLP |

## Implementation Steps
1. Navigate to **User Management** → **User Groups**
2. Click **Create Group**
3. Name the group — example: "Sales Team"
4. Define membership criteria — department, role
5. Assign apps and profiles to the group
6. Add users to the group
7. All enrolled devices of those users receive 
   policies automatically

## User Group vs Device Group

| | User Group | Device Group |
|---|---|---|
| Based on | Who the person is | What device it is |
| Best for | Policy by role/department | Policy by device type |
| Example | All Sales staff get CRM | All iPads get iOS policy |
| More common in enterprise | ✅ Yes | Situational |

## Business Impact
**Without User Groups:** IT manually configures each 
device. One mistake means wrong policies on wrong 
devices — a security gap.

**With User Groups:** Every user gets exactly the 
right configuration automatically regardless of 
how many devices they enroll. No human error. 
No delays. No gaps.

## Technical Phrasing for Resume/LinkedIn
*"Implemented User Group based policy automation 
to ensure new employees receive departmental 
security configurations and application suites 
immediately upon enrollment, reducing manual 
IT overhead and eliminating configuration errors."*

## Lesson Learned
Policies should follow the user — not the device. 
A salesperson can have a phone, a tablet and a 
laptop. Managing three separate devices manually 
is three times the work and three times the risk 
of error.

User Groups make security scalable. That is the 
foundation of enterprise IT operations.
