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
An Azure landing zone is a well-architected environment that follows key design principles across eight design areas to accommodate all application portfolios and enable application migration, modernization, and innovation at scale. These design principles ensure that the environment is scalable, modular, and consistent, allowing for the isolation and scaling of application and platform resources through subscriptions. The Azure landing zone architecture is designed to be scalable and modular, meeting various deployment needs. It uses a repeatable infrastructure that allows configurations and controls to be applied consistently across every subscription. The architecture is divided into two main types of landing zones:
- Platform landing zones are subscriptions that provide shared services such as identity, connectivity, and management to applications in application landing zones. These shared services are managed by one or more central teams, improving operational efficiency. Examples of platform landing zones include identity subscriptions, management subscriptions, and connectivity subscriptions.
- Application landing zones are subscriptions specifically for hosting applications. These zones are pre-provisioned through code and use management groups to assign policy controls.
