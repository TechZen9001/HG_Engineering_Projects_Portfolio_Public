# Project 6 – Manufacturing IT / OT Cyber-Physical Network: Secure, Segmented, & Resilient 

**Network Engineering • Cybersecurity • IT/OT Segmentation • Infrastructure Resilience • Manufacturing Operations**

**Design • Secure • Segment • Validate • Ensure Uptime**

Project 6 demonstrates the design, implementation, configuration, troubleshooting, and validation of a secure, segmented, and resilient manufacturing IT/OT network using Cisco networking technologies. The solution was implemented in Cisco Modeling Labs (CML) and integrates VLAN segmentation, IEEE 802.1Q trunking, router-on-a-stick inter-VLAN routing, Access Control Lists (ACLs), Network Address Translation (NAT), Dynamic Host Configuration Protocol (DHCP), Rapid PVST+, Network Time Protocol (NTP), and centralized Syslog monitoring. The project demonstrates practical competencies in enterprise networking, industrial network security, controlled access, network resilience, infrastructure services, troubleshooting, and evidence-based engineering validation.

![Project 6 – Manufacturing IT/OT Cyber-Physical Network](6.%20Manufacturing%20IT%20OT%20Cyber-Physical%20Network.png)

Engineering Lifecycle: Design → Build → Configure → Secure → Monitor → Test → Validate → Document.

## Project Documentation

| Section | Documentation | Detailed Guide | Infographic |
|---|---|---|---|
| 6.2 | Executive Overview | [Read Documentation](6.2%20Executive-Overview.md) | [View Infographic](infographics/6.2%20Executive-Overview%20A.png) |
| 6.3 | Business Value | [Read Documentation](6.3%20Business-Value.md) | [View Infographic](infographics/6.3%20Business-Value%20A.png) |
| 6.4 | Technical Value | [Read Documentation](6.4%20Technical-Value.md) | [View Infographic](infographics/6.4%20Technical-Value%20A.png) |
| 6.5 | Solution Architecture | [Read Documentation](6.5%20Solution-Architecture.md) | [View Infographic](infographics/6.5%20Solution-Architecture.png) |
| 6.6 | Simplified Troubleshooting Workflow | [Read Documentation](6.6%20Simplified-Troubleshooting-Workflow.md) | [View Infographic](infographics/6.6%20Simplified-Troubleshooting-Workflow.png) |
| 6.7 | Tools Used | [Read Documentation](6.7%20Tools-Used.md) | [View Infographic](infographics/6.7%20Tools-Used.png) |
| 6.8 | Simplified Implementation | [Read Documentation](6.8%20Simplified-Implementation.md) | [View Infographic](infographics/6.8%20Simplified-Implementation.png) |
| 6.9 | Project Outcomes | [Read Documentation](6.9%20Project-Outcomes.md) | [View Infographic](infographics/6.9%20Project-Outcomes%20A.png) |

## 6.2 Executive Overview

### Business Challenge

Manufacturing organizations depend on reliable network connectivity to support corporate applications, engineering systems, operational technology, and critical production services. Inadequate segmentation, inconsistent security controls, network failures, and limited operational visibility can expose these environments to cybersecurity incidents and service disruptions.

| Business Challenge                            | Operational Impact                                                         | Business Risk                                                  |
| --------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------- |
| Inadequate IT/OT Segmentation                 | Unnecessary communication between business and industrial network segments | Increased exposure of sensitive manufacturing resources        |
| Cybersecurity Exposure                        | Unauthorized access and opportunities for lateral movement                 | Potential security incidents and production disruptions        |
| Network Failures and Single Points of Failure | Loss of critical connectivity following device or link failures            | Reduced availability and business continuity                   |
| Inconsistent Security Controls                | Missing or incorrectly enforced network access policies                    | Unauthorized access or disruption of legitimate traffic        |
| Limited Network Visibility                    | Insufficient logging and inconsistent timestamps                           | Slower incident investigation and troubleshooting              |
| Manual Troubleshooting                        | Repetitive configuration inspection and fault isolation                    | Increased engineering effort and operational costs             |
| Infrastructure Growth                         | More network segments, devices, and operational requirements               | Increased administrative complexity and scalability challenges |

### Technical Solution

| Solution Component    | Engineering Implementation                                                        | Primary Value                             |
| --------------------- | --------------------------------------------------------------------------------- | ----------------------------------------- |
| VLAN Segmentation     | Six logical VLANs for Corporate, Engineering, OT, Guest, Services, and Management | Logical network separation                |
| IEEE 802.1Q Trunking  | Tagged VLAN connections between R1–SW1 and SW1–SW2                                | Multi-VLAN connectivity                   |
| Router-on-a-Stick     | R1 router subinterfaces and VLAN gateways                                         | Controlled inter-VLAN routing             |
| ACL Enforcement       | Restrict Guest VLAN 40 access to protected internal networks                      | Security policy enforcement               |
| NAT                   | Translate approved internal traffic for external access                           | Controlled external connectivity          |
| DHCP                  | Automatic addressing for Corporate and Guest endpoints                            | Simplified endpoint provisioning          |
| Rapid PVST+           | SW1 root bridge and redundant inter-switch trunks                                 | Loop prevention and link-failure recovery |
| NTP and Syslog        | Time synchronization and centralized event collection using SRV1                  | Monitoring and event correlation          |
| Structured Validation | CLI diagnostics, connectivity tests, ACL counters, and failover testing           | Documented engineering evidence           |

### Project Scope

