---
layout: default
title: Step 3 - Design the Foundations
parent: AI Foundations Challenge
nav_order: 3
---

## Step 3: Design Challenges (Foundations & Workloads) (1.5 hours)

**Activity:** Address the following technical challenges by designing the Azure architecture for IFS. Create diagrams and list key Azure services.

### Challenge 1: Foundational Azure Environment (Platform Landing Zones)

* **Task:** Design the core Azure environment structure.
* **Questions:**
    * How will you structure Azure subscriptions to separate platform functions (like networking, identity) from application workloads?
    * What core services are needed for identity management, security monitoring, and policy enforcement across the entire Azure estate?
    * How will you establish secure network connectivity between Azure and IFS's on-premises locations?
    * How will you ensure consistent application of security policies and compliance standards?

### Challenge 2: Application & Workload Environments (Application Landing Zones)

* **Task:** Design the environment(s) where IFS will host its modernized applications, data platforms, and specific AI/ML workloads (excluding the central AI services hub for now).
* **Questions:**
    * What patterns will you use to provide standardized, secure environments for different types of applications (e.g., web apps, containerized services, data analytics)?
    * How will these environments securely connect to the foundational services (identity, networking, management)?
    * How will you ensure network segmentation between different applications or business units hosted in Azure?

**Success Criteria:**  
By the end of this step, participants should be able to:
- Present a high-level Azure architecture diagram addressing Challenge 1 and Challenge 2.
- Clearly explain how their design meets IFS's requirements for governance, security, compliance, scalability, and operational efficiency for foundational and workload environments.
- Identify and justify the selection of key Azure services and architectural patterns for each challenge.
- Demonstrate how private networking, centralized governance, and secure workload enablement are achieved.
- Provide rationale for design decisions, referencing IFS's business objectives and regulatory needs.

**Notes:**  
To effectively migrate, modernize, and innovate with applications at scale in Azure, a well-architected foundation is crucial. This is precisely what an Azure landing zone provides. Following key design principles across eight essential areas, it creates a scalable, modular, and consistent environment. A core tenet is the use of Azure subscriptions to provide isolation and enable independent scaling of both application and the underlying platform resources they depend on.

The scalable and modular nature of the Azure landing zone architecture allows it to meet varied deployment demands. By implementing a repeatable infrastructure, organizations can ensure consistent configurations and controls are applied across every subscription. The architecture is logically divided into two main categories of landing zones:

- Platform landing zones: These are subscriptions dedicated to hosting shared services vital for applications in the application landing zones, such as identity and access management, network connectivity, and centralized monitoring and governance. Managing these services centrally through platform landing zones increases operational efficiency. Examples include subscriptions specifically for identity, management, and connectivity.
- Application landing zones: These subscriptions are the designated environments for deploying and hosting applications. They are provisioned programmatically using infrastructure as code, and management groups are used to apply and enforce relevant policy controls for the applications within them.
