# Project 4 – Network Automation & Deployment: VLANs, Configurations, SSH Security, Ansible, Netmiko, & Python

Network Engineering • Python Automation • VLAN Deployment • SSH Security • Configuration Management • Infrastructure Validation

Automate • Configure • Secure • Deploy • Validate • Optimize

![Project 4 – Network Automation & Deployment](4.%20Network%20Automation%20%26%20Deployment%20-%20VLANs%2C%20Configs%2C%20SSH%2C%20%26%20More.png)

Project Overview: Design and implement a secure, repeatable network automation solution using Python, Netmiko, and Ansible to automate VLAN deployment, manage switch configurations, establish SSH key-based authentication, perform configuration backups, and validate network operations across multiple ExtremeXOS switches.

The Project 4 infographic provides a consolidated visual overview. Each section below provides additional business, technical, architectural, implementation, troubleshooting, and validation context.

## Project Documentation

| Section | Documentation | Detailed Guide | Infographic |
|---|---|---|---|
| 4.2 | Executive Overview | [Read Documentation](4.2%20Executive-Overview.md) | [View Infographic](infographics/4.2%20Executive-Overview%20A.png) |
| 4.3 | Business Value | [Read Documentation](4.3%20Business-Value.md) | [View Infographic](infographics/4.3%20Business-Value%20A.png) |
| 4.4 | Technical Value | [Read Documentation](4.4%20Technical-Value.md) | [View Infographic](infographics/4.4%20Technical-Value%20A.png) |
| 4.5 | Solution Architecture | [Read Documentation](4.5%20Solution-Architecture.md) | [View Infographic](infographics/4.5%20Solution-Architecture.png) |
| 4.6 | Simplified Troubleshooting Workflow | [Read Documentation](4.6%20Simplified-Troubleshooting-Workflow.md) | [View Infographic](infographics/4.6%20Simplified-Troubleshooting-Workflow.png) |
| 4.7 | Tools Used | [Read Documentation](4.7%20Tools-Used.md) | [View Infographic](infographics/4.7%20Tools-Used.png) |
| 4.8 | Simplified Implementation | [Read Documentation](4.8%20Simplified-Implementation.md) | [View Infographic](infographics/4.8%20Simplified-Implementation.png) |
| 4.9 | Project Outcomes | [Read Documentation](4.9%20Project-Outcomes.md) | [View Infographic](infographics/4.9%20Project-Outcomes%20A.png) |

## 4.2 Executive Overview

Project 4 addresses the challenges of manual switch administration, inconsistent VLAN configurations, insecure management access, limited configuration backups, and time-consuming deployment validation. It establishes a centralized, repeatable automation framework for managing enterprise switching infrastructure.

| Executive Priority            | Engineering Solution                                                                                               | Business Value                                              |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------- |
| Network Automation            | Use Python and Netmiko to automate switch discovery, configuration, VLAN deployment, and validation.               | Reduced manual administration and faster deployments.       |
| Configuration Standardization | Use Ansible inventories and YAML playbooks for consistent device management.                                       | Fewer configuration errors and improved reliability.        |
| Secure Administration         | Implement RSA SSH key-based authentication and controlled administrative access.                                   | Stronger security and reduced unauthorized access risk.     |
| VLAN Segmentation             | Configure and verify departmental VLANs for IT, Management, Accounting, and Users.                                 | Consistent network segmentation and connectivity.           |
| Configuration Preservation    | Automate switch configuration backups before and after relevant changes.                                           | Improved recovery readiness and business continuity.        |
| Operational Validation        | Verify switch reachability, SSH authentication, VLAN membership, interface assignments, and configuration changes. | Greater deployment confidence and reduced operational risk. |
| Change Management             | Maintain automation scripts, playbooks, inventories, logs, and documentation through GitLab.                       | Improved traceability, accountability, and maintainability. |
| Scalability                   | Reuse automation components across additional switches and VLANs.                                                  | A foundation for future infrastructure expansion.           |

Primary objective: Automate, standardize, secure, deploy, validate, and document network infrastructure changes through a centralized Linux automation controller.