| Category                  | Project Specification                                                                   |
| ------------------------- | --------------------------------------------------------------------------------------- |
| Primary Objective         | Implement a secure, reliable, and scalable manufacturing network proof of concept       |
| Engineering Platform      | Cisco Modeling Labs (CML)                                                               |
| Core Network              | R1, SW1, SW2, PC1, and SRV1                                                             |
| Additional Test Endpoint  | PC2 — Guest                                                                             |
| Network Segments          | Six VLANs                                                                               |
| Security Objective        | Protect internal resources through segmentation and controlled access                   |
| Availability Objective    | Validate redundant Layer 2 connectivity and Rapid PVST+ reconvergence                   |
| Monitoring Objective      | Centralized Syslog and synchronized NTP timestamps                                      |
| Validation Objective      | Successfully verify all seven functionality requirements                                |
| Production Classification | Simulated network proof of concept, not a complete production industrial control system |

### Executive Results

| Key Performance Indicator   | Validated Result                              |
| --------------------------- | --------------------------------------------- |
| Functional Requirements     | 7 of 7 validated                              |
| Logical VLAN Segments       | 6                                             |
| Core Network Devices        | 3 — R1, SW1, SW2                              |
| Network Topology            | 5 core nodes + 1 guest test endpoint          |
| Validated Redundancy Design | 1 — Redundant SW1–SW2 trunks with Rapid PVST+ |
| Project Status              | Completed Successfully — Cisco Modeling Labs  |

## 6.3 Business Value

The manufacturing network architecture demonstrates how secure segmentation, controlled routing, redundant connectivity, and centralized monitoring can improve operational reliability and reduce cybersecurity exposure.

### Strategic Business Benefits

| # | Business Benefit                             | Technical Enabler                                             | Enterprise Value                                                            |
| - | -------------------------------------------- | ------------------------------------------------------------- | --------------------------------------------------------------------------- |
| 1 | Secure IT/OT Segmentation                    | Six VLANs and controlled inter-VLAN routing                   | Reduces unnecessary communication between corporate and industrial networks |
| 2 | Stronger Cybersecurity Posture               | ACL enforcement, guest isolation, and defense in depth        | Restricts unauthorized access and lateral movement opportunities            |
| 3 | Higher Network Availability                  | Redundant IEEE 802.1Q trunks and Rapid PVST+                  | Reduces dependence on individual switching links                            |
| 4 | Business Continuity and Disaster Resilience  | Validated link failover and documented recovery procedures    | Supports connectivity during selected network disruptions                   |
| 5 | Reduced Operational Costs                    | Standardized configurations, monitoring, and troubleshooting  | Reduces repetitive engineering effort and potential incident impact         |
| 6 | Greater Productivity                         | Reliable connectivity and structured operational procedures   | Supports employees, business applications, and manufacturing services       |
| 7 | Security Governance and Compliance Readiness | Documented ACLs, Syslog, NTP, and validation evidence         | Supports security reviews and relevant NIST/IEC 62443 assessments           |
| 8 | Scalable Manufacturing Infrastructure        | Modular VLAN architecture and structured addressing           | Supports additional devices, services, and manufacturing segments           |
| 9 | Enhanced Manufacturing Reliability           | Segmentation, redundancy, centralized monitoring, and testing | Provides a foundation for dependable manufacturing operations               |

### Illustrative Enterprise Financial Impact

| Financial / Operational Metric   | Enterprise Estimate    | Business Interpretation                                                    |
| -------------------------------- | ---------------------- | -------------------------------------------------------------------------- |
| Annual Operational Cost Savings  | $2.1 million           | Modeled reduction in administrative and operational expenses               |
| Annual Avoided Downtime Costs    | $3.8 million           | Modeled reduction in manufacturing interruption costs                      |
| Combined Gross Annual Value      | $5.9 million           | Hypothetical annual benefit before implementation and operating expenses   |
| Annual Engineering Time Savings  | 2,800 IT/OT hours      | Illustrative engineering productivity improvement                          |
| Production Uptime Target         | 99.9%                  | Hypothetical enterprise availability objective                             |
| Incident Containment Improvement | 60% faster             | Illustrative incident response improvement                                 |
| Future Expansion Costs           | 50% lower              | Hypothetical benefit of modular network architecture                       |
| Illustrative First-Year ROI      | 250%                   | Infographic scenario assumption requiring independent financial validation |
| Illustrative Payback Period      | Approximately 5 months | Scenario assumption dependent on investment and cash-flow timing           |

### Financial Disclosure

| Consideration               | Financial Interpretation                                                                                                                                      |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Financial Classification    | All monetary values and performance improvements are illustrative enterprise-scale estimates, not measured Cisco Modeling Labs results.                       |
| Combined Annual Value       | The $5.9 million is composed of $2.1 million in modeled operational savings and $3.8 million in avoided downtime costs.                                       |
| ROI Calculation             | With $5.9 million in gross benefits and a $2.4 million investment, standard first-year ROI is approximately 145.8%, before additional operating expenses.     |
| 250% ROI Assumption         | The separately illustrated 250% ROI requires different documented financial assumptions.                                                                      |
| Benefit Overlap             | Technology-specific financial estimates may overlap and should not automatically be added to the $5.9 million scenario.                                       |
| Production Performance      | Uptime, incident containment, productivity, and expansion improvements are targets or estimates rather than observed production outcomes.                     |
| Formal Financial Validation | A production business case requires investment, operating costs, incident frequency, labor rates, downtime exposure, cash-flow timing, and realized benefits. |

## 6.4 Technical Value

