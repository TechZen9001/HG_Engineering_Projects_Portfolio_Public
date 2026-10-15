# Project 5 – Network Automation & Deployment: Infrastructure Automation with Terraform, Ansible, & Python

AWS Cloud Engineering • Infrastructure as Code • Configuration Management • Python Automation • DevOps • Cloud Security

Plan • Provision • Configure • Validate • Automate • Optimize

![Project 5 – Infrastructure Automation](5.%20Network%20Automation%20%26%20Deployment%20-%20Infrastructure%20Automation.png)

Project Overview: Design and implement an automated Amazon Web Services (AWS) cloud infrastructure solution using Terraform, Ansible, and Python to provision Linux servers, configure operating systems and user accounts, validate SSH connectivity, generate structured reports, and establish a secure, scalable, repeatable infrastructure deployment process.

The Project 5 infographic provides a consolidated visual overview. Each section below provides additional business, technical, architectural, implementation, troubleshooting, and validation context.

## Project Documentation

| Section | Documentation | Detailed Guide | Infographic |
|---|---|---|---|
| 5.2 | Executive Overview | [Read Documentation](5.2%20Executive-Overview.md) | [View Infographic](infographics/5.2%20Executive-Overview%20A.png) |
| 5.3 | Business Value | [Read Documentation](5.3%20Business-Value.md) | [View Infographic](infographics/5.3%20Business-Value%20A.png) |
| 5.4 | Technical Value | [Read Documentation](5.4%20Technical-Value.md) | [View Infographic](infographics/5.4%20Technical%20Value%20A.png) |
| 5.5 | Solution Architecture | [Read Documentation](5.5%20Solution-Architecture.md) | [View Infographic](infographics/5.5%20Solution-Architecture.png) |
| 5.6 | Simplified Troubleshooting Workflow | [Read Documentation](5.6%20Simplified-Troubleshooting-Workflow.md) | [View Infographic](infographics/5.6%20Simplified-Troubleshooting-Workflow.png) |
| 5.7 | Tools Used | [Read Documentation](5.7%20Tools-Used.md) | [View Infographic](infographics/5.7%20Tools-Used.png) |
| 5.8 | Simplified Implementation | [Read Documentation](5.8%20Simplified-Implementation.md) | [View Infographic](infographics/5.8%20Simplified-Implementation.png) |
| 5.9 | Project Outcomes | [Read Documentation](5.9%20Project-Outcomes.md) | [View Infographic](infographics/5.9%20Project-Outcomes%20A.png) |

## 5.2 Executive Overview

| Area                  | Business Challenge / Objective                            | Engineering Solution                                                        |
| --------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------- |
| Cloud provisioning    | Manual deployments are slow and error-prone               | Terraform Infrastructure as Code for VPC, subnets, Security Groups, EC2     |
| Linux administration  | Manual account management and inconsistent configurations | Ansible inventory and YAML playbooks create `test_user1` on Ubuntu and RHEL |
| Network security      | Inconsistent remote access controls                       | SSH key authentication, restricted Security Groups, IAM principles          |
| Validation            | Connectivity problems may remain undetected               | Python TCP port 22 checks and CSV reporting                                 |
| Governance            | Fragmented configuration and change history               | Git/GitLab, diagrams, logs, screenshots, Markdown                           |
| Scalability and costs | Growing infrastructure and resource waste                 | Reusable automation and cost-aware cleanup                                  |

Workflow: Provision → Configure → Validate → Report → Version Control → Improve.

## 5.3 Business Value