## 4.3 Business Value

Project 4 demonstrates how enterprise network automation can reduce repetitive administrative work, accelerate infrastructure deployments, improve configuration consistency, strengthen security, and support reliable network operations.

| Business Value Area                       | Engineering Implementation                                                                                     | Enterprise Benefit                                                               |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| Faster Network Deployments                | Automate switch configuration, VLAN creation, deployment, and verification using Python, Netmiko, and Ansible. | Shorter deployment timelines and reduced manual configuration effort.            |
| Configuration Consistency and Reliability | Apply standardized scripts, inventories, playbooks, and validation procedures.                                 | Fewer human errors, configuration mismatches, and network disruptions.           |
| Stronger Network Security                 | Implement RSA SSH key-based authentication, controlled administration, and approved configuration procedures.  | Reduced unauthorized access risk and improved security governance.               |
| Reduced Operational Costs                 | Automate repetitive configuration, backups, deployment, and verification tasks.                                | Lower administrative workloads and more efficient use of engineering resources.  |
| Improved Engineering Productivity         | Centralize device administration and use reusable automation workflows.                                        | More engineering time available for security, architecture, and optimization.    |
| Business Continuity and Recovery          | Preserve switch configurations and maintain documented recovery procedures.                                    | Faster recovery from configuration failures and improved operational resilience. |
| Scalability and Flexibility               | Extend reusable Python scripts, YAML inventories, and Ansible playbooks to additional infrastructure.          | Supports network growth without proportional increases in manual effort.         |
| User Experience and Service Availability  | Standardize VLAN deployments and validate network connectivity.                                                | More reliable access to business applications and network services.              |
| Change Management and Visibility          | Maintain GitLab history, configuration backups, execution logs, and validation records.                        | Better troubleshooting, auditing, accountability, and continuous improvement.    |

### Illustrative Enterprise Financial Impact

| Financial / Operational Metric        | Enterprise Estimate    |
| ------------------------------------- | ---------------------- |
| Annual Operational Cost Savings       | $2.1 million           |
| Annual Avoided Downtime Costs         | $3.8 million           |
| Combined Gross Annual Financial Value | $5.9 million           |
| Network Deployment Improvement        | 60% faster             |
| Annual Engineering Time Savings       | 2,800 IT hours         |
| Estimated First-Year ROI              | 250%                   |
| Estimated Payback Period              | Approximately 5 months |

Financial disclosure: All financial figures and performance percentages are illustrative enterprise-scale estimates, not measured laboratory or production results. The $5.9 million annual value represents modeled gross benefits before implementation and operating expenses, assuming no overlapping savings. ROI and payback require validation against a consistent financial model.

## 4.4 Technical Value

Project 4 demonstrates practical engineering capabilities in Python scripting, Netmiko SSH automation, Ansible configuration management, VLAN discovery and deployment, secure device administration, automated backups, infrastructure troubleshooting, and GitLab version control.

| Technical Capability                  | Technologies / Methods                                          | Demonstrated Engineering Value                                                                     |
| ------------------------------------- | --------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| Python Network Automation             | Python scripts and reusable functions                           | Automates device discovery, VLAN deployment, configuration backups, and validation.                |
| Netmiko Device Management             | Netmiko, SSH, ExtremeXOS CLI                                    | Establishes authenticated connections, executes commands, and retrieves configuration information. |
| Ansible Configuration Management      | Ansible, YAML inventories, playbooks                            | Standardizes multi-device administration and approved configuration changes.                       |
| VLAN Deployment and Segmentation      | VLAN discovery, creation, membership, interface verification    | Automates departmental VLAN configurations and validates network segmentation.                     |
| Secure SSH Authentication             | SSH2, RSA key pairs, administrative accounts                    | Enables authenticated remote administration and controlled device access.                          |
| Automated Configuration Backups       | Python, Netmiko, configuration archives                         | Preserves switch configurations for recovery, comparison, and change tracking.                     |
| Multi-Device Automation               | Centralized Linux controller, device inventories                | Manages four ExtremeXOS switches through repeatable workflows.                                     |
| Network Discovery and Validation      | CLI diagnostics, connectivity testing, configuration inspection | Confirms device reachability, VLAN configurations, and expected operational behavior.              |
| Version Control and Change Management | Git, GitLab                                                     | Tracks scripts, inventories, playbooks, configuration records, and engineering documentation.      |
| Modular Architecture and Scalability  | Reusable Python modules, YAML inventories, Ansible playbooks    | Supports additional switches, VLANs, and future automation requirements.                           |
| Troubleshooting and Error Analysis    | SSH diagnostics, Python logs, YAML validation, Ansible output   | Identifies and resolves authentication, connectivity, configuration, and automation failures.      |
| Technical Documentation and Reporting | Markdown, JSON, diagrams, logs, screenshots                     | Produces structured engineering evidence, deployment records, and reusable runbooks.               |