Project 6 demonstrates practical engineering competencies in network architecture, Cisco routing and switching, IT/OT segmentation, cybersecurity, network resilience, infrastructure services, and systematic troubleshooting.

### Engineering Competencies Demonstrated

| #  | Engineering Competency              | Technical Value                                                                                                               |
| -- | ----------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| 1  | Enterprise Network Architecture     | Design a manufacturing topology integrating a perimeter router, interconnected switches, endpoints, and centralized services. |
| 2  | IT/OT Network Segmentation          | Separate Corporate, Engineering, OT, Guest, Services, and Management traffic.                                                 |
| 3  | VLAN Configuration                  | Configure six logical network segments with appropriate access port assignments.                                              |
| 4  | IEEE 802.1Q Trunking                | Transport tagged VLAN traffic across router-to-switch and inter-switch connections.                                           |
| 5  | Router-on-a-Stick Routing           | Configure router subinterfaces and default gateways for controlled inter-VLAN connectivity.                                   |
| 6  | IPv4 Addressing and Subnetting      | Implement structured IPv4 addressing across manufacturing network segments.                                                   |
| 7  | ACL Design and Enforcement          | Restrict unauthorized network communication through traffic filtering policies.                                               |
| 8  | Guest Network Isolation             | Prevent guest access to protected Corporate, Engineering, OT, Services, and Management resources.                             |
| 9  | NAT Configuration                   | Enable and verify approved external network connectivity.                                                                     |
| 10 | DHCP Configuration                  | Automate IPv4 addressing for Corporate and Guest endpoints.                                                                   |
| 11 | Rapid PVST+ Implementation          | Prevent Layer 2 loops and establish spanning-tree root bridge selection.                                                      |
| 12 | Network Redundancy                  | Validate redundant switching paths, link failure recovery, and reconvergence.                                                 |
| 13 | Syslog Monitoring                   | Centralize network event collection and support security investigations.                                                      |
| 14 | NTP Synchronization                 | Maintain consistent timestamps for event correlation.                                                                         |
| 15 | Secure Administration               | Apply controlled administrative access, appropriate SSH practices, and acceptable-use login banners.                          |
| 16 | Cisco IOS CLI                       | Configure, troubleshoot, and validate network infrastructure.                                                                 |
| 17 | Layer 2 and Layer 3 Troubleshooting | Diagnose VLAN, trunking, routing, ACL, NAT, DHCP, and spanning-tree issues.                                                   |
| 18 | Network Connectivity Testing        | Verify endpoint addressing, gateway reachability, authorized inter-VLAN communication, and external access.                   |
| 19 | Security Policy Validation          | Confirm permitted and denied traffic through connectivity tests, ACL counters, and logs.                                      |
| 20 | Technical Documentation             | Produce network diagrams, configuration records, CLI outputs, screenshots, and validation reports.                            |

### Engineering Domains

| Engineering Domain      | Technologies and Skills                                         |
| ----------------------- | --------------------------------------------------------------- |
| Network Design          | Cisco IOS, enterprise topology, IPv4 subnetting                 |
| Network Segmentation    | VLANs, access ports, IEEE 802.1Q trunks                         |
| Layer 3 Connectivity    | Router-on-a-stick, gateway configuration, inter-VLAN routing    |
| Cybersecurity           | ACLs, guest isolation, secure administration                    |
| External Connectivity   | NAT and connectivity validation                                 |
| Infrastructure Services | DHCP, NTP, Syslog                                               |
| Network Resilience      | Rapid PVST+, root bridge selection, failover testing            |
| Troubleshooting         | Cisco IOS CLI, Layer 2/Layer 3 diagnostics, root-cause analysis |
| Engineering Validation  | Connectivity testing, ACL counters, service verification        |
| Documentation           | Network diagrams, CLI evidence, screenshots, validation records |

Core Technologies: Cisco IOS • Cisco Modeling Labs • VLANs • IEEE 802.1Q • ACLs • NAT • DHCP • Rapid PVST+ • NTP • Syslog • CLI

## 6.5 Solution Architecture

### Architecture Overview

Project 6 implements a segmented manufacturing network consisting of an edge/perimeter router, two interconnected Layer 2 switches, corporate and guest endpoints, and a centralized services server.

The architecture provides controlled inter-VLAN communication, ACL enforcement, redundant switching paths, and centralized infrastructure services.

### Network Components

| Component | Role                     | Primary Function                                                                                   |
| --------- | ------------------------ | -------------------------------------------------------------------------------------------------- |
| R1        | Edge/Perimeter Router    | Inter-VLAN routing, ACL enforcement, NAT, DHCP, NTP, and Syslog forwarding                         |
| SW1       | Primary Layer 2 Switch   | VLAN switching, IEEE 802.1Q trunking, Rapid PVST+ root bridge, Corporate and Services connectivity |
| SW2       | Secondary Layer 2 Switch | Redundant switching, Rapid PVST+ participation, Guest endpoint connectivity                        |
| PC1       | Corporate Workstation    | Validates DHCP, gateway reachability, authorized inter-VLAN communication, and external access     |
| SRV1      | Services Server          | Provides centralized infrastructure services, including Syslog and NTP                             |
| PC2       | Guest Test Endpoint      | Validates guest isolation, ACL restrictions, and permitted external connectivity                   |

### VLAN and IP Addressing Plan