| # | Strategic Business Benefit              | Technical Enabler                    | Expected Enterprise Value              |
| - | --------------------------------------- | ------------------------------------ | -------------------------------------- |
| 1 | Faster Infrastructure Deployment        | Terraform + Ansible                  | Faster environment readiness           |
| 2 | Reduced Operational Costs               | Automated administration and cleanup | Less repetitive effort and waste       |
| 3 | Stronger Cloud Security                 | SSH, IAM, Security Groups            | Controlled administrative access       |
| 4 | Configuration Consistency & Reliability | IaC and playbooks                    | Less drift and rework                  |
| 5 | Scalability and Flexibility             | Reusable modules and scripts         | Extensible cloud environments          |
| 6 | Greater Engineering Productivity        | Automated configuration and testing  | More time for higher-value engineering |
| 7 | Faster Time to Value & Business Agility | Repeatable deployment workflows      | Faster cloud service delivery          |
| 8 | DevOps Enablement                       | Terraform, Ansible, Python, GitLab   | Integrated engineering lifecycle       |
| 9 | Improved Governance & Visibility        | Git history, CSV, logs, diagrams     | Traceability and audit readiness       |

### Illustrative Enterprise Financial Scenario

| Metric                     | Illustrative Estimate | Meaning                               |
| -------------------------- | --------------------- | ------------------------------------- |
| Annual operational savings | $2.1M                 | Modeled reduced administration        |
| Annual avoided downtime    | $3.8M                 | Modeled reduced service interruptions |
| Combined annual value      | $5.9M                 | Gross modeled benefit before expenses |
| Deployment speed           | 60% faster            | Hypothetical improvement              |
| Annual engineering time    | 2,800 hours saved     | Hypothetical productivity benefit     |
| First-year ROI             | 250%                  | Hypothetical financial assumption     |
| Payback                    | \~5 months            | Hypothetical cash-flow assumption     |

Financial disclosure: These figures are illustrative enterprise scenarios, not measured laboratory or production results. The $5.9M is modeled gross, not verified net benefit. ROI and payback require consistent investment, operating expense, benefit-realization, and cash-flow assumptions.

## 5.4 Technical Value

| # | Engineering Capability                       | Demonstrated Implementation                                                   | Value                                |
| - | -------------------------------------------- | ----------------------------------------------------------------------------- | ------------------------------------ |
| 1 | Terraform Infrastructure as Code             | AWS provider, reusable definitions, init/validate/plan/apply, state awareness | Repeatable provisioning              |
| 2 | AWS Cloud Infrastructure Provisioning        | VPC, two public subnets, routes, Security Groups, two EC2 hosts               | Cloud network and compute skills     |
| 3 | Ansible Configuration Management             | Inventory, SSH parameters, YAML playbook, `test_user1`                        | Standardized Linux administration    |
| 4 | Python Infrastructure Validation & Reporting | TCP port 22 tests, error handling, CSV                                        | Automated network-level verification |
| 5 | Secure Cloud Networking & Access Control     | SSH keys, Security Groups, IAM/least privilege, credential protection         | Security-conscious administration    |
| 6 | Automated Deployment Verification            | AWS/EC2 checks, Ansible output, SSH and Python results                        | Complementary validation             |
| 7 | Modular Architecture & Scalability           | Reusable Terraform, Ansible, Python components                                | Expansion readiness                  |
| 8 | Version Control & Change Management          | Git/GitLab and documented evidence                                            | Traceability                         |
| 9 | Engineering Competencies                     | AWS, Linux, networking, IaC, YAML, Python, SSH, DevOps                        | Transferable technical skills        |

Validation distinction: TCP port 22 reachability is not proof of successful SSH authentication, Linux permissions, application health, or overall deployment success. Those are separately checked.

Illustrative technical targets, not measured outcomes: 70% fewer configuration errors, 95% validation coverage, 100% automated reporting, 99.9% uptime/deployment success, 60% fewer security incidents, 100% policy compliance, 3× faster scaling, and 100% change traceability.

## 5.5 Solution Architecture

### AWS Network Components

