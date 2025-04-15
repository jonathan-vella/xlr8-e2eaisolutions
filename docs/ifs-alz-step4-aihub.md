---
layout: default
title: Step 4 - Centralize AI Services
parent: AI Foundations Challenges
nav_order: 4
---

## Step 4: Design Challenge – Centralized & Secure AI Service Hub (1.5 hours)

**Activity:** Design the dedicated, secure "AI Hub" environment to host and manage shared Azure AI services (like Azure OpenAI, Azure AI Search) and orchestration logic. This hub must act as the single, controlled gateway for accessing these services, enforcing strict security and governance. Private networking is mandatory for all components.

### Challenge 3: Centralized & Secure AI Service Hub

* **Core Requirements:**
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

**Success Criteria:**  
By the end of this step, participants should be able to:
- Present a high-level Azure architecture diagram for the AI Hub.
- Clearly explain how the design meets IFS's requirements for security, private networking, centralized access, and governance for shared AI services.
- Identify and justify the selection of key Azure services and architectural patterns for the AI Hub.
- Demonstrate how secure access, secrets management, and monitoring are achieved.
- Provide rationale for design decisions, referencing IFS's business objectives and regulatory needs.