Core Technology Stack: Python • Netmiko • Ansible • Linux • ExtremeXOS • SSH • RSA Keys • YAML • JSON • Git • GitLab • CLI • Configuration Backups • Markdown

## 4.5 Solution Architecture

Project 4 uses a centralized Linux automation controller running Python, Netmiko, and Ansible to manage four ExtremeXOS access switches through the N-CoreA-01 core switch. The architecture integrates SSH key-based authentication, structured inventories, reusable scripts, Ansible playbooks, automated configuration backups, operational validation, and GitLab version control.

### Network Components and Topology

| Component                | Device / Technology             | Management IP         | Primary Function                                                                       |
| ------------------------ | ------------------------------- | --------------------- | -------------------------------------------------------------------------------------- |
| Automation Controller    | Linux, Python, Netmiko, Ansible | `10.10.1.10`          | Centralized execution of network automation, configuration management, and validation. |
| Core Switch              | N-CoreA-01                      | `10.10.1.1`           | Provides management connectivity to departmental switches.                             |
| IT Switch                | IT_Network                      | `10.10.1.21`          | VLAN 10 — IT systems and administration.                                               |
| Management Switch        | MGMT_Network                    | `10.10.1.22`          | VLAN 20 — Network Management.                                                          |
| Accounting Switch        | ACCT_Network                    | `10.10.1.23`          | VLAN 30 — Accounting systems.                                                          |
| User Switch              | User_Network                    | `10.10.1.24`          | VLAN 40 — General Users.                                                               |
| Secure Connectivity      | SSH / RSA Keys                  | Management Network    | Authenticated device management and command execution.                                 |
| Configuration Management | Ansible / YAML                  | Automation Controller | Standardized multi-device administrative workflows.                                    |
| Configuration Backups    | Python / Netmiko                | Automation Controller | Configuration preservation and recovery support.                                       |
| Version Control          | Git / GitLab                    | Repository            | Automation history, documentation, and change traceability.                            |

### Architecture Workflow

| Phase | Architecture Layer            | Primary Function                                                          |
| ----- | ----------------------------- | ------------------------------------------------------------------------- |
| 1     | Automation Controller         | Execute Python, Netmiko, and Ansible workflows.                           |
| 2     | Device Inventory              | Identify managed switches and connection parameters.                      |
| 3     | Secure Authentication         | Establish RSA SSH key-based device access.                                |
| 4     | Core Network Connectivity     | Reach managed switches through N-CoreA-01.                                |
| 5     | Managed Infrastructure        | Perform authorized operations on four ExtremeXOS switches.                |
| 6     | VLAN Discovery and Deployment | Retrieve existing VLANs and apply approved configurations.                |
| 7     | Configuration Management      | Execute standardized Ansible administrative tasks.                        |
| 8     | Configuration Backups         | Preserve switch configurations for recovery.                              |
| 9     | Post-Deployment Validation    | Verify VLANs, interfaces, SSH connectivity, and expected device behavior. |
| 10    | Version Control and Reporting | Maintain GitLab history, logs, validation results, and documentation.     |

### Architecture Design Principles