| Component                         | Illustrative Configuration                     | Purpose                       |
| --------------------------------- | ---------------------------------------------- | ----------------------------- |
| Developer workstation             | Terraform, Ansible, Python, Git, VS Code, Bash | Centralized automation        |
| VPC                               | `10.0.0.0/16`                                  | Isolated AWS network          |
| Public subnet A                   | `10.0.1.0/24`                                  | Ubuntu EC2 placement          |
| Ubuntu EC2                        | Private IP `10.0.1.10`                         | Application/tools Linux host  |
| Public subnet B                   | `10.0.2.0/24`                                  | RHEL EC2 placement            |
| RHEL EC2                          | Private IP `10.0.2.10`                         | Management Linux host         |
| Internet Gateway and route tables | Appropriate routes                             | External connectivity         |
| Security Groups                   | Approved inbound/outbound rules                | Network access controls       |
| SSH key pair                      | Approved management identity                   | Authenticated remote access   |
| Ansible inventory                 | Ubuntu/RHEL groups and public IPs              | Managed configuration targets |
| Python + CSV                      | TCP 22 tests and reports                       | Validation evidence           |

Private addresses are illustrative. Actual public IPs are collected after provisioning. Public subnet placement alone does not ensure public reachability.

### End-to-End Automation Workflow

| Phase           | Tool                  | Activity                                    | Evidence                    |
| --------------- | --------------------- | ------------------------------------------- | --------------------------- |
| 1. Define       | Terraform             | Write resources; initialize, validate, plan | Reviewed configuration      |
| 2. Provision    | Terraform/AWS         | Create VPC, subnets, security and EC2       | Apply output and AWS checks |
| 3. Discover     | AWS/Terraform outputs | Collect public IPs and identifiers          | Host inventory              |
| 4. Authenticate | SSH                   | Verify authorized key-based login           | SSH result                  |
| 5. Configure    | Ansible               | Create `test_user1` on both Linux hosts     | Playbook and account checks |
| 6. Validate     | Python                | Test TCP port 22                            | Connection results          |
| 7. Report       | CSV                   | Record host and connection status           | CSV file                    |
| 8. Manage       | Git/GitLab            | Commit reviewed code and documentation      | Repository history          |

### Architecture Design Principles

| Principle                      | Engineering Practice                                                                             |
| ------------------------------ | ------------------------------------------------------------------------------------------------ |
| Security by design             | IAM least privilege, SSH keys, restricted Security Groups, protected secrets and Terraform state |
| Separation of responsibilities | Terraform provisions; Ansible configures; Python validates; GitLab tracks                        |
| Repeatability                  | Reusable IaC, inventories, playbooks and scripts                                                 |
| Controlled change              | Plan review, syntax checks, execution evidence, rollback readiness                               |
| Operational visibility         | Correlate AWS, Terraform, SSH, Ansible, Python and CSV records                                   |
| Cost control                   | Resource reviews and optional Terraform cleanup                                                  |
| Production readiness           | Lab uses public subnets; production management should favor private access and hardened controls |

## 5.6 Simplified Troubleshooting Workflow

| Step                    | Diagnostic Activities                                                         | Verification                                                   | Expected Outcome                                    |
| ----------------------- | ----------------------------------------------------------------------------- | -------------------------------------------------------------- | --------------------------------------------------- |
| 1. Check Deployment     | Terraform configuration, AWS provider, IAM, plan/apply errors                 | `terraform init`, `terraform validate`, `terraform plan`, logs | Expected resources created                          |
| 2. Check Instance State | EC2 health, public IPs, subnets, routes, Security Groups                      | AWS Console/CLI                                                | Running and properly networked instances            |
| 3. Test Connectivity    | TCP 22, SSH keys/usernames, network ACLs, host firewall; ICMP where permitted | Python TCP tests and SSH diagnostics                           | Reachability and authentication separately verified |
| 4. Check Configuration  | Inventory, YAML, playbook results, Linux user permissions                     | `ansible-playbook --syntax-check`, Linux CLI                   | `test_user1` configured                             |
| 5. Validate & Report    | Repeat checks, inspect CSV, document correction, commit artifacts             | Python, CSV, GitLab                                            | Reproducible validation evidence                    |

