# Phase 1 — Domain Controller Deployment

## Objective
Promote Windows Server 2025 to Domain Controller.

## Steps
1. Installed AD DS role
2. Ran Install-ADDSForest
3. Created domain: corp.local
4. Installed DNS role automatically

## Domain Info
Domain Name: corp.local  
NetBIOS Name: CORP  

## Observations
- First promotion attempt failed due to PowerShell multiline paste issue.
- Re-ran Install-ADDSForest interactively.

## Validation
- Logged in as CORP\Administrator
- Verified DNS configuration
- Confirmed DNS points to 127.0.0.1
- Verified domain with Get-ADDomain
- Verified forest with Get-ADForest
