# Phase 4 – Tier Model Hardening

## Context

As the lab environment matured through Phase 3.1,
it became clear that administrative tooling and credential
placement needed to align with Microsoft's Tier Model.

Before expanding further (Azure integration, workstation
management, or hybrid identity), privilege boundaries must
be enforced.

This phase introduces formal tier separation.


---

## Tier 0 – Identity

Account:
- CORP\T0Admin

Group Membership:
- Domain Admins

Purpose:
- Manage Domain Controllers
- Manage Active Directory
- Tier 0 systems only

Security Principle:
- Never logs into Tier 1 or Tier 2 systems

---

## Tier 1 – Servers

Security Group:
- GG_T1_Server_Admins

Account:
- CORP\T1Admin

Purpose:
- Manage member servers
- No Domain Admin privileges
- No DC logon rights

---

## Tier 2 – Workstations

Security Group:
- GG_T2_Helpdesk

Account:
- CORP\HelpdeskT2

Purpose:
- Manage workstation configuration
- Reset standard user passwords (delegated later)
- No server or DC access

---

## Design Notes

- Administrative groups are isolated in `OU=Admin\Groups`
- Administrative users are isolated in `OU=Admin\Users`
- Resource groups remain in `OU=Groups`
- Separation prepares environment for:
  - Logon restrictions
  - GPO scoping
  - Privileged Access Workstation (PAW)
  - Azure AD Connect (future Tier 0 system)

---

## Validation

Screenshots captured:
- Admin OU structure
- Tier admin group creation
- Tier admin user placement

### Evidence

![Admin OU Structure](../screenshots/phase1/01-admin-ou-structure.png)
![Admin Groups](../screenshots/phase1/02-admin-groups.png)
![Admin Users](../screenshots/phase1/03-admin-users.png)
