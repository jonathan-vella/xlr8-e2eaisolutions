---
layout: default
title: Step 2 - Define Requirements
parent: AI Hub Challenge
nav_order: 2
---

## Step 2: Define Requirements (45 minutes)

**Activity:** Based on the scenario and the experience gained from the RAG chatbot implementation, define the specific requirements for a centralized AI services hub that addresses the limitations encountered and scales to support enterprise-wide AI adoption.

**Outcome:** Document requirements covering the following areas:

* **Network Isolation Requirements:**
    * Requirement: All Azure services within the hub (AI services, data stores, compute/orchestration logic, access gateway) must use private endpoints or VNet integration.
    * Requirement: No public internet exposure for any of the hub's AI services or components.
    * Requirement: Secure cross-VNet connectivity to allow multiple application landing zones to access the AI Hub.
    * Requirement: Network traffic filtering and inspection capabilities at the entry point to the hub.

* **Access Control Requirements:**
    * Requirement: A secure, managed gateway or proxy must be the sole entry point for accessing AI capabilities.
    * Requirement: Support for strong authentication mechanisms, including Azure AD.
    * Requirement: Fine-grained authorization controls to limit access to specific AI services based on department or project needs.
    * Requirement: Support for rate limiting, request validation, and potentially Web Application Firewall (WAF) capabilities.

* **Secrets Management Requirements:**
    * Requirement: Centralized secure storage for all API keys, connection strings, and other secrets.
    * Requirement: Secure runtime access to secrets by applications/services without exposure in code or configuration files.
    * Requirement: Automated rotation capability for secrets where applicable.
    * Requirement: Audit trail for secret access and usage.

* **Monitoring and Logging Requirements:**
    * Requirement: Detailed logging of all API requests to AI services for security and compliance purposes.
    * Requirement: Performance monitoring for all components within the hub (gateway, AI services, compute).
    * Requirement: Usage tracking and reporting for cost allocation and chargeback to different business units.
    * Requirement: Security event monitoring and alerting capabilities.

* **Governance Requirements:**
    * Requirement: Ability to enforce specific policies for resources deployed within the AI Hub.
    * Requirement: Controls for provisioning and management of AI service instances.
    * Requirement: Monitoring for compliance with security and regulatory standards.
    * Requirement: Cost management and quota enforcement mechanisms for different departments.
    * Requirement: Centralized governance of prompt engineering best practices and model configurations.

* **Scalability Requirements (Based on RAG Implementation Learnings):**
    * Requirement: The hub must support multiple AI workloads across different departments simultaneously.
    * Requirement: Ability to easily onboard new AI services as requirements evolve.
    * Requirement: Support for varying performance needs across different business units.
    * Requirement: Clear process for requesting and provisioning new AI capabilities.

**Success Criteria:**  
By the end of this step, participants should be able to:
- Clearly list and categorize the key functional and non-functional requirements for the AI Hub.
- Ensure requirements address network isolation, access control, secrets management, monitoring, governance, and scalability.
- Demonstrate alignment of requirements with IFS's business objectives and regulatory obligations.
- Explain how these requirements address the limitations observed in the initial RAG chatbot implementation.
- Provide a requirements summary that will guide the subsequent architecture design step.