| VLAN | Network Segment | IPv4 Subnet     | Default Gateway | Primary Purpose                          |
| ---- | --------------- | --------------- | --------------- | ---------------------------------------- |
| 10   | Corporate       | `10.10.10.0/24` | `10.10.10.1`    | Corporate IT and administration          |
| 20   | Engineering     | `10.10.20.0/24` | `10.10.20.1`    | Engineering applications and systems     |
| 30   | OT              | `10.10.30.0/24` | `10.10.30.1`    | Manufacturing and operational technology |
| 40   | Guest           | `10.10.40.0/24` | `10.10.40.1`    | Restricted guest connectivity            |
| 50   | Services        | `10.10.50.0/24` | `10.10.50.1`    | Centralized infrastructure services      |
| 99   | Management      | `10.10.99.0/24` | `10.10.99.1`    | Network device administration            |

R1 provides the corresponding default gateways through IEEE 802.1Q router subinterfaces. SRV1 uses static address `10.10.50.10/24`.

### Architecture and Security Controls

| Architecture Component  | Implementation                      | Security / Operational Value                                  |
| ----------------------- | ----------------------------------- | ------------------------------------------------------------- |
| Perimeter Routing       | R1 router-on-a-stick                | Controlled communication between VLANs                        |
| VLAN Segmentation       | Six logical VLANs                   | Separation of IT, OT, Guest, Services, and Management traffic |
| Switch Interconnects    | Redundant IEEE 802.1Q trunks        | VLAN transport and alternate network paths                    |
| Spanning Tree           | Rapid PVST+ with SW1 as root        | Loop prevention and Layer 2 reconvergence                     |
| Network Access          | ACL enforcement on R1               | Guest isolation and restricted access to protected resources  |
| External Connectivity   | NAT on R1                           | Permitted access to external networks                         |
| Endpoint Addressing     | DHCP for Corporate and Guest        | Automated endpoint configuration                              |
| Centralized Monitoring  | Syslog through SRV1                 | Network event collection and investigation                    |
| Time Synchronization    | NTP through SRV1                    | Consistent timestamps for event correlation                   |
| Administrative Security | Controlled access and login banners | Improved administration and acceptable-use notification       |

### Network Resilience

SW1 and SW2 use redundant IEEE 802.1Q trunk links. Rapid PVST+ prevents switching loops by placing redundant paths into appropriate spanning-tree states.

During controlled link failure testing, the network demonstrated reconvergence and preservation of connectivity through an alternate forwarding path.

## 6.6 Simplified Troubleshooting Workflow

Project 6 applies a structured troubleshooting methodology to investigate network connectivity, security, redundancy, and infrastructure service problems.

### Five-Step Troubleshooting Workflow

| Step                    | Verification                                                        | Expected Outcome                     |
| ----------------------- | ------------------------------------------------------------------- | ------------------------------------ |
| 1. Verify Connectivity  | Interfaces, ping tests, endpoints, and default gateways             | Network reachability established     |
| 2. Check VLANs & Trunks | VLAN membership, access ports, and IEEE 802.1Q trunks               | Network segmentation verified        |
| 3. Validate Security    | ACL permit/deny rules, guest isolation, counters, and logs          | Access policies enforced             |
| 4. Test Redundancy      | Rapid PVST+ root bridge, alternate paths, and link failure recovery | Selected failover behavior validated |
| 5. Confirm Services     | DHCP, NAT, NTP, Syslog, and DNS where configured                    | Infrastructure services verified     |

### Six-Stage Troubleshooting Methodology

| Phase | Stage    | Engineering Activities                                                                            | Expected Outcome                  |
| ----- | -------- | ------------------------------------------------------------------------------------------------- | --------------------------------- |
| 1     | Identify | Determine affected devices, VLANs, network services, and observed symptoms.                       | Clearly defined problem           |
| 2     | Analyze  | Examine device status, configurations, logs, connectivity tests, and protocol behavior.           | Evidence-based understanding      |
| 3     | Isolate  | Narrow the issue to switching, trunking, routing, ACLs, NAT, DHCP, NTP, Syslog, or spanning tree. | Identified root cause             |
| 4     | Resolve  | Correct configurations, restore connectivity, or adjust network services and security policies.   | Remediated issue                  |
| 5     | Validate | Repeat connectivity, security, redundancy, and service verification tests.                        | Confirmed functionality           |
| 6     | Document | Capture commands, screenshots, findings, corrective actions, and final results.                   | Reproducible engineering evidence |

### Troubleshooting and Verification Matrix

| Network Area         | Potential Issue                                              | Verification Method                                 |
| -------------------- | ------------------------------------------------------------ | --------------------------------------------------- |
| Device Connectivity  | Device or interface unavailable                              | Interface status and ping testing                   |
| VLAN Segmentation    | Missing VLAN or incorrect access port                        | VLAN membership verification                        |
| IEEE 802.1Q Trunking | Incorrect trunk configuration or allowed VLANs               | Trunk interface verification                        |
| Inter-VLAN Routing   | Incorrect gateway or router subinterface                     | Routing and interface verification                  |
| ACL Enforcement      | Unauthorized access or incorrect traffic restrictions        | ACL inspection, counters, and connectivity testing  |
| NAT                  | Failed external connectivity                                 | NAT translation verification                        |
| DHCP                 | Missing or incorrect endpoint IP configuration               | Endpoint addressing and DHCP verification           |
| Rapid PVST+          | Incorrect root bridge, blocked path, or failed reconvergence | Spanning-tree verification and link failure testing |
| Syslog               | Missing network events                                       | Logging configuration and event inspection          |
| NTP                  | Unsynchronized timestamps                                    | NTP status and association verification             |

### Troubleshooting Principles

