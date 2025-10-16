# Linux Host Firewall & Logging Lab (UFW + Journalctl)

## Description
This project demonstrates the setup, configuration, and verification of a firewall on an Ubuntu virtual machine using Uncomplicated Firewall (UFW).
The goal was to strengthen host-based defenses, document rule enforcement, and validate blocking behavior using real system logs and network tests.

##  Objectives
- Configure a secure virtual network environment using VirtualBox
- Enable and verify UFW firewall functionality
- Implement port-based allow rules (22, 80, 443)
- Block outbound DNS traffic (port 53) and ICMP pings to external addresses
- Enable logging and analysis of dropped packets
- Reset and restore firewall configuration to defaults

## Environment Setup
- **Platform:** Ubuntu 24.04 LTS (running in VirtualBox)
- **Network Mode:** NAT + Internal Network
- **Tools Used:** UFW, journalctl, ping, tail, nano
- **Skills Demonstrated:** Linux administration, network security, log analysis, firewall configuration

## Commands Used
```bash
sudo apt update && sudo apt upgrade -y
sudo ufw enable
sudo ufw allow 22/tcp
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw deny out to any port 53 proto udp
sudo ufw logging on
sudo journalctl -k | grep -i ufw
sudo ufw reset
`````
## Results
- Firewall enabled and active
- Allowed ports 22, 80, 443 verified
- Outbound DNS blocked successfully
- Logs confirmed blocked traffic
- Rules reset and restored defaults
