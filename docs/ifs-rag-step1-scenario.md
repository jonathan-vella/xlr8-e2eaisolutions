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
2.  Securely access a curated set of internal documents which will be indexed and and made available via an Azure AI Search instance.
3.  Use an approved Azure OpenAI model to generate relevant, grounded answers based on the retrieved documents.
4.  Present the answers through a simple, intuitive web interface.
5.  Adhere strictly to IFS's security and compliance standards, running entirely within their private Azure network.
6.  Be maintainable and deployable using modern DevOps practices (including IaC).

**Activity:** Discuss the core functional components required to fulfill this scenario. What are the high-level inputs, processes, and outputs?

---

**Success Criteria:**
By the end of this step, participants should be able to:
- Identify and list the primary input (user query) and output (generated answer) of the "IFS Knowledge Assistant".
- Describe the core processing steps involved: retrieving relevant documents, augmenting the prompt, and generating the response using an LLM.
- List **at least three** distinct functional components needed (e.g., User Interface, Orchestration Logic, Document Search, AI Model Interaction).
- Acknowledge any key constraints mentioned in the scenario, for example the use of existing Azure AI Search and the requirement for private network operation.

---