| Principle                     | Engineering Practice                                                                              |
| ----------------------------- | ------------------------------------------------------------------------------------------------- |
| Evidence-Based Investigation  | Collect diagnostic evidence before modifying network configurations.                              |
| Root-Cause Analysis           | Isolate the affected network layer, service, or security policy.                                  |
| Minimal Configuration Changes | Avoid unnecessary changes to unaffected devices or services.                                      |
| Security Policy Preservation  | Ensure troubleshooting does not introduce unauthorized network access.                            |
| Controlled Remediation        | Apply targeted configuration corrections and document corrective actions.                         |
| Post-Remediation Verification | Confirm functionality without introducing connectivity regressions or infrastructure instability. |
| Engineering Documentation     | Preserve findings, screenshots, CLI outputs, and final validation evidence.                       |

## 6.7 Tools Used

Project 6 uses Cisco networking technologies, simulation tools, diagnostic utilities, and technical documentation methods to implement and validate the manufacturing network.

### Engineering Tools and Technologies

| Tool / Technology         | Category                      | Primary Purpose                                                                 |
| ------------------------- | ----------------------------- | ------------------------------------------------------------------------------- |
| Cisco Modeling Labs (CML) | Network Simulation            | Build, configure, and test the manufacturing topology                           |
| Cisco IOS                 | Network Operating System      | Configure routers, switches, routing, security, and infrastructure services     |
| Cisco IOS CLI             | Configuration and Diagnostics | Execute configuration, monitoring, and verification commands                    |
| Terminal / SSH Utilities  | Device Administration         | Provide command-line access and support secure remote management                |
| Wireshark                 | Packet Analysis               | Analyze network traffic and support protocol troubleshooting                    |
| VLANs                     | Network Segmentation          | Separate Corporate, Engineering, OT, Guest, Services, and Management traffic    |
| IEEE 802.1Q               | VLAN Trunking                 | Carry multiple VLANs across network links                                       |
| ACLs                      | Network Security              | Enforce permitted and denied traffic policies                                   |
| NAT                       | External Connectivity         | Translate network addresses for approved external access                        |
| DHCP                      | Network Services              | Automatically assign endpoint IP configurations                                 |
| Rapid PVST+               | Network Resilience            | Prevent switching loops and support redundant paths                             |
| NTP                       | Time Synchronization          | Synchronize timestamps across infrastructure devices                            |
| Syslog                    | Monitoring and Logging        | Centralize network events and security-related logs                             |
| Network Diagrams          | Architecture Documentation    | Illustrate network topology, segmentation, and device relationships             |
| Markdown                  | Technical Documentation       | Maintain project descriptions, implementation records, and engineering evidence |

### Technology Integration

| Technology            | Integration                                                                              | Engineering Value                                |
| --------------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------ |
| Cisco IOS and CLI     | Configure and verify routing, switching, security controls, and infrastructure services. | Hands-on network engineering and troubleshooting |
| Cisco Modeling Labs   | Simulate the manufacturing network topology and support controlled validation.           | Repeatable network testing                       |
| VLANs and IEEE 802.1Q | Separate traffic and transport multiple VLANs across trunk links.                        | Logical segmentation and connectivity            |
| ACLs                  | Restrict guest access and regulate authorized network communication.                     | Security policy enforcement                      |
| NAT and DHCP          | Support external connectivity and automatic client addressing.                           | Simplified network operations                    |
| Rapid PVST+           | Maintain redundant Layer 2 paths while preventing switching loops.                       | Network resilience                               |
| NTP and Syslog        | Synchronize timestamps and centralize network events.                                    | Operational visibility and event correlation     |
| Wireshark             | Support packet-level troubleshooting where required.                                     | Protocol analysis                                |
| Python                | Provide a potential foundation for automated validation and reporting.                   | Future network automation                        |
| Git / GitLab          | Manage project configurations, diagrams, and technical documentation.                    | Version control and traceability                 |
| Markdown              | Organize technical documentation and engineering evidence.                               | Professional GitHub presentation                 |

Core Technology Stack: Cisco IOS • Cisco Modeling Labs • CLI • SSH • VLANs • IEEE 802.1Q • ACLs • NAT • DHCP • Rapid PVST+ • NTP • Syslog • Wireshark • Markdown

## 6.8 Simplified Implementation

Project 6 follows a structured implementation lifecycle to design, configure, deploy, test, troubleshoot, and document the manufacturing network.

### Simplified Implementation Workflow

| Step                                 | Activity                                                         | Engineering Outcome                        |
| ------------------------------------ | ---------------------------------------------------------------- | ------------------------------------------ |
| 1. Build Topology Lab                | Deploy R1, SW1, SW2, PC1, SRV1, and PC2 in CML.                  | Working simulated topology                 |
| 2. Configure Switches                | Create VLANs, access ports, IEEE 802.1Q trunks, and Rapid PVST+. | Segmented and redundant Layer 2 network    |
| 3. Configure Router                  | Configure subinterfaces, DHCP, NAT, and routing.                 | Controlled Layer 3 connectivity            |
| 4. Implement Network Security        | Apply ACLs, guest restrictions, and login banners.               | Protected internal segments                |
| 5. Configure Infrastructure Services | Configure SRV1, NTP, Syslog, and validate addressing.            | Centralized services and monitoring        |
| 6. Test and Validate                 | Verify connectivity, access rules, NAT, services, and failover.  | Seven functionality requirements validated |
| 7. Document and Verify               | Preserve CLI outputs, screenshots, diagrams, and test results.   | Reproducible engineering evidence          |

### Six-Phase Implementation Lifecycle