| Six-Stage Methodology | Purpose                                                                     |
| --------------------- | --------------------------------------------------------------------------- |
| Identify              | Detect infrastructure or automation failure                                 |
| Diagnose              | Gather Terraform, AWS, SSH, Ansible and Python evidence                     |
| Isolate               | Locate provisioning, networking, authentication, Linux or script root cause |
| Resolve               | Apply approved targeted correction                                          |
| Validate              | Rerun checks and verify results                                             |
| Document              | Preserve symptoms, root causes, actions, logs, screenshots and reports      |

Principles: Evidence-based diagnosis, secure access, configuration consistency, controlled changes, error handling, Terraform state protection, rollback readiness, version control, cost awareness, continuous improvement.

## 5.7 Tools Used

| Tool / Technology                               | Engineering Function                        |
| ----------------------------------------------- | ------------------------------------------- |
| Terraform                                       | AWS Infrastructure as Code                  |
| Ansible                                         | Linux configuration and user automation     |
| Python                                          | TCP connectivity validation and CSV reports |
| AWS / EC2                                       | Cloud platform and Linux compute            |
| VPC / subnets / route tables / Internet Gateway | Network isolation, addressing and routing   |
| Security Groups / IAM                           | Network and cloud permission controls       |
| Ubuntu / RHEL                                   | Managed Linux operating systems             |
| SSH / SSH key pairs                             | Secure remote administration                |
| YAML / INI                                      | Ansible inventory and playbook formats      |
| CSV                                             | Structured reporting                        |
| AWS CLI / Linux CLI                             | Cloud and OS diagnostics                    |
| Visual Studio Code / Bash                       | Development and command execution           |
| Git / GitLab                                    | Version control and repository management   |
| Markdown / diagrams / logs                      | Documentation and validation evidence       |

| Integration             | Output                                    |
| ----------------------- | ----------------------------------------- |
| Terraform → AWS         | VPC, subnets, security, EC2               |
| Ansible → Linux         | Configured accounts and system settings   |
| Python → CSV            | Network-level SSH reachability report     |
| Git/GitLab → repository | Version-controlled code and documentation |

## 5.8 Simplified Implementation

| Step                      | Implementation Activities                                                                                    | Deliverable                               |
| ------------------------- | ------------------------------------------------------------------------------------------------------------ | ----------------------------------------- |
| 1. Write Terraform Code   | Define VPC, subnets, routing, Security Groups, Ubuntu/RHEL EC2; run init, validate, plan, apply; collect IPs | AWS resources and Terraform files         |
| 2. Configure with Ansible | Create inventory, SSH settings and YAML playbook; create and verify `test_user1`                             | Managed Linux hosts and Ansible artifacts |
| 3. Validate with Python   | Test TCP 22, handle errors/timeouts, record host, OS, IP, status, timestamp                                  | Python script and CSV report              |
| 4. Document & Commit      | Preserve sanitized logs, screenshots, architecture, reports and Git history                                  | Version-controlled engineering evidence   |
| 5. Clean Up (Optional)    | Review state and `terraform plan -destroy`; authorize `terraform destroy`; check AWS billing/resources       | Cost-aware cleanup                        |

### Detailed Implementation Methodology

| Phase     | Activity                                             | Verification               |
| --------- | ---------------------------------------------------- | -------------------------- |
| Plan      | Define infrastructure, security and success criteria | Requirements               |
| Build     | Develop and apply Terraform                          | AWS provisioning results   |
| Configure | Ansible inventory, SSH and user playbook             | Account and task results   |
| Validate  | Inspect AWS, SSH and Linux settings                  | Deployment evidence        |
| Test      | Run Python connectivity and CSV reporting            | TCP status report          |
| Document  | Capture diagrams, logs, screenshots and commits      | Reusable project artifacts |

### Deliverables and Security Considerations

| Deliverable                              | Engineering Evidence                      |
| ---------------------------------------- | ----------------------------------------- |
| Infrastructure design and Terraform code | VPC, EC2, security and deployment records |
| Ansible inventory and playbook           | Managed host groups and user creation     |
| Python script and CSV report             | TCP port 22 connectivity results          |
| GitLab repository and documentation      | Code, logs, diagrams and screenshots      |

