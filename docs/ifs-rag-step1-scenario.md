---
layout: default
title: Step 1 - Define the Scenario
parent: RAG Chatbot Challenge
nav_order: 1
---

## Step 1: Define the Workload Scenario (15 minutes)

**Scenario:**
Innovate Financial Services (IFS) wants to empower its employees by providing quick and accurate answers to questions about internal policies, procedures, and market analysis reports. They have decided to build an internal web-based chatbot, the "IFS Knowledge Assistant". This application needs to:

1.  Understand employee questions asked in natural language.
2.  Securely access a curated set of internal documents (already indexed and available via an Azure AI Search instance managed by the platform team).
3.  Use an approved Azure OpenAI model (available via the central AI Hub) to generate relevant, grounded answers based on the retrieved documents.
4.  Present the answers through a simple, intuitive web interface.
5.  Adhere strictly to IFS's security and compliance standards, running entirely within their private Azure network.
6.  Be maintainable and deployable using modern DevOps practices (including IaC).

**Activity:** Discuss the core functional components required to fulfill this scenario. What are the high-level inputs, processes, and outputs?