| Principle                       | Engineering Implementation                                                   | Operational Value                            |
| ------------------------------- | ---------------------------------------------------------------------------- | -------------------------------------------- |
| Centralized Management          | Manage switches from a dedicated Linux automation controller.                | Reduced administrative complexity.           |
| Secure Connectivity             | Use SSH key-based authentication and controlled administrative access.       | Stronger network security.                   |
| Configuration Standardization   | Apply reusable Python scripts, Netmiko workflows, and Ansible playbooks.     | Reduced configuration drift and human error. |
| Repeatability and Scalability   | Maintain structured inventories and modular automation components.           | Supports infrastructure growth.              |
| Automated Validation            | Verify connectivity, VLAN membership, interfaces, and configuration changes. | Improved deployment reliability.             |
| Auditability and Change Control | Preserve backups, logs, validation reports, and GitLab history.              | Better accountability and traceability.      |

Architecture Workflow: Automation Controller → Device Inventory → SSH Authentication → Core Network → ExtremeXOS Switches → VLAN Discovery & Deployment → Configuration Backups → Validation → GitLab & Reporting.

## 4.6 Simplified Troubleshooting Workflow

Project 4 applies a structured troubleshooting methodology to identify SSH connectivity failures, VLAN configuration mismatches, Python automation errors, Ansible playbook issues, and unsuccessful deployments.

| Workflow Stage        | Engineering Activities                                                                                                                                                      | Expected Outcome                                                     |
| --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| 1. Identify the Issue | Review errors and logs, test ping and SSH connectivity, identify affected switches and VLANs, and classify connectivity, authentication, inventory, or automation failures. | Problem identified and diagnostic evidence collected.                |
| 2. Check Device State | Execute ExtremeXOS verification commands, inspect VLAN membership and interfaces, review configurations and logs, and confirm SSH2 and RSA key authentication.              | Current device state verified and probable root cause isolated.      |
| 3. Run Automation     | Execute approved Python scripts or Ansible playbooks, apply authorized corrective changes, and troubleshoot YAML, inventory, Netmiko, SSH, or module errors.                | Automation or configuration issue corrected with execution evidence. |
| 4. Validate Results   | Verify VLAN IDs, membership, interface assignments, connectivity, SSH authentication, administrative accounts, and expected configurations.                                 | Successful remediation and intended network behavior confirmed.      |
| 5. Document & Back Up | Save switch configurations, archive backups and execution logs, document root causes and corrective actions, and commit reviewed artifacts to GitLab.                       | Recoverable configurations and reusable engineering documentation.   |
| Repeat and Improve    | Refine scripts, inventories, playbooks, validation checks, and troubleshooting procedures using recorded findings.                                                          | More secure, consistent, and reliable network automation.            |

### Troubleshooting Principles

| Engineering Principle         | Operational Practice                                                                                   |
| ----------------------------- | ------------------------------------------------------------------------------------------------------ |
| Evidence-Based Investigation  | Collect device outputs, SSH results, automation logs, and configuration records before making changes. |
| Secure Authentication         | Verify authorized SSH access without exposing private keys or credentials.                             |
| Inventory Accuracy            | Validate switch IP addresses, platform settings, groups, and connection parameters.                    |
| YAML Validation               | Check syntax, indentation, task structure, and inventory formatting.                                   |
| Controlled Changes            | Execute approved scripts, commands, and playbooks.                                                     |
| Backup and Rollback Readiness | Preserve configurations and maintain recovery procedures before disruptive changes.                    |
| Error Handling                | Detect authentication failures, invalid commands, and unsuccessful automation execution.               |
| Post-Deployment Validation    | Verify VLANs, administrative accounts, connectivity, and configuration accuracy.                       |
| Version Control               | Track approved automation changes using Git and GitLab.                                                |
| Documentation and Improvement | Record findings, corrective actions, and validation evidence to improve future workflows.              |

Troubleshooting Workflow: Identify → Inspect → Automate → Validate → Document & Back Up → Repeat.

## 4.7 Tools Used

Project 4 integrates industry-standard network automation, configuration management, secure connectivity, version control, and documentation technologies to automate enterprise switch administration and deployment.

