# 00 - Network Topology Diagram

## Goal
Provide a single visual reference tying together the network layout, firewall/VPN architecture, and Active Directory structure built across the project.

## Diagram
![Network Topology and AD Structure](network-topology.svg)

## Summary

**Network layer:** All internal traffic runs on the `vboxnet0` Host-Only network (192.168.56.0/24). **pfSense** sits between this network and the internet, acting as the single gateway — every machine's traffic to the outside world passes through it, replacing the earlier per-VM direct NAT setup. DC01 and FILE01 use static IPs (100-109 range); CLIENT01 and CLIENT02 receive dynamic IPs from the DHCP scope (110-200 range), with pfSense's LAN address (192.168.56.254) pushed to all clients as their default gateway.

**Firewall layer:** pfSense enforces a Default-Deny outbound policy — nothing leaves the network unless explicitly allowed. Only DC01 can reach external DNS (53) and NTP (123) servers; all LAN hosts can use HTTPS (443), HTTP (80), and ICMP (ping). Everything else is blocked by a catch-all rule at the bottom of the rule set.

**Remote access layer:** A remote user connects via OpenVPN (UDP 1194) into a dedicated tunnel network (10.10.10.0/24). Following least-privilege principles, the VPN user is pinned to a fixed tunnel IP and can only reach CLIENT02 on port 3389 (RDP) — no other host on the network is reachable through the tunnel. RDP is never exposed directly to the internet.

**AD layer:** Four Organizational Units (IT, HR, Finance, Management) each contain a dedicated security group and user. File access and mapped drives are scoped per department through NTFS/Share permissions and a single Mapped Drives GPO using Item-Level Targeting.

**GPOs:**
- Domain-wide: Password Policy, Login Banner, Mapped Drives (targeted per department)
- HR / Finance / Management: Disable Control Panel, USB storage disabled
- IT: no extra restrictions — full local access required for support work
