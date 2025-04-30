---
layout: default
title: Step 3 - Design the Foundations
parent: AI Foundations Challenge
nav_order: 3
---

## Step 3: Design Challenges (Foundations & Workloads) (1.5 hours)

**Activity:** Address the following technical challenges by designing the cloud architecture for IFS. Create diagrams illustrating your design and describe the key capabilities needed.

### Challenge 1: Foundational Cloud Environment (Platform Capabilities)

* **Task:** Design the core cloud environment structure that provides shared services and governance.
* **Questions:**
    * How will you structure the cloud environment's resources (e.g., subscriptions, resource groups, resources) to separate platform functions (like networking, identity) from application workloads?
    * How will you separate different operational environments (e.g., development, testing, production) within the cloud environment?
    * What capabilities will you use to manage identity and control access across the entire cloud estate?
    * How will you implement centralized monitoring and logging for all cloud resources?
    * How will you ensure that all cloud resources are compliant with IFS's security and governance policies (e.g., financial regulations)?
    * How will you manage and enforce policies consistently across the different organizational units?
    * How will you implement a secure and scalable network architecture, including connectivity to existing data centers?
    * How will you ensure that all cloud infrastructure is deployed in a secure, compliant, and repeatable manner?
    * How will you manage and monitor costs across the cloud environment?
  
### Challenge 2: Application & Workload Environments (Application Hosting Capabilities)

* **Task:** Design the standardized environment(s) where IFS will host its modernized applications, data platforms, and specific AI/ML workloads.
* **Questions:**
    * What patterns will you use to provide standardized, secure environments suitable for different types of applications (e.g., web apps, containerized services, data analytics, AI models)?
    * How will these application environments securely connect to and consume the foundational shared services (identity, networking, management)?
    * How will you ensure network segmentation and isolation between different applications or business units hosted in the cloud?
    * How will you implement security controls for data protection (at rest and in transit) within these application environments?
    * How will you manage secrets and sensitive configuration information securely within the application environments?
    * What capabilities will you use to monitor and log activities specific to the applications within their environments?
    * How will automated deployment pipelines (CI/CD) interact with these standardized application environments?

---

**Success Criteria:**  
By the end of this step, participants should be able to:
- Present an Azure architecture diagram illustrating:
    - Management Group and Subscription structure (clearly delineating Platform and Application Landing Zones).
    - Hub-and-Spoke network topology, including core networking services (e.g., Azure Firewall, ExpressRoute/VPN Gateway).
    - Key identity and management services (e.g., Microsoft Entra ID integration, Azure Monitor, Azure Policy).
- Explain how the proposed Landing Zone design specifically addresses the requirements captured in Step 2 for:
    - **Governance:** Centralized policy enforcement, resource organization, separation of duties.
    - **Security & Compliance:** Meeting regulations (PCI DSS, GDPR), data protection, threat monitoring.
    - **Connectivity:** Secure hybrid connection, network segmentation.
    - **AI Service Enablement:** Providing a foundation for secure AI service access (even if detailed in later modules).
    - **Scalability & Operations:** Supporting growth, operational efficiency, reliability.
- List and justify the selection of **at least five** key Azure services (e.g., Azure Policy, Azure Firewall, Microsoft Entra ID PIM, Azure Monitor, Azure Key Vault) and explain their role within the Platform and Application Landing Zones.
- Demonstrate how the design implements core Landing Zone principles, including private networking (e.g., use of Private Endpoints where applicable), centralized governance through Azure Policy, and secure workload isolation.
- Articulate the rationale for major design decisions, explicitly linking them back to specific IFS business objectives (e.g., reducing costs, improving innovation speed) and regulatory requirements identified in Step 1 and Step 2.

---
  
**Notes:**  
To effectively migrate, modernize, and innovate with applications at scale in Azure, a well-architected foundation is crucial. This is precisely what an Azure landing zone provides. Following key design principles across eight essential areas, it creates a scalable, modular, and consistent environment. A core tenet is the use of Azure subscriptions to provide isolation and enable independent scaling of both application and the underlying platform resources they depend on.

The scalable and modular nature of the Azure landing zone architecture allows it to meet varied deployment demands. By implementing a repeatable infrastructure, organizations can ensure consistent configurations and controls are applied across every subscription. The architecture is logically divided into two main categories of landing zones:

- Platform landing zones: These are subscriptions dedicated to hosting shared services vital for applications in the application landing zones, such as identity and access management, network connectivity, and centralized monitoring and governance. Managing these services centrally through platform landing zones increases operational efficiency. Examples include subscriptions specifically for identity, management, and connectivity.
- Application landing zones: These subscriptions are the designated environments for deploying and hosting applications. They are provisioned programmatically using infrastructure as code, and management groups are used to apply and enforce relevant policy controls for the applications within them.