| Security / Production Consideration | Requirement                                                             |
| ----------------------------------- | ----------------------------------------------------------------------- |
| Credentials and secrets             | Never publish AWS keys, SSH private keys, passwords or Ansible secrets  |
| Terraform state                     | Protect and exclude sensitive state files from public repositories      |
| Administrative access               | Least-privilege IAM and Linux permissions; restrict SSH sources         |
| Public portfolio                    | Sanitize active IPs, confidential records, screenshots and logs         |
| Production networking               | Prefer private management access over lab-style public management hosts |
| Change safety                       | Review plans/playbooks; document backup and recovery procedures         |
| Cost management                     | Review resources, billing and optional cleanup                          |
| Accurate reporting                  | Distinguish lab results from enterprise projections                     |

## 5.9 Project Outcomes

### Key Outcomes

| # | Outcome                                    | Demonstrated Result                                                |
| - | ------------------------------------------ | ------------------------------------------------------------------ |
| 1 | AWS Infrastructure Deployed with Terraform | VPC, networking, Security Groups and two EC2 Linux instances       |
| 2 | Linux Configuration Automated with Ansible | Ubuntu/RHEL inventory and `test_user1` user creation               |
| 3 | Connectivity Validated with Python         | TCP port 22 checks on both EC2 hosts and CSV reporting             |
| 4 | Infrastructure as Code                     | Reusable Terraform configurations and provisioning workflow        |
| 5 | Version Control with Git/GitLab            | Managed infrastructure code, scripts, playbooks and documentation  |
| 6 | Secure Cloud Engineering Practices         | SSH key authentication, Security Groups, controlled administration |
| 7 | Repeatable End-to-End Automation Workflow  | Terraform → Ansible → Python → CSV → Git/GitLab                    |

### Project Results and Deliverables

| Category         | Final Result                                                                    | Portfolio Value                                |
| ---------------- | ------------------------------------------------------------------------------- | ---------------------------------------------- |
| Infrastructure   | Two AWS EC2 Linux instances provisioned                                         | AWS networking and compute engineering         |
| Configuration    | Ansible playbook created approved Linux account                                 | Multi-distribution automation                  |
| Validation       | Python verified TCP 22 reachability                                             | Automated network-level testing                |
| Reporting        | CSV infrastructure status report                                                | Machine-readable engineering evidence          |
| Security         | SSH and AWS network access controls                                             | Security-conscious engineering                 |
| Troubleshooting  | Terraform, AWS, SSH, Ansible and Python investigation                           | Systematic fault isolation                     |
| Documentation    | Terraform code, inventories, playbooks, scripts, diagrams, screenshots and logs | Reusable technical portfolio                   |
| Business impact  | Faster, more consistent and scalable deployments as intended benefits           | Enterprise automation value proposition        |
| Financial impact | $5.9M gross modeled annual value; 250% illustrative ROI                         | Hypothetical enterprise scenario, not measured |

### Final Project Conclusion

| Category                 | Summary                                                                                                                                                          |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Technical Result         | Successfully implemented and validated an AWS infrastructure automation laboratory integrating Terraform, Ansible, Python, and Git/GitLab.                       |
| Engineering Competencies | AWS cloud networking, IaC, Linux administration, SSH security, Ansible configuration, Python automation, troubleshooting, reporting, and documentation.          |
| Business Value           | Demonstrates how standardized automation can reduce manual work, improve deployment consistency, strengthen security, and support future cloud growth.           |
| Portfolio Value          | End-to-end evidence of design, provisioning, configuration, validation, troubleshooting, and documentation for cloud, network, and DevOps engineering audiences. |
| Executive Takeaway       | Terraform provisions; Ansible configures; Python validates; Git/GitLab tracks.                                                                                   |
| Final Project Value      | Infrastructure as Code · AWS Cloud Automation · Secure Linux Administration · Repeatable Deployments · Enterprise Business Value                                 |