| Tool / Technology            | Primary Function                                                                   | Engineering Value                                   |
| ---------------------------- | ---------------------------------------------------------------------------------- | --------------------------------------------------- |
| Python                       | Network automation scripting, VLAN discovery, deployment, backups, and validation. | Reusable automation and reduced manual effort.      |
| Netmiko                      | SSH connectivity and ExtremeXOS CLI command execution.                             | Programmatic device management.                     |
| Ansible                      | Configuration management and standardized administrative playbooks.                | Repeatable multi-device deployment.                 |
| Linux                        | Hosts Python, Netmiko, Ansible, SSH, inventories, and automation utilities.        | Centralized automation platform.                    |
| ExtremeXOS                   | Enterprise switching, VLAN configuration, and device administration.               | Practical switch automation environment.            |
| ExtremeXOS CLI               | Device configuration, troubleshooting, and verification.                           | Direct operational visibility and validation.       |
| SSH / RSA Keys               | Encrypted management connectivity and public-key authentication.                   | Secure administrative access.                       |
| YAML                         | Defines Ansible inventories, playbooks, and connection parameters.                 | Readable and maintainable automation configuration. |
| JSON                         | Stores structured automation results and device information.                       | Machine-readable reporting and integration.         |
| Git / GitLab                 | Version control, repository management, and change tracking.                       | Engineering traceability and accountability.        |
| Configuration Backups        | Archives switch configurations.                                                    | Recovery readiness and configuration preservation.  |
| Logs and Reports             | Records automation execution, errors, and validation results.                      | Troubleshooting evidence and auditability.          |
| Network Diagrams             | Documents topology, device relationships, VLANs, and connectivity.                 | Architecture communication and knowledge transfer.  |
| Markdown                     | Maintains README files, procedures, runbooks, and engineering records.             | Structured technical documentation.                 |
| Network Diagnostic Utilities | Ping, SSH diagnostics, and device verification commands.                           | Connectivity testing and fault isolation.           |

### Technology Integration Workflow

| Stage                    | Supporting Technologies                          | Engineering Function                                         |
| ------------------------ | ------------------------------------------------ | ------------------------------------------------------------ |
| Write Scripts            | Python, Linux                                    | Develop reusable automation logic.                           |
| Connect Devices          | Netmiko, SSH, RSA Keys                           | Establish secure device sessions.                            |
| Deploy Configurations    | Ansible, YAML, Python, Netmiko                   | Execute standardized configuration and administrative tasks. |
| Back Up and Log          | Python, Netmiko, configuration archives          | Preserve configurations and execution evidence.              |
| Version Control          | Git, GitLab, Markdown                            | Maintain reviewed automation assets and change history.      |
| Manage Switches          | ExtremeXOS CLI                                   | Perform authorized VLAN and device administration.           |
| Validate Results         | CLI, Python, Ansible, connectivity testing       | Verify configuration accuracy and expected behavior.         |
| Troubleshoot and Improve | Execution logs, SSH diagnostics, YAML validation | Resolve errors and refine automation workflows.              |

Toolchain Value: Secure Connectivity • Standardized Configuration • Automated Deployment • Reliable Backups • Operational Validation • Version Control.

## 4.8 Simplified Implementation

Project 4 establishes a secure and repeatable network automation framework through structured environment preparation, inventory management, SSH authentication, configuration deployment, verification, and documentation.

### Implementation Steps

| Step | Implementation Phase   | Engineering Activities                                                                                                                                        | Primary Deliverable                                                   |
| ---- | ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| 1    | Set Up Environment     | Prepare the Linux controller, install Python, Netmiko, and Ansible, configure project directories, verify connectivity, and generate RSA SSH keys.            | Functional network automation environment.                            |
| 2    | Create Inventory       | Define four managed ExtremeXOS switches, management IP addresses, hostnames, connection parameters, and Ansible inventory groups.                             | Validated device inventory.                                           |
| 3    | Implement SSH Security | Enable SSH2, distribute approved public keys, associate keys with administrative accounts, protect credentials, and verify key-based authentication.          | Secure administrative access.                                         |
| 4    | Deploy VLANs           | Back up configurations, discover existing VLANs, deploy departmental VLANs using Python and Netmiko, and execute approved Ansible administrative playbooks.   | Standardized VLAN configurations and automated device administration. |
| 5    | Verify & Back Up       | Validate VLANs, interfaces, SSH access, local administrator accounts, and connectivity; archive configurations and logs; commit reviewed artifacts to GitLab. | Validated deployment, configuration backups, and documentation.       |

