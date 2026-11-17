# Enterprise Network Infrastructure

## Overview

This project consists of a simulated enterprise network infrastructure developed using Cisco Packet Tracer.

The objective was to design, configure, and validate a segmented network environment with multiple departments, centralized services, and dedicated network management.

## Network Architecture

The infrastructure follows a hierarchical star topology with:

- 1 Cisco 2911 Router
- 1 Core Switch
- 3 Access Switches
- Multiple workstations and printers
- 3 Internal Servers

## Network Segmentation

The network is divided into eight VLANs:

| VLAN | Department | Network |
|---|---|---|
| 10 | Administrative | 192.168.10.0/24 |
| 20 | IT | 192.168.20.0/24 |
| 30 | Operations | 192.168.30.0/24 |
| 40 | Finance | 192.168.40.0/24 |
| 50 | Servers | 192.168.50.0/24 |
| 60 | Printers | 192.168.60.0/24 |
| 70 | Guests | 192.168.70.0/24 |
| 99 | Management | 192.168.99.0/24 |

## Implemented Services

### Inter-VLAN Routing
- Router-on-a-Stick architecture
- IEEE 802.1Q trunk links
- Dedicated gateway for each VLAN

### DHCP
- Dynamic IPv4 address allocation
- Configured pools for user VLANs
- DNS and default gateway distribution

### FTP Server
- Individual user accounts
- Different file permissions
- Upload, download, listing, deletion and rename permission tests

### DNS Server
- Internal DNS records
- Name resolution for internal servers
- DNS alias for the FTP server

### HTTP Server
- Internal corporate dashboard
- Basic infrastructure and financial demonstration information

### Network Management
- Dedicated Management VLAN (99)
- Static management addresses for switches
- Dedicated management workstation

## Validation

Connectivity and service tests included:

- DHCP address renewal and verification
- DNS name resolution using `nslookup`
- Inter-VLAN connectivity using `ping`
- FTP authentication and permission testing
- HTTP dashboard accessibility
- Management connectivity to switches and servers

## Tools

- Cisco Packet Tracer
- Cisco IOS CLI
- IPv4
- VLANs
- DHCP
- DNS
- FTP
- HTTP

## Project Files

- `packet-tracer/`: Network simulation file.
- `documentation/`: Technical implementation documentation.
- `screenshots/`: Selected configuration and validation evidence.

## Scope and Limitations

This project represents a functional network infrastructure simulation.

Advanced inter-VLAN ACL policies, guest network isolation, and stateful firewall controls were not implemented in this version.

The dashboard uses demonstration data and does not connect to real financial market services.

## Author

H-Augusto