| Phase | Stage        | Implementation Activities                                                                                                 | Deliverable                             |
| ----- | ------------ | ------------------------------------------------------------------------------------------------------------------------- | --------------------------------------- |
| 1     | Plan         | Define business requirements, network architecture, VLANs, IP addressing, security policies, and redundancy requirements. | Network design and addressing plan      |
| 2     | Configure    | Configure Cisco IOS devices, VLANs, trunks, routing, ACLs, NAT, DHCP, Rapid PVST+, NTP, and Syslog.                       | Device configurations                   |
| 3     | Deploy       | Establish network connections, assign endpoints, activate services, and implement security controls.                      | Operational CML topology                |
| 4     | Test         | Verify device connectivity, VLAN isolation, routing, external access, infrastructure services, and redundancy.            | Functional validation results           |
| 5     | Troubleshoot | Investigate configuration issues, correct failures, and repeat verification.                                              | Resolved issues and confirmed operation |
| 6     | Document     | Capture network diagrams, CLI outputs, screenshots, configurations, and validation evidence.                              | Final engineering documentation         |

### Implementation and Validation Activities

| Engineering Activity    | Implementation / Verification                                                         |
| ----------------------- | ------------------------------------------------------------------------------------- |
| Network Topology        | Deploy R1, SW1, SW2, PC1, and SRV1, with PC2 as an additional guest test endpoint     |
| VLAN Configuration      | Create six logical network segments                                                   |
| Trunk Configuration     | Configure IEEE 802.1Q trunk links between network devices                             |
| Inter-VLAN Routing      | Configure R1 router subinterfaces and default gateways                                |
| Security Policies       | Apply ACLs to restrict unauthorized access between network segments                   |
| Guest Isolation         | Verify Guest cannot access protected internal networks                                |
| External Connectivity   | Configure NAT and test permitted external access                                      |
| DHCP Services           | Configure automated IP addressing for Corporate and Guest endpoints                   |
| Layer 2 Redundancy      | Configure Rapid PVST+ and verify SW1 root bridge selection                            |
| Failover Testing        | Simulate switching-link failure and verify reconvergence                              |
| Network Monitoring      | Configure Syslog forwarding and inspect logged events                                 |
| Time Synchronization    | Configure NTP and verify synchronization and associations                             |
| Administrative Controls | Configure acceptable-use login banners and controlled device access                   |
| Functional Validation   | Verify all seven network functionality requirements                                   |
| Documentation           | Capture screenshots, CLI verification results, network diagrams, and testing evidence |

### Security and Privacy Requirements

This repository is intended for public engineering portfolio presentation. All published project artifacts follow security-conscious documentation practices to protect credentials, confidential information, and sensitive industrial network details.

| #  | Security Requirement           | Engineering / Publication Practice                                                                                  | Security & Operational Value                                            |
| -- | ------------------------------ | ------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| 1  | Credential Protection          | Exclude passwords, SSH private keys, authentication secrets, and confidential credentials from public repositories. | Prevents unauthorized access and credential exposure.                   |
| 2  | Confidentiality                | Exclude sensitive manufacturing, employee, customer, and organizational information.                                | Protects confidential business and operational data.                    |
| 3  | Network Information Protection | Avoid exposing production OT configurations, management addresses, or industrial device details.                    | Reduces unnecessary disclosure of sensitive infrastructure information. |
| 4  | Sanitized Evidence             | Publish simulated or appropriately sanitized diagrams, screenshots, logs, and configurations.                       | Supports secure public portfolio presentation.                          |
| 5  | Least Privilege                | Apply controlled administrative access and appropriate permissions.                                                 | Restricts unauthorized administrative activity.                         |
| 6  | Network Segmentation           | Maintain separation between Corporate, Engineering, OT, Guest, Services, and Management networks.                   | Establishes logical security boundaries.                                |
| 7  | Access Enforcement             | Apply ACLs and verify restrictions on unauthorized communication.                                                   | Protects internal resources and supports controlled connectivity.       |
| 8  | Monitoring                     | Maintain centralized Syslog collection and synchronized NTP timestamps.                                             | Supports security investigations and operational visibility.            |
| 9  | Resilience                     | Validate redundant switching paths and recovery behavior through controlled testing.                                | Supports network availability and business continuity.                  |
| 10 | Evidence Review                | Inspect CLI outputs, screenshots, logs, and reports before publication.                                             | Prevents unintended disclosure of sensitive information.                |
| 11 | Accurate Reporting             | Distinguish validated laboratory results from production performance claims.                                        | Maintains technical accuracy and professional credibility.              |
| 12 | Financial Transparency         | Clearly identify enterprise financial estimates as illustrative rather than measured project results.               | Supports responsible financial communication.                           |

### Production IT/OT Deployment Considerations

The Cisco Modeling Labs implementation is a validated manufacturing network proof of concept rather than a complete production industrial control system architecture.

A production deployment requires additional security engineering, industrial risk assessment, operational safety review, and environment-specific validation.

