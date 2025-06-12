---
layout: default
title: FAQ
nav_order: 8
permalink: /faq/
---

# Frequently Asked Questions (FAQ)

## General Questions

### What is the purpose of this whiteboard design session?

This session aims to guide attendees through designing a secure, scalable Azure architecture to support IFS's AI adoption journey. Attendees will address real-world business requirements, technical challenges, and strategic objectives.

### Who is IFS?

IFS (Innovate Financial Services) is a well-established global financial institution providing banking, investment, and insurance services. They specialize in financial services across multiple markets.

## Azure and AI Adoption

### Why did IFS choose Azure for their AI adoption?

IFS selected Azure due to its comprehensive AI capabilities, robust security features, scalability, and alignment with industry best practices outlined in the Microsoft Cloud Adoption Framework.

### What are the primary AI use cases identified by IFS?

- Fraud detection using AI-powered analytics.
- Personalized financial advice and recommendations.
- Risk management and assessment.
- Automated customer support and virtual assistants.

## Business Requirements

### What are the key business requirements for IFS?

- Security and compliance (PCI DSS, GDPR, local financial regulations).
- Centralized governance and management of AI services.
- Secure connectivity and integration with on-premises environments.
- Centralized AI model governance and control.
- Data security, privacy, and residency compliance.
- Operational efficiency through automation and self-service.
- Cost optimization and resource visibility.
- Scalability to support future growth.

### Why is AI model governance important for IFS?

IFS requires strict control over AI models to ensure only validated, compliant, and ethically approved models are deployed. Centralized governance helps maintain compliance, security, and ethical standards in financial services.

### How does IFS ensure data privacy?

IFS emphasizes strict adherence to data residency and sovereignty requirements, encryption of data at rest and in transit, and maintaining full organizational control over sensitive customer financial data.

## Technical Challenges

### What technical challenges will attendees address?

Attendees will design:

- A secure and scalable core cloud environment.
- Optimized workload hosting environments for diverse applications.
- A specific RAG chatbot application to meet an initial business need.
- Based on learnings from the initial workload, a centralized AI management environment with secure access, governance, and private connectivity.

### What deliverables are expected from attendees?

- High-level architecture diagrams.
- List of Azure services and their roles.
- Implementation plan including phased deployment, migration strategy, governance, and security controls.
- Risk assessment and mitigation strategies.

## Workshop Structure

### What are the main challenges in the workshop?

The workshop is structured around three main challenges in a logical progression:

1. **AI Foundations Challenge** - Design a secure, scalable, and governed Azure foundation using Landing Zone principles.

2. **RAG Chatbot Challenge** - Design an initial AI workload (a secure internal chatbot) that uses retrieval-augmented generation to provide employees with information from internal documents.

3. **AI Hub Challenge** - Based on the experience gained from implementing the initial workload, design a dedicated environment for centralized management and secure access to shared AI services for all future AI workloads.

### How do the challenges build upon each other?

The challenges follow the natural evolution of an organization's AI journey:

1. First, establishing the foundational environment (landing zones, networking, identity) to support any AI initiative.

2. Next, implementing a specific AI workload to solve a business need and gain practical experience with AI technologies.

3. Finally, expanding the environment by creating a centralized hub for AI services based on the lessons learned from the initial implementation, enabling broader adoption of AI across the organization while maintaining proper governance and security.

### What is the AI Hub challenge about?

The AI Hub challenge focuses on creating a centralized, secure environment to host shared Azure AI services and provide governed access to these services across the organization. It builds upon the learnings from the RAG chatbot implementation, addressing scaling concerns, cross-department governance, and the need for consistent security controls as the organization's AI usage expands. The AI Hub acts as the organization's centralized point for deploying, managing, and securely accessing AI services like Azure OpenAI.
