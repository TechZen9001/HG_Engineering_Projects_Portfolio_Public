
# Recruiter Resources: Project 6. Manufacturing IT/OT Cyber-Physical Network – Secure, Segmented, & Resilient

Network Engineering • Cybersecurity • IT/OT Segmentation • Infrastructure Resilience • Manufacturing Operations

## Executive Overview

This directory provides a recruiter-focused summary of Project 6, highlighting practical manufacturing network engineering capabilities, IT/OT segmentation, cybersecurity, network resilience, Cisco IOS administration, technical validation, relevant career opportunities, and architecture decisions.

The project demonstrates a secure, segmented, and resilient manufacturing network proof of concept using Cisco Modeling Labs (CML). The architecture integrates six VLANs, IEEE 802.1Q trunking, controlled inter-VLAN routing, Access Control Lists (ACLs), Network Address Translation (NAT), Dynamic Host Configuration Protocol (DHCP), Rapid PVST+ redundancy, Network Time Protocol (NTP), and centralized Syslog monitoring.

The laboratory implementation successfully validated all seven network functionality requirements, including device reachability, guest network isolation, login banners, routing and external connectivity, Layer 2 redundancy, Syslog/NTP services, and VLAN operations.

The resources complement the detailed technical documentation available in the main project directory.

## Recruiter Resource Directory

| Section | Resource | Purpose |
|---|---|---|
| 6.10 | [60-Second Recruiter Dashboard](6.10%20Recruiter%20Dashboard.png) | Rapid executive overview of manufacturing network architecture, IT/OT segmentation, security, resilience, and business value |
| 6.11 | [Skills-to-Project Evidence Matrix](6.11%20Skills-to-Project%20Evidence%20Matrix.png) | Cisco IOS, VLANs, ACLs, routing, NAT, DHCP, Rapid PVST+, NTP, Syslog, and engineering skills mapped to project applications and evidence |
| 6.12 | [Career Roles Matrix](6.12%20Career%20Roles%20Matrix.png) | Professional roles and transferable skills in network engineering, cybersecurity, industrial networking, infrastructure security, and operational technology |
| 6.13 | [Architecture Decision Records](6.13%20Architecture%20Decision%20Records.png) | Manufacturing network architecture, segmentation strategy, security controls, redundancy design, alternatives, and engineering rationale |

## Recruiter Resource Infographics

### 6.10 — 60-Second Recruiter Dashboard

![Project 6 - Recruiter Dashboard](6.10%20Recruiter%20Dashboard.png)

### 6.11 — Skills-to-Project Evidence Matrix

![Project 6 - Skills-to-Project Evidence Matrix](6.11%20Skills-to-Project%20Evidence%20Matrix.png)

### 6.12 — Career Roles Matrix

![Project 6 - Career Roles Matrix](6.12%20Career%20Roles%20Matrix.png)

### 6.13 — Architecture Decision Records

![Project 6 - Architecture Decision Records](6.13%20Architecture%20Decision%20Records.png)

## Engineering Focus

