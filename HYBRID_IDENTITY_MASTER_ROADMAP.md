# Hybrid Identity Lab – Master Roadmap

---

## 🔹 Current Lab Environment

## 🖥️ Deployed Infrastructure

🟩 **DC01** – Domain Controller (AD DS + DNS)  
🟩 **FS01** – File Server  
🟩 **PAW01** – Privileged Access Workstation  
🟩 **CL01** – Domain-Joined Windows 11 Client  

---

# Phase A – Core Identity Deployment

🟩 **Status: Core AD Infrastructure Operational**

☑️ AD DS deployed  
☑️ DNS integrated  
☑️ Domain functional level configured  
☑️ Windows 11 joined to domain  

⬜ Multi-DC replication  
⬜ FSMO role documentation  
⬜ DC health validation  

---

# Phase B – Administrative Tier Model

🟩 **Status: Tier Architecture Designed**

☑️ Tier accounts created  
☑️ Tier boundaries identified  
☑️ PAW01 deployed  

⬜ Enforced logon restrictions via GPO  
⬜ Deny policy validation testing  
⬜ Protected Users group configuration  
⬜ PAW hardening baseline  

---

# Phase C – Authentication & Kerberos

🟩 **Status: Authentication Flow Understood**

☑️ Kerberos TGT lifecycle mapped  
☑️ PAC structure understood  
☑️ Ticket purge & validation tested  

⬜ Constrained delegation lab  
⬜ Unconstrained delegation comparison  
⬜ Authentication event log deep analysis  
⬜ Ticket lifetime tuning  
⬜ Golden/Silver ticket theory documentation  

---

# Phase D – Domain Controller Operations

🟥 **Status: Not Yet Implemented**

⬜ FSMO role review  
⬜ System State backup  
⬜ Authoritative restore simulation  
⬜ Replication validation  
⬜ DC health baseline report  

---

# Phase E – Group Policy Governance

🟥 **Status: Not Yet Implemented**

⬜ Baseline workstation GPO  
⬜ Tier enforcement GPO  
⬜ Admin logon restriction GPO  
⬜ Audit policy GPO  
⬜ Central store implementation  

---

# Phase F – Secure Windows Server

🟥 **Status: Not Yet Implemented**

⬜ Harden DC01  
⬜ Harden FS01  
⬜ Remove legacy protocols  
⬜ Local security policy audit  

---

# Phase G – Hybrid Identity Integration

🟥 **Status: Not Yet Implemented**

⬜ Deploy Azure AD Connect  
⬜ Sync users  
⬜ Validate hybrid authentication  
⬜ Compare Kerberos vs JWT token flow  

---

# Phase H – Cloud Identity Security

🟥 **Status: Not Yet Implemented**

⬜ Implement MFA  
⬜ Create Conditional Access policy  
⬜ Azure RBAC testing  
⬜ Zero Trust validation  

---

# Phase I – Monitoring & Threat Detection

🟥 **Status: Not Yet Implemented**

⬜ Review DC security logs  
⬜ Track failed logons  
⬜ Hybrid sign-in logs review  
⬜ Audit policy validation  

---

# 🧠 Design Principle

Identity is the security boundary.

This lab is structured in progressive security layers:

1. Identity Architecture  
2. Boundary Enforcement  
3. Authentication Understanding  
4. Operational Resilience  
5. Policy Control  
6. Hybrid Expansion  
7. Security Hardening  

---

**End of Master Roadmap**