### Implementation Methodology

| Phase           | Engineering Activities                                                               | Expected Outcome                                 |
| --------------- | ------------------------------------------------------------------------------------ | ------------------------------------------------ |
| Prepare         | Configure the automation controller, dependencies, and management connectivity.      | Automation environment ready.                    |
| Inventory       | Define managed switches, addresses, groups, and connection parameters.               | Accurate automation targets.                     |
| Secure          | Configure SSH2, RSA keys, and controlled administrative access.                      | Authenticated device management.                 |
| Back Up         | Retrieve and archive configurations before changes.                                  | Recovery baseline preserved.                     |
| Deploy          | Execute Python, Netmiko, and approved Ansible workflows.                             | Intended configurations applied.                 |
| Validate        | Verify VLANs, interfaces, SSH, accounts, and connectivity.                           | Deployment accuracy confirmed.                   |
| Document        | Preserve execution logs, troubleshooting records, diagrams, and validation evidence. | Reusable engineering documentation.              |
| Version Control | Commit reviewed and sanitized automation artifacts to GitLab.                        | Traceable development and configuration history. |

### Security and Engineering Considerations

| Security Control             | Implementation Requirement                                                                                               |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Credential Protection        | Never commit private SSH keys, passwords, API tokens, or authentication secrets to Git repositories.                     |
| Least Privilege              | Restrict administrative permissions to required operations where supported.                                              |
| Secure Secrets Management    | Use approved mechanisms for storing and accessing automation credentials.                                                |
| Approved Device Inventory    | Limit automation execution to authorized infrastructure.                                                                 |
| Configuration Backups        | Preserve recoverable configurations before potentially disruptive changes.                                               |
| YAML and Playbook Validation | Verify syntax, indentation, inventories, modules, and connection parameters before execution.                            |
| Controlled Testing           | Test scripts and playbooks in representative laboratory environments before production use.                              |
| Change Authorization         | Require approval for potentially disruptive configuration changes.                                                       |
| Idempotent Automation        | Avoid unnecessary repeated changes wherever supported.                                                                   |
| Rollback Readiness           | Maintain procedures for recovering from unsuccessful deployments.                                                        |
| Execution Logging            | Preserve script output, playbook results, errors, and validation evidence.                                               |
| GitLab Change Control        | Use version history, branches, and reviews for controlled automation development.                                        |
| Infrastructure Protection    | Exclude sensitive production addresses, configurations, and internal security information from public repositories.      |
| Sanitized Evidence           | Review logs, backups, diagrams, screenshots, and documentation before publication.                                       |
| Production Readiness         | Apply appropriate authorization, operational safeguards, security controls, and validation before production deployment. |

Implementation Lifecycle: Prepare → Inventory → Secure → Back Up → Deploy → Validate → Document → Version Control.

## 4.9 Project Outcomes