| Domain | Demonstrated Project Capabilities |
|---|---|
| Network Engineering | Cisco IOS configuration, enterprise network design, switching, routing, IPv4 addressing, network connectivity, and infrastructure troubleshooting |
| Cybersecurity | Network segmentation, ACL enforcement, guest network isolation, restricted communication, secure administration, and security policy validation |
| IT/OT Network Segmentation | Separation of Corporate, Engineering, Operational Technology, Guest, Services, and Management network traffic |
| Manufacturing Network Architecture | Secure and resilient manufacturing network design using an edge router, redundant switches, corporate and guest endpoints, and centralized services |
| Cisco Modeling Labs (CML) | Design, implementation, simulation, troubleshooting, and validation of the manufacturing network topology |
| Cisco IOS Administration | Router and switch configuration, CLI diagnostics, interface verification, routing inspection, and network service management |
| VLAN Configuration | Six VLANs: VLAN 10 Corporate, VLAN 20 Engineering, VLAN 30 OT, VLAN 40 Guest, VLAN 50 Services, and VLAN 99 Management |
| IEEE 802.1Q Trunking | VLAN transport between switches and router uplinks, trunk configuration, allowed VLAN verification, and network segmentation |
| Inter-VLAN Routing | Router-on-a-stick architecture, IEEE 802.1Q subinterfaces, default gateways, and controlled communication between network segments |
| Access Control Lists (ACLs) | Policy-based traffic filtering, restricted guest access, permitted and denied traffic validation, and ACL counter verification |
| Guest Network Isolation | Prevention of unauthorized guest access to Corporate, Engineering, OT, Services, and Management resources |
| Network Address Translation (NAT) | Approved external connectivity, network address translation, and NAT translation verification |
| DHCP Services | Automated IPv4 address assignment for Corporate and Guest endpoints, DHCP pool configuration, and client address validation |
| Network Resilience | Redundant switching connectivity, alternate forwarding paths, failure testing, and service continuity validation |
| Rapid PVST+ | Spanning-tree root bridge configuration, Layer 2 loop prevention, redundant trunk management, and reconvergence verification |
| Infrastructure Monitoring | Centralized Syslog collection, operational event monitoring, network diagnostics, and security event visibility |
| Network Time Protocol (NTP) | Device time synchronization, NTP association verification, synchronized logging, and accurate event correlation |
| Syslog | Centralized network event collection, ACL deny logging, operational monitoring, and troubleshooting evidence |
| Secure Administration | Controlled administrative access, acceptable-use login banners, management network separation, and security-conscious configuration |
| Network Connectivity Testing | Endpoint addressing, gateway reachability, inter-VLAN communication, permitted external access, and unauthorized traffic denial |
| Security Policy Validation | ACL inspection, permit/deny testing, traffic counters, connectivity verification, and enforcement of network access restrictions |
| Layer 2 and Layer 3 Troubleshooting | VLAN membership, trunking, router subinterfaces, ACLs, NAT, DHCP, Rapid PVST+, NTP, and Syslog diagnostics |
| Network Failover Testing | Controlled switching-link failure simulation, spanning-tree reconvergence, alternate path verification, and connectivity preservation |
| Troubleshooting Methodology | Identify, Analyze, Isolate, Resolve, Validate, and Document workflow for connectivity, security, resilience, and infrastructure service issues |
| Infrastructure Services | DHCP, NAT, NTP, Syslog, centralized service configuration, and operational verification |
| Technical Documentation | Network topology diagrams, VLAN addressing plans, device configurations, CLI outputs, validation screenshots, troubleshooting records, and engineering evidence |
| Architecture | Segmented manufacturing network integrating R1, SW1, SW2, PC1, PC2, SRV1, six VLANs, ACL enforcement, redundant trunks, and centralized infrastructure services |
| Engineering Validation | Seven functional requirements successfully validated through Cisco Modeling Labs testing and documented technical evidence |
| Security and Privacy | Least-privilege principles, controlled access, sanitized network configurations, protected operational information, and responsible public portfolio documentation |
| Business Value | Reduced cybersecurity exposure, improved network resilience, stronger manufacturing reliability objectives, operational visibility, business continuity, and infrastructure scalability |

## Project Outcomes

| Key Performance Indicator | Validated Project Result |
|---|---|
| Network Simulation Platform | Cisco Modeling Labs (CML) |
| Functional Requirements | 7 of 7 successfully validated |
| Logical Network Segments | 6 VLANs configured |
| Core Network Devices | 1 router and 2 switches |
| Network Architecture | 5 core nodes plus an additional guest test endpoint |
| IT/OT Segmentation | Corporate, Engineering, OT, Guest, Services, and Management |
| Guest Network Security | ACL enforcement and guest isolation validated |
| Inter-VLAN Routing | Authorized network communication verified |
| External Connectivity | NAT operation and permitted external access verified |
| Layer 2 Redundancy | Rapid PVST+ root bridge selection, failover, and reconvergence validated |
| Infrastructure Services | DHCP, NTP, and Syslog validated |
| Network Monitoring | Centralized Syslog and synchronized timestamps verified |
| Technical Evidence | Cisco IOS CLI outputs, screenshots, network diagrams, and testing documentation |
| Final Project Status | Successfully completed and validated in the CML laboratory |
