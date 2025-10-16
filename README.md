# Linux Host Firewall & Logging Lab (UFW + Journalctl)

## Description
Harden a Linux host using **UFW** (Uncomplicated Firewall), enable detailed logging, create/verify custom rules (e.g., **block DNS egress**), and analyze events with `journalctl` and `/var/log/ufw.log`.

## Languages Used
 - Bash
## Utilities Used
 - **Oracle Virtual Box:** virtual machines running Ubuntu Linux

 ##  Lab Stack
- Ubuntu Server 22.04+ (works on 20.04)
- UFW, iptables (under the hood), rsyslog
- Tools: `ping`, `curl`, `dig`/`nslookup`, `journalctl`

##  Objectives
- Default-deny inbound; allow essential services
- Enforce **egress control** (block DNS as example)
- Turn on **UFW logging** and validate with real traffic
- Document tests, findings, and remediation steps



##  Prereqs
```bash
sudo apt update && sudo apt install -y ufw dnsutils curl
