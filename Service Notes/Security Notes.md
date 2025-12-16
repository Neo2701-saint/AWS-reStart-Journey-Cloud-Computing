# **Cloud Computing Security Services Notes**

Cloud security is the combination of policies, controls, procedures, and technologies that protect cloud-based systems, data, and infrastructure from threats.

The fundamental principle governing cloud security is the Shared Responsibility Model.

---

1. **The Shared Responsibility Model**

This is the most critical concept. It defines what the Cloud Service Provider (CSP) is responsible for securing and what the Customer is responsible for securing.

_**Area of Responsibility,	CSP Responsibility (Security OF the Cloud) and	Customer Responsibility (Security IN the Cloud)**_

- **IaaS (e.g., VMs)**:	Physical facilities, Host OS, Virtualization Layer, Compute, Storage, Networking.
  -     Operating System, Applications, Data, Identity & Access Management (IAM), Network Configuration (e.g., Virtual Firewalls).
- **PaaS (e.g., App Service)**:	Everything in IaaS plus the Host OS, Middleware, and Runtime environment.
  -     Applications, Data, Identity & Access Management (IAM).
- **SaaS (e.g., Microsoft 365)**:	Nearly everything: Application, OS, Network, Data Center.
  -       Data (Classification, encryption, sensitivity), User Access (Passwords, MFA, User Provisioning).
 
Key Takeaway: Regardless of the service model, the customer is ALWAYS responsible for their data and the configuration of their access controls (IAM).    

---

2. **Core Security Service Categories**

Major cloud providers (AWS, Azure, GCP) offer services in these key areas:

_**A. Identity and Access Management (IAM)**_

  Goal: To ensure only authenticated and authorized users (or services) can access resources, adhering to the Principle of Least Privilege (PoLP).

    Services:

        - User/Group Management: Creating user identities and organizing them into groups.

        - Role-Based Access Control (RBAC): Assigning permissions based on a user's role (e.g., Admin, Developer, Viewer).

        - Multi-Factor Authentication (MFA): Requires users to provide multiple forms of verification to gain access.

        - AWS: IAM

        - Azure: Azure Active Directory (Azure AD / Microsoft Entra ID)

        - GCP: Cloud IAM

_**B. Data Protection (Encryption & Key Management)**_

  Goal: Protect sensitive data from unauthorized viewing, both when it's stored and when it's moving.

    Concepts:

        - Encryption at Rest: Encrypting data stored on disks (storage, databases).

        - Encryption in Transit: Encrypting data moving over networks (using TLS/SSL).

        - Bring Your Own Key (BYOK): Allowing customers to import and manage their own encryption keys.

    Services:

        - AWS: KMS (Key Management Service), Secrets Manager

        - Azure: Azure Key Vault

        - GCP: Cloud Key Management Service (KMS), Secret Manager

_**C. Network Security (Perimeter & Isolation)**_

  Goal: Isolate and protect virtual network environments, control inbound/outbound traffic, and prevent Denial of Service (DDoS) attacks.

    Services:

        - Virtual Private Cloud (VPC/VNet): Logically isolated section of the cloud network where resources are launched.

        - Security Groups/Network Security Groups (NSG): Virtual firewalls that control traffic to/from virtual machines.

        - Web Application Firewall (WAF): Protects web applications from common web exploits (e.g., SQL injection, cross-site scripting).

        - DDoS Protection: Automated services that defend against Distributed Denial of Service attacks.

        - AWS: VPC, Security Groups, AWS WAF, AWS Shield

        - Azure: Azure Virtual Network (VNet), NSG, Azure Firewall, Azure DDoS Protection

        - GCP: VPC, Cloud Armor, Cloud Firewall

_**D. Logging, Monitoring, and Threat Detection**_

  Goal: Provide visibility into all activities, automatically detect threats, and support incident response and auditing.

    Services:

        - Activity/API Logging: Recording all API calls and configuration changes (e.g., who did what, when, and from where).

        - Security Information and Event Management (SIEM) / Threat Detection: Services that analyze logs and activity data using machine learning to find suspicious patterns.

        - Vulnerability Scanning: Tools to scan environments (VMs, containers) for known vulnerabilities.

        - AWS: CloudTrail (API logging), GuardDuty (Threat Detection)

        - Azure: Azure Monitor, Azure Sentinel (SIEM), Microsoft Defender for Cloud (CSPM/CWPP)

        - GCP: Cloud Logging, Security Command Center

---

3. **Emerging Cloud Security Disciplines**

**Discipline, Focus and	Description**

- **CSPM**:	Cloud Security Posture Management
  -     Continuously monitors cloud configurations (IaaS, PaaS) for misconfigurations, policy violations, and compliance drift. A primary cause of breaches is often simple misconfiguration.

- **CWPP**:	Cloud Workload Protection Platforms
  -      Secures compute workloads like VMs, Containers (Docker), and Serverless Functions (Lambda/Functions) against threats at runtime.

- **CASB**:	Cloud Access Security Broker
  -     Security policy enforcement points placed between cloud service consumers and cloud service providers to ensure corporate security policies are extended to SaaS applications.

- **DevSecOps**:	Security in the Pipeline
  -     Integrating security testing and practices (like vulnerability scanning and code analysis) directly into the development and deployment pipelines.
