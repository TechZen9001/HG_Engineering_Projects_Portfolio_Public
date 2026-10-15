# Project 6 — Manufacturing IT / OT Cyber-Physical Network: Secure, Segmented, & Resilient

**Visual Engineering Portfolio | Cisco Networking • IT/OT Security • VLAN Segmentation • Network Resilience • Industrial Infrastructure**

Welcome to the visual documentation library for Project 6. This directory contains eight professional infographics summarizing the project's business value, technical architecture, engineering methodology, implementation, and results.

Each infographic corresponds to a detailed Markdown document in the parent project directory.

---

## Featured Project Overview

![Project 6 — Executive Overview](6.2%20Executive-Overview%20A.png)

**Project Objective:** Design, implement, secure, and validate a segmented manufacturing network that protects operational technology (OT) resources, enables controlled communication between network segments, provides resilient connectivity, and supports centralized network monitoring and business continuity.

**Engineering Focus:** Cisco IOS, VLAN segmentation, IEEE 802.1Q trunking, router-on-a-stick inter-VLAN routing, Access Control Lists (ACLs), Network Address Translation (NAT), Dynamic Host Configuration Protocol (DHCP), Rapid PVST+, Network Time Protocol (NTP), Syslog, network troubleshooting, and infrastructure validation.

**Business Focus:** Manufacturing availability, cybersecurity risk reduction, reduced operational costs, business continuity, increased productivity, resilient infrastructure, and scalable industrial network operations.

---

## Infographic Directory

| Section | Infographic | Detailed Documentation |
|---|---|---|
| 6.2 Executive Overview | [View Infographic](6.2%20Executive-Overview%20A.png) | [Read Documentation](../6.2%20Executive-Overview.md) |
| 6.3 Business Value | [View Infographic](6.3%20Business-Value%20A.png) | [Read Documentation](../6.3%20Business-Value.md) |
| 6.4 Technical Value | [View Infographic](6.4%20Technical-Value%20A.png) | [Read Documentation](../6.4%20Technical-Value.md) |
| 6.5 Solution Architecture | [View Infographic](6.5%20Solution-Architecture.png) | [Read Documentation](../6.5%20Solution-Architecture.md) |
| 6.6 Troubleshooting Workflow | [View Infographic](6.6%20Simplified-Troubleshooting-Workflow.png) | [Read Documentation](../6.6%20Simplified-Troubleshooting-Workflow.md) |
| 6.7 Tools Used | [View Infographic](6.7%20Tools-Used.png) | [Read Documentation](../6.7%20Tools-Used.md) |
| 6.8 Simplified Implementation | [View Infographic](6.8%20Simplified-Implementation.png) | [Read Documentation](../6.8%20Simplified-Implementation.md) |
| 6.9 Project Outcomes | [View Infographic](6.9%20Project-Outcomes%20A.png) | [Read Documentation](../6.9%20Project-Outcomes.md) |

---

## Engineering Capabilities Demonstrated

1. **Enterprise Network Architecture Design:** Design a hierarchical manufacturing network using an edge router, primary and secondary switches, corporate endpoints, infrastructure services, and a restricted guest test endpoint.
2. **IT/OT Network Segmentation:** Separate corporate, engineering, operational technology, guest, services, and management traffic into distinct VLANs.
3. **VLAN Configuration:** Create and manage six logical network segments with structured IPv4 addressing.
4. **IEEE 802.1Q Trunking:** Configure trunk links to transport multiple VLANs between network devices.
5. **Router-on-a-Stick Inter-VLAN Routing:** Configure router subinterfaces and default gateways to enable controlled communication between VLANs.
6. **IPv4 Subnetting and Addressing:** Design and implement consistent IP addressing across network segments.
7. **ACL Design and Enforcement:** Configure and validate security policies that restrict unauthorized communication.
8. **Guest Network Isolation:** Prevent guest endpoints from accessing protected corporate, engineering, OT, services, and management resources.
9. **NAT Configuration and Verification:** Enable approved external connectivity and verify address translations.
10. **DHCP Service Configuration:** Automate IP address allocation for corporate and guest endpoints.
11. **Rapid PVST+ Implementation:** Configure Layer 2 spanning-tree operations to prevent switching loops.
12. **Layer 2 Redundancy and Failover Testing:** Establish redundant switching links, verify root bridge selection, simulate link failures, and validate reconvergence.
13. **Syslog Configuration and Validation:** Centralize network event logging to support troubleshooting, monitoring, and security investigations.
14. **NTP Configuration and Synchronization:** Maintain synchronized network device timestamps for accurate event correlation.
15. **Secure Network Device Administration:** Apply controlled administrative access and acceptable-use login banners.
16. **Cisco IOS CLI Proficiency:** Configure, troubleshoot, and validate network infrastructure using Cisco IOS commands.
17. **Layer 2 and Layer 3 Troubleshooting:** Investigate VLAN, trunking, routing, ACL, NAT, DHCP, and spanning-tree issues.
18. **Network Connectivity Testing:** Validate endpoint addressing, default gateway connectivity, authorized inter-VLAN communication, and external network access.
19. **Security Policy Validation:** Verify permitted and denied traffic using connectivity tests, ACL counters, and network logs.
20. **Technical Documentation and Evidence Collection:** Produce network diagrams, configuration records, CLI outputs, screenshots, troubleshooting documentation, and validation reports.

---

## Manufacturing Network Architecture

Project 6 implements a five-node core manufacturing network with an additional guest endpoint for security testing.

### Network Components