| # | Production Consideration         | Engineering Purpose                                                                             | Security & Operational Value                                                  |
| - | -------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| 1 | Industrial Firewalls             | Enforce dedicated security boundaries between manufacturing security zones.                     | Provides granular traffic inspection and access enforcement.                  |
| 2 | IT/OT Demilitarized Zones (DMZs) | Control communication between enterprise IT and industrial environments.                        | Reduces direct exposure of operational technology networks.                   |
| 3 | Industrial Asset Inventories     | Identify, classify, and protect operational technology assets.                                  | Improves asset visibility and cybersecurity risk management.                  |
| 4 | Restricted Remote Access         | Control administrative and third-party connectivity.                                            | Reduces unauthorized remote access risks.                                     |
| 5 | Industrial Protocol Monitoring   | Improve visibility into industrial communications and abnormal activity.                        | Supports detection and investigation of industrial network threats.           |
| 6 | Backup and Recovery              | Support restoration of critical infrastructure and device configurations.                       | Improves operational recovery readiness.                                      |
| 7 | Safety Engineering               | Account for manufacturing processes, operational safety, and industrial equipment requirements. | Supports safe and reliable industrial operations.                             |
| 8 | IEC 62443                        | Apply relevant industrial automation and control system security guidance.                      | Supports industrial cybersecurity engineering and security assessments.       |
| 9 | NIST SP 800-82                   | Apply operational technology security planning and risk management guidance.                    | Supports OT cybersecurity risk assessment and security architecture planning. |

Deployment Classification: Successfully validated Cisco Modeling Labs manufacturing network proof of concept. Production deployment requires additional security controls, safety engineering, risk assessment, and operational validation.

## 6.9 Project Outcomes

### Executive Results Dashboard

Project 6 successfully demonstrates the implementation and validation of a secure, segmented, and resilient manufacturing IT/OT network using Cisco Modeling Labs.

| #  | Key Performance Indicator         | Validated Project Result                                                        |
| -- | --------------------------------- | ------------------------------------------------------------------------------- |
| 1  | Functional Requirements Validated | 7/7                                                                             |
| 2  | Logical VLAN Segments             | 6                                                                               |
| 3  | Core Network Devices              | 3 — R1, SW1, SW2                                                                |
| 4  | Validated Redundancy Design       | 1 — Rapid PVST+ with redundant SW1–SW2 trunks                                   |
| 5  | Network Topology                  | Five core nodes plus an additional guest test endpoint                          |
| 6  | Network Segmentation              | Corporate, Engineering, OT, Guest, Services, and Management                     |
| 7  | Network Security                  | ACL enforcement and guest isolation validated                                   |
| 8  | Inter-VLAN Routing                | Authorized communication verified                                               |
| 9  | External Connectivity             | NAT operation and permitted external access verified                            |
| 10 | Layer 2 Redundancy                | Rapid PVST+ failover and reconvergence validated                                |
| 11 | Infrastructure Services           | DHCP, NTP, and Syslog validated                                                 |
| 12 | Technical Documentation           | Architecture diagrams, CLI outputs, screenshots, and testing evidence completed |
| 13 | Final Project Status              | Completed Successfully — Cisco Modeling Labs Proof of Concept                   |

### Seven Functional Requirements Validated

| # | Functional Requirement            | Validated Engineering Outcome                                                             |
| - | --------------------------------- | ----------------------------------------------------------------------------------------- |
| 1 | Device Discovery and Reachability | Verified endpoint addressing, gateway reachability, and authorized network communication. |
| 2 | Guest Network Security            | Validated ACL enforcement and guest isolation from protected internal resources.          |
| 3 | Login Banners                     | Configured acceptable-use login banners on R1, SW1, and SW2.                              |
| 4 | Routing and External Connectivity | Verified inter-VLAN routing, permitted external connectivity, and NAT translations.       |
| 5 | Layer 2 Redundancy                | Validated Rapid PVST+ root bridge selection, failover, and reconvergence.                 |
| 6 | Syslog and NTP                    | Verified centralized logging, time synchronization, and NTP associations.                 |
| 7 | VLANs and IEEE 802.1Q             | Validated six VLANs, trunk links, access ports, and VLAN operation.                       |

### Engineering Accomplishments

| #  | Engineering Area        | Final Achievement                                                                                         | Technical & Operational Value                                     |
| -- | ----------------------- | --------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| 1  | Network Architecture    | Designed and implemented a segmented Cisco manufacturing network in CML.                                  | Demonstrates enterprise network design and implementation skills. |
| 2  | Network Segmentation    | Configured six VLANs and IEEE 802.1Q trunk connections.                                                   | Establishes logical network separation.                           |
| 3  | Layer 3 Routing         | Implemented router-on-a-stick inter-VLAN routing.                                                         | Supports controlled communication between authorized networks.    |
| 4  | Cybersecurity           | Enforced ACL policies and validated guest network isolation.                                              | Restricts unauthorized access to protected resources.             |
| 5  | External Connectivity   | Configured NAT and verified permitted external communication.                                             | Supports controlled access to external networks.                  |
| 6  | Endpoint Addressing     | Configured DHCP and validated corporate and guest client addressing.                                      | Reduces manual endpoint configuration.                            |
| 7  | Network Resilience      | Implemented Rapid PVST+ and validated redundant switching failover.                                       | Supports recovery from selected link failures.                    |
| 8  | Network Monitoring      | Configured and verified Syslog event collection.                                                          | Improves operational visibility and troubleshooting.              |
| 9  | Time Synchronization    | Configured NTP and verified synchronization.                                                              | Supports consistent event timestamps.                             |
| 10 | Administrative Security | Configured acceptable-use login banners and documented access controls.                                   | Supports administrative security governance.                      |
| 11 | Testing and Validation  | Completed all seven functionality requirements.                                                           | Provides evidence of intended network functionality.              |
| 12 | Technical Documentation | Produced network diagrams, CLI outputs, screenshots, configuration records, and troubleshooting evidence. | Supports engineering accountability and knowledge transfer.       |

### Final Business, Technical, and Portfolio Outcomes

