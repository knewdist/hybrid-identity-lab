# Proxmox Service Interruption – 2026-02-26

## Summary

During disk addition preparation for DC01 backup configuration, the Proxmox web interface became unresponsive and VMs were not reachable.

Host remained reachable via ping.

## Symptoms

- Proxmox web UI unavailable
- VMs not responding to network traffic
- Host IP responded to ping

## Investigation

Verified Proxmox services:

- pveproxy – running
- pvedaemon – running
- pve-cluster – running

Confirmed VMs via CLI:

qm list

DC01 and PAW01 were still running.

## Action Taken

Restarted pveproxy service:

systemctl restart pveproxy

Web interface restored.

No VM restarts required.

## Root Cause (Likely)

Transient pveproxy worker interruption or session instability.
Host services remained healthy.

## Lessons

- Always verify host availability before rebooting.
- Use CLI validation before assuming infrastructure failure.
- Separate web UI failure from hypervisor failure.
- Confirmed hypervisor stability before restarting services.
- Avoided unnecessary host reboot.

## Service Verification

### PVE Proxy Service Status
![pveproxy status](screenshots/ops-01-pveproxy-status.png)

### PVE Daemon Service Status
![pvedaemon status](screenshots/ops-02-pvedaemon-status.png)

### PVE Cluster Service Status
![pve-cluster status](screenshots/ops-03-pve-cluster-status.png)

## VM State Validation

Verified running virtual machines via CLI:

![qm list output](screenshots/ops-04-qm-list.png)


