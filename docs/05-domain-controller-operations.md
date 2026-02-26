## 5.1 FSMO Role Verification

### CLI Verification

Command executed:

netdom query fsmo

Result:

- Schema master: DC01.corp.local
- Domain naming master: DC01.corp.local
- PDC: DC01.corp.local
- RID pool manager: DC01.corp.local
- Infrastructure master: DC01.corp.local

#### Evidence
![FSMO CLI Output](../screenshots/05/01-fsmo-cli.png)

---

### GUI Verification – Domain Roles

Verified via:
Active Directory Users and Computers  
corp.local → Right-click → Operations Masters

Tabs validated:
- RID
- PDC
- Infrastructure

Each confirmed: DC01.corp.local

#### Evidence
![RID Role](../screenshots/05/02-rid-role.png)
![PDC Role](../screenshots/05/03-pdc-role.png)
![Infrastructure Role](../screenshots/05/04-infrastructure-role.png)

---

### GUI Verification – Forest Role

Verified via:
Active Directory Domains and Trusts  
Right-click → Operations Master

Confirmed:
Domain Naming Master → DC01.corp.local

#### Evidence
![Domain Naming Master](../screenshots/05/05-domain-naming-role.png)

---

### Summary

All FSMO roles are held by DC01 as expected in a single-domain-controller lab environment.

DC01 currently functions as:
- Forest authority
- Domain authority
- RID allocator
- Time authority (PDC Emulator)
- Authentication authority
