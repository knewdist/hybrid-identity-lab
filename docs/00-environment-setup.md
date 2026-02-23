# Phase 0 — Environment Setup

## Objective
Build clean Windows Server lab infrastructure in Proxmox.

## Network Plan
Subnet: 192.168.1.0/24  
Gateway: 192.168.1.1  

| Machine | Role | IP |
|----------|------|------|
| DC01 | Domain Controller | 192.168.1.11 |
| FS01 | File Server | 192.168.1.21 |
| CL01 | Client | DHCP (initially) |

## VM Specs

### DC01
- 2 vCPU
- 4GB RAM
- 60GB Disk
- Intel E1000 NIC
- OVMF (UEFI)

## Validation
- Ping gateway
- Ping internet
- Confirm DNS resolution

## Notes
- VirtIO NIC initially failed — switched to Intel E1000.
