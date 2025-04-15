# Workshop: Designing an End-to-End Azure AI Solution

**Version:** 1.0  
**Date:** 2025-04-15

![IFS Logo](./media/images/ifs.png)

## Overview

This workshop guides participants through the end-to-end process of designing a secure, scalable, and governed AI solution on Microsoft Azure, aligning with the Microsoft Cloud Adoption Framework (CAF) and Azure Well-Architected Framework (WAF) principles.

The workshop begins with a realistic customer scenario (Innovate Financial Services - IFS). Participants will first design the foundational Azure platform using Azure Landing Zones concepts, including a specialized AI Hub for governed access to AI services. Subsequently, they will design a specific AI workload – an internal RAG (Retrieval-Augmented Generation) chatbot – that leverages this platform foundation.

**Goal:** To equip participants with the knowledge and design patterns necessary to architect robust enterprise AI solutions on Azure, from the underlying platform infrastructure to the specific AI application components.

## Workshop Flow

```mermaid
%% AI Adoption Journey - The "Like a Boss" version
graph LR
    %% Phase 01: Define AI Strategy with starting glyph
    P1[🚀 Phase 01: Define AI Strategy]
    P1a[Motivations]
    P1b[Mission]
    P1c[Objectives]
    
    %% Phase 02: Design AI platform
    P2[Phase 02: Design AI platform]
    P2a[Identity & Access Mgmt]
    P2b[Resource Organization]
    P2c[Networking]
    P2d[Management & Monitoring]
    P2e[Security & Compliance]
    
    %% Phase 03: Design AI workload
    P3w[Phase 03: Design AI workload]
    P3w1[Use Cases]
    P3w2[Prompt Flow]
    P3w3[Components]
    P3w4[Well-Architected Considerations]
    
    %% Phase 03: Design AI environment
    P3e[Phase 03: Design AI environment]
    P3e1[Subscription Setup]
    P3e2[Networking]
    P3e3[AI Model Governance]
    P3e4[Data Governance]
    P3e5[Management & Monitoring]
    P3e6[Security & Compliance]
    
    %% Phase 03: AI Workload Landing Zone Integration Phase
    P3l[Phase 03: AI Workload Landing Zone Integration Phase]
    
    %% Phase 04: End-to-End Review & Justification
    P4[Phase 04: End-to-End Review & Justification]
    
    %% Phase 05: Beer o'clock with beer glyph
    P5[🍺 Phase 05: Beer o'clock]

    %% Link sections within each phase
    P1 --> P1a
    P1 --> P1b
    P1 --> P1c

    P2 --> P2a
    P2 --> P2b
    P2 --> P2c
    P2 --> P2d
    P2 --> P2e

    P3w --> P3w1
    P3w --> P3w2
    P3w --> P3w3
    P3w --> P3w4

    P3e --> P3e1
    P3e --> P3e2
    P3e --> P3e3
    P3e --> P3e4
    P3e --> P3e5
    P3e --> P3e6

    %% Define overall sequence
    P1 --> P2
    P2 --> P3w
    P3w --> P3e
    P3e --> P3l
    P3l --> P4
    P4 --> P5
```

## Modules

### Module 1: Understanding the Business Need
#### In scope: CAF AI Strategy - Process to develop an AI strategy | AI Plan - Process to plan for AI adoption

**Objective:** Analyze the customer's (IFS) business drivers, challenges, goals, and specific AI use cases.

**Activities:**  
- Review the customer story.  
- Identify key objectives, success metrics, and initial high-level requirements.

**Materials:**  
- [Customer Story](./docs/ifs-customer-story.md)

---

### Module 2: Designing the Azure AI Platform Foundation
#### In scope: CAF: Ready, Govern, Manage, Secure | WAF: Security, Reliability, Operational Excellence

**Objective:** Design a secure, scalable, and well-governed Azure foundation using Landing Zone principles to support IFS's current needs and future AI adoption. This includes designing a central, secure "AI Hub" for managing and accessing shared AI services like Azure OpenAI and Azure AI Search.

**Activities:**  
- Define platform requirements (security, governance, connectivity, AI service management).  
- Design the Landing Zone structure (Platform & Application LZs).  
- Architect the AI Hub with private networking (Private Endpoints, secure gateway).  
- Select core platform services.

**Key Concepts:**  
- Subscription democratization.  
- Identity management.  
- Network topology (Hub-Spoke).  
- Private networking.  
- Azure Policy.  
- Azure Monitor.  
- Centralized AI service governance.

