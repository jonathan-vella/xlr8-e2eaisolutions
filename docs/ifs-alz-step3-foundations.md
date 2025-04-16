---
layout: default
title: Step 3 - Design the Foundations
parent: AI Foundations Challenge
nav_order: 3
---

## Step 3: Design Challenges (Foundations & Workloads) (1.5 hours)

**Activity:** Address the following technical challenges by designing the Azure architecture for IFS. Create diagrams and list key Azure services.

### Challenge 1: Foundational Azure Environment (Landing Zones)

* **Task:** Design the core Azure environment structure. How will you organize subscriptions and resources to meet IFS's requirements for governance, security, and separation? Consider identity, management, and connectivity.
* **Questions:**
    * How will you structure Azure subscriptions to separate platform functions (like networking, identity) from application workloads?
    * What core services are needed for identity management, security monitoring, and policy enforcement across the entire Azure estate?
    * How will you establish secure network connectivity between Azure and IFS's on-premises locations?
    * How will you ensure consistent application of security policies and compliance standards?

### Challenge 2: Application & Workload Environments (Landing Zones)

* **Task:** Design the environment(s) where IFS will host its modernized applications, data platforms (like data lakes, analytics engines), and specific AI/ML workloads (excluding the central AI services hub for now).
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