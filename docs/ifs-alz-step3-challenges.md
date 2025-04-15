---
layout: default
title: Step 3 - Design Challenges
parent: AI Foundation & Hub Challenge
nav_order: 3
---

## Step 3: Design Challenges (3 hours)

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

### Challenge 3: Centralized & Secure AI Service Hub

* **Context:** IFS requires a dedicated, secure environment (the "AI Hub") to host and manage shared Azure AI services (like Azure OpenAI, Azure AI Search) and potentially the logic that orchestrates them (e.g., prompt flows). This hub must act as the single, controlled gateway for accessing these services, enforcing strict security and governance. Private networking is mandatory for all components.
* **Core Requirements derived from baseline:**
    * **Network Isolation:** All Azure services used within this hub (AI services, data stores, compute/hosting for AI logic, access gateway) must communicate exclusively over private network connections, with no public internet exposure.
    * **Secure Access Point:** A managed, secure gateway or proxy must be implemented as the sole entry point for accessing the AI capabilities hosted within the hub. This gateway should also support security enforcement (e.g., request validation, potentially WAF).
    * **Secure Secrets Management:** API keys, connection strings, and other secrets must be stored securely and accessed by applications/services without being exposed in code or configuration files.
    * **Comprehensive Monitoring:** Detailed logging and monitoring must be in place for usage, performance, and security events across all components in the hub (gateway, AI services, compute).
    * **AI Workload Governance:** Apply specific policies to govern the resources and configurations within this AI Hub.
* **Design Questions:**
    * How will you ensure that access to the core PaaS services (like Azure OpenAI, Azure AI Search, Azure Storage if used for related data) is restricted solely to private network endpoints within the AI Hub's virtual network?
    * What specific Azure service(s) could function as the secure, managed entry point (reverse proxy/API gateway) for AI requests into the hub? How would you configure it to enhance security (e.g., firewall capabilities)?
    * Considering the strict private networking requirement, how will other IFS applications running in separate Application Landing Zones securely connect to *only* the designated entry point of this AI Hub? What networking mechanisms facilitate this private cross-environment communication?
    * How will applications and services within the AI Hub securely obtain necessary secrets (like the Azure OpenAI API key) at runtime?
    * What specific Azure services and configurations will you use to implement the required comprehensive monitoring and logging for the AI Hub components?
    * If IFS needs to host custom AI orchestration logic (like prompt flows) within this hub, what Azure compute service(s) could host this securely within the private network, and how would they integrate with the VNet?
    * Within Azure, how will internal DNS resolution be handled to ensure services correctly resolve the private IP addresses of the various components (like Azure OpenAI, the gateway, etc.) within the hub and across connected networks?
    * Which Azure Policy definitions are relevant for enforcing governance specifically for the resources deployed within this AI Hub (e.g., enforcing private endpoints, specific SKUs, tagging)?