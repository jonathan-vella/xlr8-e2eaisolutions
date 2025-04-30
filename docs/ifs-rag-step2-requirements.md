---
layout: default
title: Step 2 - Elicit Requirements
parent: RAG Chatbot Challenge
nav_order: 2
---

## Step 2: Elicit Workload Requirements (45 minutes)

**Activity:** Based on the scenario and the assumed context, define the specific functional and non-functional requirements for the *IFS Knowledge Assistant application itself*.

**Outcome:** Document requirements covering:

* **Functionality:**
    * Requirement: Web-based user interface for submitting questions and viewing answers.
    * Requirement: Backend logic to orchestrate the RAG process (receive query, retrieve documents from AI Search, formulate prompt, call OpenAI, process response).
    * Requirement: Utilize the centrally managed Azure AI Search index for document retrieval.
* **Security & Compliance:**
    * Requirement: All application components (UI, backend API/logic) must reside within IFS's private network.
    * Requirement: All communication between components and with dependent Azure services must use private network connections. No public endpoints for backend components.
    * Requirement: Securely manage all application secrets (e.g., connection details, API keys if needed).
    * Requirement: Implement appropriate authentication and authorization for application components using Managed Identities.
* **Operations & Deployment:**
    * Requirement: Implement comprehensive logging and monitoring for application health, performance, and usage (UI, backend, AI interactions).
    * Requirement: Define an automated deployment process for both infrastructure (using IaC like Bicep/Terraform) and application code/logic.
    * Requirement: The backend logic requires a well-defined authoring and testing process and a reliable hosting mechanism.
    * Requirement: The solution should be designed for reliability (e.g., consider zone redundancy for key components) and scalability.

---

**Success Criteria:**
By the end of this step, participants should be able to:
- List **at least two** specific functional requirements detailing *what* the application must do (e.g., "Orchestrate RAG flow", "Provide web UI").
- List **at least three** specific security requirements, explicitly mentioning:
    - Private network integration (e.g., VNet integration, Private Endpoints).
    - Secure secrets management (e.g., using Azure Key Vault).
    - Secure service-to-service authentication (e.g., using Managed Identities).
- List **at least two** specific operational requirements, covering:
    - Monitoring and logging needs.
    - Automated deployment (IaC and CI/CD).
- Ensure all requirements align with the constraints defined in Step 1 (use of central AI Search/OpenAI, private network operation).
- Present the requirements in a clearly categorized list (Functionality, Security & Compliance, Operations & Deployment).

---