| Outcome Category            | Demonstrated Project Result                                                                                                                                               | Business & Engineering Value                                                         |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| Project Completion          | Successfully implemented, troubleshot, and validated the network automation laboratory.                                                                                   | Demonstrates end-to-end infrastructure automation engineering.                       |
| Managed Infrastructure      | Four ExtremeXOS access switches managed through a centralized Linux controller.                                                                                           | Multi-device network administration.                                                 |
| VLAN Deployment             | VLANs 10, 20, 30, and 40 configured and verified for IT, Management, Accounting, and Users.                                                                               | Standardized departmental network segmentation.                                      |
| Secure Administration       | RSA SSH key-based authentication implemented and verified.                                                                                                                | Stronger administrative access security.                                             |
| Python / Netmiko Automation | Reusable scripts for VLAN discovery, deployment, configuration backups, and verification.                                                                                 | Reduced manual work and repeatable device management.                                |
| Ansible Automation          | YAML inventories and playbooks supporting standardized device administration and local administrator account creation.                                                    | Consistent multi-device configuration management.                                    |
| Configuration Backups       | Switch configurations retrieved and archived.                                                                                                                             | Improved recovery readiness and change tracking.                                     |
| Network Validation          | Connectivity, SSH authentication, VLAN configurations, and administrative settings verified.                                                                              | Confirmed intended network functionality.                                            |
| Troubleshooting             | SSH, YAML, inventory, Python, and Ansible execution issues investigated and corrected.                                                                                    | Demonstrates practical troubleshooting and fault isolation.                          |
| Version Control             | GitLab repository maintained with automation scripts, playbooks, inventories, and documentation.                                                                          | Improved traceability and accountability.                                            |
| Engineering Deliverables    | Python scripts, Ansible playbooks, inventories, backups, logs, reports, architecture diagrams, screenshots, and runbooks.                                                 | Portfolio-ready technical evidence and reusable documentation.                       |
| Scalability                 | Modular automation framework designed for additional switches, VLANs, and network environments.                                                                           | Foundation for future infrastructure expansion.                                      |
| Business Outcomes           | Standardized configuration, secure administration, automated deployment, and operational validation.                                                                      | Potential improvements in efficiency, reliability, security, and continuity.         |
| Financial Perspective       | Illustrative $5.9 million combined annual value, 60% faster deployments, 2,800 annual engineering hours saved, 250% first-year ROI, and approximately five-month payback. | Hypothetical enterprise-scale benefits, not measured laboratory results.             |
| Final Project Result        | Successfully implemented and validated a secure, centralized, repeatable network automation framework for four ExtremeXOS switches.                                       | Faster Deployments. Stronger Security. Greater Reliability. Scalable Infrastructure. |

## Final Project Summary

| # | Category                                  | Final Project Summary                                                                                                                                                                                                                                      | Business & Technical Value                                                                                                           |
| - | ----------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| 1 | Project Overview                          | Demonstrates practical engineering capabilities in Python network automation, Netmiko device management, Ansible configuration management, VLAN deployment, SSH security, configuration backups, infrastructure troubleshooting, and technical validation. | Demonstrates end-to-end network automation, secure infrastructure management, and engineering proficiency.                           |
| 2 | Network Automation Architecture           | Integrates four ExtremeXOS switches with centralized automation using Python, Netmiko, and Ansible.                                                                                                                                                        | Reduces repetitive manual administration and supports consistent, scalable network operations.                                       |
| 3 | Secure Infrastructure Management          | Implements secure SSH authentication, standardized administrative workflows, and controlled network configuration procedures.                                                                                                                              | Strengthens network security, improves administrative consistency, and reduces configuration risks.                                  |
| 4 | Configuration Management and Preservation | Automates VLAN deployment, standardized device configurations, and configuration backups.                                                                                                                                                                  | Improves deployment reliability, configuration consistency, change tracking, and recovery readiness.                                 |
| 5 | Version Control and Documentation         | Integrates GitLab version control, configuration records, automation logs, and documented engineering evidence.                                                                                                                                            | Supports traceability, troubleshooting, technical validation, and continuous improvement.                                            |
| 6 | Engineering Competencies                  | Demonstrates Python scripting, Netmiko SSH automation, Ansible playbooks, YAML inventories, VLAN management, configuration backups, network troubleshooting, and validation.                                                                               | Provides practical engineering evidence relevant to network engineering, cybersecurity, infrastructure automation, and DevOps roles. |
| 7 | Final Project Result                      | A completed network automation laboratory integrating four ExtremeXOS switches, centralized automation, secure SSH authentication, standardized configurations, automated backups, GitLab version control, and documented validation.                      | Secure Automation. Consistent Configurations. Repeatable Deployments. Scalable Infrastructure.                                       |
| 8 | Final Takeaway                            | Network automation transforms repetitive manual administration into secure, consistent, repeatable, and scalable infrastructure management.                                                                                                                | Automate → Secure → Standardize → Validate → Scale.                                                                                  |

