---
layout: default
title: Step 3 - Design Architecture
parent: RAG Chatbot Challenge
nav_order: 3
---

## Step 3: Design the Chat Application Architecture (1.5 hours)

**Activity:** Design the end-to-end architecture for the "IFS Knowledge Assistant". Create diagrams showing components, interactions, networking, and key Azure services. Address the questions below.

**Challenge Questions:**

1.  **Component Breakdown:** What are the distinct logical components of this application (e.g., frontend, backend API, orchestration logic)? What Azure services map to these components?
2.  **User Interface (UI):**
    * Which Azure service is suitable for hosting the web UI? Why?
    * How will this service be integrated into the private network?
    * How will employees access the UI securely? What handles ingress traffic and potential security filtering (like WAF)? (Consider Application Gateway).
3.  **Backend Orchestration (Prompt Flow Logic):**
    * The core logic involves receiving user input, querying AI Search, constructing a prompt, calling Azure OpenAI, and returning the response. Where would this logic (potentially developed as a Prompt Flow) be authored and tested securely within the IFS environment? (Reference the authoring pattern in the baseline).
    * **Hosting:** What are the primary Azure options for *hosting* this backend orchestration logic once developed? Compare deploying it to:
        * Azure Machine Learning Managed Online Endpoint.
        * A self-hosted container within Azure App Service.
        * (Optional: Consider Azure Container Apps or Azure Functions).
    * **Pros & Cons:** Discuss the trade-offs of each hosting option regarding management overhead, scalability, cost, network integration complexity, and deployment process.
    * **Chosen Option Design:** For your recommended hosting option:
        * How is it deployed? (e.g., container image from ACR, ML model deployment).
        * How does it integrate securely into the VNet?
        * How does it securely connect to dependencies (AI Search, OpenAI via AI Hub, Key Vault) using private networking and managed identities?
4.  **Data Flow & RAG:** Diagram the flow of a user request from the UI through the backend orchestration, showing interactions with Azure AI Search and Azure OpenAI (via the AI Hub).
5.  **Security & Identity:**
    * How does the UI authenticate/authorize calls to the backend API?
    * How does the backend API/orchestration logic authenticate to Azure AI Search, Azure OpenAI (via AI Hub), and Key Vault? Detail the use of Managed Identities.
    * How are secrets (e.g., Key Vault URI, Search endpoint) provided securely to the application components at runtime?
6.  **Networking:**
    * Illustrate how the application components (UI, Backend Hoster) reside within or integrate with the Application Landing Zone VNet.
    * Show the network paths (using private endpoints/VNet integration) for communication:
        * User -> Ingress (App Gateway) -> UI Hoster
        * UI Hoster -> Backend Hoster
        * Backend Hoster -> Key Vault
        * Backend Hoster -> AI Search (via AI Hub or direct PE)
        * Backend Hoster -> Azure OpenAI (via AI Hub PE)
    * How is DNS resolution handled for these private connections?
7.  **Monitoring & Observability:**
    * What specific metrics and logs would you capture from the UI, the backend host, and the prompt flow logic itself?
    * Which Azure Monitor components (Application Insights, Log Analytics) would you use and how would they be configured for each application component?
8.  **Deployment (IaC & CI/CD):**
    * Outline the steps needed to deploy the Azure resources for this application using IaC (e.g., Bicep).
    * How would you package and deploy the UI code?
    * How would you package (e.g., containerize if applicable) and deploy the backend prompt flow logic to your chosen hosting option? What tools are involved (`pf` CLI, `az cli`, Docker, ACR)?