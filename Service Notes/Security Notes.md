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




