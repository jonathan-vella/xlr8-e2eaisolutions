---
layout: default
title: Step 3 - Design Architecture
parent: AI Hub Challenge
nav_order: 3
---

## Step 3: Design the AI Hub Architecture (2 hours)

**Activity:** Design the end-to-end architecture for the "AI Hub" based on the lessons learned from the RAG chatbot implementation. Create diagrams showing components, interactions, networking, and key Azure services. Address the questions below.

**Challenge Questions:**

1. **Evolution from RAG Implementation:**
   * What limitations or challenges did you identify in how AI services were accessed during the RAG chatbot implementation?
   * How does this AI Hub design address these challenges and provide a more scalable solution?
   * What specific architectural components need to change as IFS moves from a single AI workload to multiple workloads across different departments?

2. **Network Isolation:**
   * How will you ensure that access to the core PaaS services (Azure OpenAI, Azure AI Search, Azure Storage if used for related data) is restricted solely to private network endpoints within the AI Hub's virtual network?
   * What networking components are required to isolate the AI Hub while still allowing authorized access from multiple application landing zones?
   * How will you implement network security groups (NSGs) and other network security controls to enforce proper segmentation?

3. **Secure Access Point:**
   * What specific Azure service(s) could function as the secure, managed entry point (reverse proxy/API gateway) for AI requests into the hub? 
   * How would you configure this entry point to enhance security (e.g., firewall capabilities, authentication, authorization)?
   * What mechanisms will you implement for rate limiting, request validation, and traffic management?

4. **Cross-Environment Connectivity:**
   * How will multiple IFS applications running in separate Application Landing Zones securely connect to the AI Hub services?
   * What networking mechanisms facilitate this private cross-environment communication?
   * How will you enforce that only approved applications can access the AI Hub services?

5. **Secrets Management:**
   * How will applications and services within the AI Hub securely obtain necessary secrets (like the Azure OpenAI API key) at runtime?
   * What service will you use for centralized secrets storage, and how will it be secured?
   * How will you implement a rotation strategy for secrets where applicable?

6. **Monitoring and Logging:**
   * What specific Azure services and configurations will you use to implement comprehensive monitoring and logging for the AI Hub components?
   * How will you capture and analyze usage patterns, performance metrics, and security events?
   * What dashboards and alerting mechanisms will you implement for different stakeholders (IT operations, security teams, business units)?

7. **AI Orchestration Logic:**
   * How will you improve upon the orchestration approach used in the RAG chatbot implementation for a multi-workload environment?
   * What Azure compute service(s) could host orchestration logic securely within the private network?
   * How will you standardize development and deployment practices for AI workloads across the organization?

8. **Governance and Cost Management:**
   * How will you implement centralized governance for AI models and prompts used across different departments?
   * What mechanisms will you create for tracking and allocating costs to different business units?
   * What policies will you enforce for security, compliance, and resource optimization?

**Success Criteria:**
By the end of this step, participants should be able to:
- Present a high-level Azure architecture diagram for the AI Hub showing all key components.
- Explain how the design builds upon and improves the approach used in the RAG chatbot implementation.
- Identify and justify the selection of key Azure services and architectural patterns for the AI Hub.
- Demonstrate how the design addresses the scalability needs for supporting multiple AI workloads.
- Provide a rationale for design decisions, referencing IFS's business objectives and regulatory needs.