**Materials:**  
- [Platform Challenge Overview](./docs/ifs-alz-overview.md)
- [Step 1: Understand the Customer](./docs/ifs-alz-step1-customer.md)
- [Step 2: Define Requirements](./docs/ifs-alz-step2-requirements.md)
- [Step 3: Design Challenges](./docs/ifs-alz-step3-challenges.md)
- [Step 4: Present and Justify](./docs/ifs-alz-step4-present.md)
- [References](./docs/ifs-alz-references.md)

---

### Module 3: Designing the AI Workload - RAG Chatbot
#### In scope: AI Ready – Process to build AI workloads in Azure | Well Architected Framework

**Objective:** Design the specific "IFS Knowledge Assistant" RAG chatbot application, ensuring it leverages the platform foundation securely and efficiently.

**Activities:**  
- Define workload requirements.  
- Design the application architecture (UI, backend/orchestration, data sources).  
- Select appropriate Azure services for hosting components (e.g., App Service, ML Endpoints).  
- Design the RAG pipeline.  
- Implement security controls (Managed Identities, Key Vault).  
- Plan for monitoring.  
- Outline deployment strategies (IaC, CI/CD).

**Key Concepts:**  
- RAG pattern.  
- Prompt Flow.  
- Azure OpenAI.  
- Azure AI Search.  
- App Service.  
- ML Managed Online Endpoints.  
- Application Gateway.  
- VNet Integration.  
- Private Endpoints.  
- Managed Identities.  
- Application Insights.  
- IaC (Bicep).

**Materials:**  
- [RAG Chatbot Challenge Overview](./docs/ifs-rag-overview.md)
- [Step 1: Define the Scenario](./docs/ifs-rag-step1-scenario.md)
- [Step 2: Elicit Requirements](./docs/ifs-rag-step2-requirements.md)
- [Step 3: Design Architecture](./docs/ifs-rag-step3-design.md)
- [Step 4: Integration](./docs/ifs-rag-step4-integrate.md)
- [Step 5: Present and Justify](./docs/ifs-rag-step5-present.md)
- [References](./docs/ifs-rag-references.md)

---

### Module 4: End-to-End Review & Justification

**Objective:** Consolidate the platform and workload designs into a cohesive end-to-end solution.

**Activities:**  
- Present the final architecture, justifying design choices based on requirements, CAF principles, and WAF pillars.  
- Discuss potential risks and mitigation strategies.

---

## Key Principles Emphasized

- **Cloud Adoption Framework (CAF):** Applying guidance across Strategy, Plan, Ready, Adopt, Govern, Manage, and Secure phases.  
- **Well-Architected Framework (WAF):** Designing solutions considering the five pillars: Cost Optimization, Operational Excellence, Performance Efficiency, Reliability, and Security.  
- **Security:** Defense-in-depth, private networking, identity-based access control, secure secrets management.  
- **Governance:** Centralized policy enforcement, cost management, resource organization.  
- **Scalability & Reliability:** Designing for growth and resilience.  
- **Automation:** Utilizing Infrastructure as Code (IaC) and CI/CD practices.

---

## Prerequisites

- Familiarity with fundamental Azure concepts (Subscriptions, Resource Groups, Networking, PaaS services).  
- Basic understanding of AI/ML concepts (LLMs, RAG is helpful but not essential).  
- Experience with architectural design discussions.

---

## Workshop Materials

- [Workshop Home Page](./docs/index.md)
- [Scenario definition for Innovate Financial Services](./docs/ifs-customer-story.md)
- [Whiteboard Design Session guide for the Platform Foundation & AI Hub](./docs/ifs-alz-overview.md)
- [Whiteboard Design Session guide for the RAG Chatbot Workload](./docs/ifs-rag-overview.md)
- [Frequently Asked Questions](./docs/ifs-faq.md)
- Workshop presentation slides (available separately)
- IFS logo image at [media/images/ifs.png](./media/images/ifs.png)

---

## GitHub Pages Documentation

This repository is configured to be published as a documentation site using GitHub Pages with:
- Jekyll static site generator
- Just-the-Docs theme for clean navigation and documentation layout

The documentation site structure includes:
- Home page with workshop overview
- Split challenge sessions with step-by-step guides
- Navigation hierarchy for easy content exploration

---

## References

* [Microsoft Cloud Adoption Framework for Azure](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/)
* [Azure Cloud Adoption Framework - AI Scenario](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/ai/)
* [Azure OpenAI baseline Landing Zone reference architecture](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/architecture/azure-openai-baseline-landing-zone)
* [AI Hub Gateway Solution Accelerator Concept](https://github.com/Azure-Samples/ai-hub-gateway-solution-accelerator/tree/main)
* [Just-the-Docs Jekyll Theme](https://just-the-docs.github.io/just-the-docs/)