| Component | Role | Primary Function |
|---|---|---|
| R1 | Edge/Perimeter Router | Inter-VLAN routing, ACL enforcement, NAT, DHCP, NTP, and Syslog forwarding. |
| SW1 | Primary Layer 2 Switch | VLAN switching, 802.1Q trunking, Rapid PVST+ root bridge, and corporate/services connectivity. |
| SW2 | Secondary Layer 2 Switch | Redundant switching, Rapid PVST+ participation, and guest endpoint connectivity. |
| PC1 | Corporate Workstation | Validates DHCP, gateway connectivity, authorized inter-VLAN communication, and external access. |
| SRV1 | Services Server | Provides centralized infrastructure services, including Syslog and NTP. |
| PC2 | Guest Test Endpoint | Validates guest isolation, ACL enforcement, and permitted external connectivity. |

### VLAN and IP Addressing Plan

| VLAN | Network Segment | IPv4 Subnet | Primary Purpose |
|---|---|---|---|
| 10 | Corporate | 10.10.10.0/24 | Corporate IT and administration. |
| 20 | Engineering | 10.10.20.0/24 | Engineering systems and applications. |
| 30 | OT | 10.10.30.0/24 | Operational technology and manufacturing systems. |
| 40 | Guest | 10.10.40.0/24 | Restricted guest connectivity. |
| 50 | Services | 10.10.50.0/24 | Infrastructure and network services. |
| 99 | Management | 10.10.99.0/24 | Network device management. |

R1 provides the corresponding `.1` default gateway addresses through router subinterfaces.

The network uses redundant IEEE 802.1Q trunk links between SW1 and SW2. Rapid PVST+ provides loop prevention and alternate forwarding path support when a switching link fails.

**Architecture Scope:** The implementation was developed and validated in Cisco Modeling Labs (CML). It demonstrates core IT/OT segmentation and network resilience principles but does not represent a complete production industrial control system architecture.

---

## Enterprise Business and Financial Value

Project 6 demonstrates how secure manufacturing network segmentation, controlled connectivity, redundant switching, and centralized monitoring can support operational availability, cybersecurity risk reduction, and business continuity.

### Illustrative Enterprise Financial Scenario

| Business Metric | Enterprise Estimate |
|---|---|
| Annual Operational Cost Savings | $2.1 million |
| Annual Avoided Downtime Costs | $3.8 million |
| Combined Annual Financial Value | $5.9 million |
| Production Uptime Target | 99.9% |
| Annual Engineering Time Savings | 2,800 IT hours |
| Illustrative First-Year ROI | 250% |
| Illustrative Payback Period | Approximately 5 months |

**Financial Disclosure:** These figures are illustrative enterprise-scale estimates used to demonstrate potential financial impact. They are not actual financial results measured in the Cisco Modeling Labs environment.

The combined $5.9 million represents modeled annual operational savings and avoided downtime costs before implementation and operating expenses. The 99.9% production uptime figure represents a hypothetical enterprise target, not a measured production availability result.

The ROI and payback figures are scenario assumptions and require a consistent investment, cash-flow, and benefit-realization model before use in a formal financial business case.

### Strategic Business Benefits

1. **Secure IT/OT Network Segmentation:** Reduce exposure between corporate IT networks and industrial operational technology systems.
2. **Stronger Cybersecurity Posture:** Restrict unauthorized communication and reduce opportunities for lateral movement.
3. **Higher Network Availability:** Use redundant switching paths to reduce dependence on individual network links.
4. **Business Continuity and Disaster Resilience:** Support reliable access to manufacturing services and recovery from connectivity failures.
5. **Reduced Operational Costs:** Improve troubleshooting efficiency and help prevent costly network outages and security incidents.
6. **Greater Operational Efficiency:** Standardize network configurations, centralize event logging, and simplify troubleshooting.
7. **Security Governance and Compliance Readiness:** Maintain documented access controls, network policies, monitoring records, and validation evidence.
8. **Scalable Manufacturing Infrastructure:** Use modular VLAN-based architecture to support additional devices, services, and network segments.
9. **Improved Manufacturing Reliability and Growth:** Combine secure segmentation, resilient connectivity, and operational visibility to support dependable manufacturing operations and future expansion.

---

### Production IT/OT Security Considerations

A production manufacturing environment would require additional controls appropriate to its industrial systems, operational risks, and safety requirements. These may include industrial firewalls, IT/OT demilitarized zones (DMZs), restricted remote access, asset inventories, industrial protocol monitoring, backup and recovery procedures, and alignment with relevant industrial cybersecurity frameworks such as IEC 62443 and NIST SP 800-82. These production considerations extend beyond the scope of the simulated five-node core network.

---

## Project Results and Validation

The Cisco Modeling Labs proof of concept demonstrated the implementation and validation of the project's seven functional requirements.

| Validation Category | Project Result |
|---|---|
| Device Discovery and Reachability | Endpoint addressing and authorized connectivity verified. |
| Guest Network Security | ACL restrictions and guest isolation validated. |
| Login Banners | Acceptable-use banners configured on network devices. |
| Routing and External Connectivity | Inter-VLAN routing and NAT operation verified. |
| Layer 2 Redundancy | Rapid PVST+ failover and reconvergence validated. |
| Syslog and NTP | Centralized logging and time synchronization verified. |
| VLANs and IEEE 802.1Q | Six VLANs, trunk connectivity, and VLAN operations validated. |

**Final Laboratory Result:** Seven functional requirements validated, six logical network segments configured, three core network devices deployed, and a redundant Layer 2 switching design tested.

---

*Manufacturing IT/OT Cyber-Physical Network — Secure Segmentation, Resilient Infrastructure, Reliable Operations, and Enterprise Business Value.*