| # | Outcome Category      | Project Value                                                                                                                                                                        |
| - | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1 | Business Outcome      | Demonstrates a manufacturing network architecture designed to improve reliability, reduce cybersecurity exposure, support business continuity, and minimize operational disruptions. |
| 2 | Technical Outcome     | Validated a Cisco network proof of concept featuring six VLANs, controlled inter-VLAN routing, ACL enforcement, NAT, DHCP, Rapid PVST+, NTP, and Syslog.                             |
| 3 | Operational Outcome   | Improved laboratory visibility through centralized logging, synchronized timestamps, and structured troubleshooting.                                                                 |
| 4 | Security Outcome      | Demonstrated IT/OT segmentation principles, restricted guest access, and verified ACL enforcement.                                                                                   |
| 5 | Engineering Outcome   | Demonstrated Cisco IOS configuration, network architecture, Layer 2/Layer 3 troubleshooting, infrastructure services, redundancy, and validation skills.                             |
| 6 | Resilience Outcome    | Validated redundant Layer 2 switching paths and spanning-tree reconvergence following a simulated link failure.                                                                      |
| 7 | Documentation Outcome | Completed architecture diagrams, configuration records, CLI evidence, screenshots, troubleshooting records, and functionality reporting.                                             |
| 8 | Portfolio Outcome     | Demonstrates end-to-end network engineering capabilities relevant to enterprise networking, cybersecurity, manufacturing infrastructure, and industrial IT/OT security roles.        |
| 9 | Financial Outcome     | Illustrates potential enterprise financial benefits through modeled operational savings and avoided downtime costs; no financial results were measured in the laboratory.            |

### Final Project Summary

| #  | Category                | Final Project Summary                                                                                                                                                                        |
| -- | ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1  | Project Overview        | Successfully designed, implemented, configured, troubleshot, and validated a secure, segmented, and resilient manufacturing IT/OT network in Cisco Modeling Labs.                            |
| 2  | Solution Architecture   | Implemented R1, SW1, SW2, PC1, and SRV1, with PC2 as an additional guest security test endpoint.                                                                                             |
| 3  | Network Segmentation    | Established six logical VLANs for Corporate, Engineering, OT, Guest, Services, and Management traffic.                                                                                       |
| 4  | Network Security        | Implemented ACL restrictions, guest isolation, controlled inter-VLAN routing, and acceptable-use login banners.                                                                              |
| 5  | Network Connectivity    | Validated IEEE 802.1Q trunking, router-on-a-stick routing, DHCP, NAT, and authorized external communication.                                                                                 |
| 6  | Network Resilience      | Configured Rapid PVST+ with SW1 as root bridge and validated alternate-path recovery during simulated link failure.                                                                          |
| 7  | Infrastructure Services | Configured and validated centralized Syslog, NTP synchronization, and DHCP services.                                                                                                         |
| 8  | Engineering Validation  | Successfully completed all seven functionality requirements using Cisco IOS diagnostics, connectivity tests, ACL counters, and service verification.                                         |
| 9  | Technical Documentation | Produced architecture diagrams, configuration evidence, CLI outputs, screenshots, troubleshooting records, and the final functionality report.                                               |
| 10 | Business Value          | Demonstrates how secure segmentation, controlled access, redundancy, and centralized monitoring can support manufacturing reliability and business continuity.                               |
| 11 | Financial Value         | Illustrative enterprise scenario: $2.1M annual operational savings, $3.8M avoided downtime costs, and $5.9M combined gross annual value.                                                     |
| 12 | Production Scope        | Validated simulated network proof of concept; not a production industrial control system or evidence of production uptime or financial performance.                                          |
| 13 | Final Laboratory Result | Project Completed Successfully — All Seven Functional Requirements Validated.                                                                                                                |
| 14 | Portfolio Value         | Demonstrates practical Cisco network engineering, industrial IT/OT segmentation, cybersecurity, routing, switching, monitoring, redundancy, troubleshooting, and professional documentation. |

### Final Project Conclusion

| # | Category                 | Final Project Summary                                                                                                                                                                  | Business & Technical Value                                                                                                                 |
| - | ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 1 | Project Overview         | Successfully demonstrated the end-to-end engineering lifecycle of a secure, segmented, and resilient manufacturing IT/OT network.                                                      | Demonstrates practical network architecture, implementation, security engineering, troubleshooting, and validation capabilities.           |
| 2 | Technical Solution       | Integrated six VLANs, IEEE 802.1Q trunking, controlled inter-VLAN routing, ACL enforcement, NAT, DHCP, Rapid PVST+ redundancy, NTP synchronization, and centralized Syslog monitoring. | Establishes secure network segmentation, controlled connectivity, infrastructure services, operational visibility, and Layer 2 resilience. |
| 3 | Engineering Competencies | Demonstrated practical skills in enterprise networking, cybersecurity, manufacturing infrastructure, industrial IT/OT security, and operational resilience.                            | Provides professional engineering evidence relevant to network engineering, cybersecurity, and industrial network security roles.          |
| 4 | Laboratory Foundation    | Established a documented Cisco Modeling Labs environment for secure industrial network design, configuration, testing, and validation.                                                 | Provides a repeatable engineering foundation for network security assessments, infrastructure improvements, and future development.        |
| 5 | Final Laboratory Result  | Project Completed Successfully — All Seven Functional Requirements Validated in Cisco Modeling Labs.                                                                                   | Secure Manufacturing. Segmented Networks. Resilient Infrastructure. Validated Engineering. Stronger Business Operations.                   |
