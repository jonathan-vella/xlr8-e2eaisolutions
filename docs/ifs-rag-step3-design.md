---
layout: default
title: Step 3 - Design Architecture
parent: RAG Chatbot Challenge
nav_order: 3
---

## Step 3: Design the Chat Application Architecture (1.5 hours)

**Activity:** Based on the scenario defined in Step 1 and the requirements elicited in Step 2, design the end-to-end architecture for the "IFS Knowledge Assistant". Create diagrams showing components, interactions, networking, and key Azure services. Address the questions below, ensuring your design meets all specified requirements.

**Challenge Questions:**

1.  **Component Breakdown:** Based on the functional requirements from Step 2, what are the distinct logical components of this application (e.g., frontend, backend API, orchestration logic)? What specific Azure services will you use for each component?
2.  **User Interface (UI):**
    * Which Azure service meets the requirement for hosting the web UI? Justify your choice.
    * How will this service integrate into the private network as required?
    * How will employees access the UI securely, fulfilling the private network requirement? What handles ingress traffic and potential security filtering (like WAF)? (Consider Application Gateway).
3.  **Backend Orchestration (Prompt Flow Logic):**
    * The core logic involves receiving user input, querying AI Search, constructing a prompt, calling Azure OpenAI, and returning the response, as per the functional requirements. Where would this logic (potentially developed as a Prompt Flow) be authored and tested securely within the IFS environment, adhering to operational requirements? (Reference the authoring pattern in the baseline).
    * **Hosting:** What are the primary Azure options for *hosting* this backend orchestration logic once developed, meeting the reliability and scalability requirements? Compare deploying it to:
        * Azure Machine Learning Managed Online Endpoint.
        * A self-hosted container within Azure App Service.
        * (Optional: Consider Azure Container Apps or Azure Functions).
    * **Pros & Cons:** Discuss the trade-offs of each hosting option regarding management overhead, scalability, cost, network integration complexity (meeting private network requirements), and the deployment process (meeting operational requirements).
    * **Chosen Option Design:** For your recommended hosting option:
        * How is it deployed (e.g., container image from ACR, ML model deployment)?
        * How does it integrate securely into the VNet, fulfilling the private network requirement?
        * How does it securely connect to dependencies (AI Search, OpenAI, Key Vault) using private networking and managed identities, fulfilling security requirements?
4.  **Data Flow & RAG:** Diagram the flow of a user request from the UI through the backend orchestration, showing interactions with Azure AI Search and Azure OpenAI, ensuring all communication adheres to the private networking requirements.
5.  **Security & Identity:**
    * How does the UI authenticate/authorize calls to the backend API?
    * How does the backend API/orchestration logic authenticate to Azure AI Search, Azure OpenAI, and Key Vault, fulfilling the Managed Identity requirement?
    * How are secrets (e.g., Key Vault URI, Search endpoint) provided securely to the application components at runtime, fulfilling the Key Vault requirement?
6.  **Networking:**
    * Illustrate how the application components (UI, Backend Hoster) reside within or integrate with the Application Landing Zone VNet, fulfilling the private network requirement.
    * Show the network paths for communication, ensuring no public endpoints are used for backend components:
        * User -> Ingress (App Gateway) -> UI Hoster
        * UI Hoster -> Backend Hoster
        * Backend Hoster -> Key Vault
        * Backend Hoster -> AI Search
        * Backend Hoster -> Azure OpenAI
    * How is DNS resolution handled for these private connections?
7.  **Monitoring & Observability:**
    * What specific metrics and logs would you capture from the UI, the backend host, and the prompt flow logic itself to meet the monitoring requirements?
    * Which Azure Monitor components (Application Insights, Log Analytics) would you use and how would they be configured for each application component?
8.  **Deployment (IaC & CI/CD):**
    * Outline the steps needed to deploy the Azure resources for this application using IaC (e.g., Bicep), fulfilling the operational requirement for automated deployment.
    * How would you package and deploy the UI code?
    * How would you package (e.g., containerize if applicable) and deploy the backend prompt flow logic to your chosen hosting option? What tools are involved (`pf` CLI, `az cli`, Docker, ACR)?

---

**Success Criteria:**
By the end of this step, participants should be able to:
- Present a clear architecture diagram illustrating:
    - All logical application components (UI, Backend/Orchestration).
    - The specific Azure services chosen for hosting each component.
    - Network integration within the Application Landing Zone VNet.
    - Network paths (using VNet Integration/Private Endpoints) between components and dependencies (Key Vault, AI Search, OpenAI).
- Justify the selection of Azure services for the UI and backend orchestration by explicitly linking them to **at least three** specific functional, security, or operational requirements identified in Step 2.
- Detail the secure integration strategy by:
    - Specifying whether VNet Integration or Private Endpoints are used for each connection.
    - Explaining the DNS configuration required for private endpoint resolution.
    - Confirming no public endpoints are exposed for backend components.
- Explain the end-to-end authentication flow, specifying the type of Managed Identity (System or User-Assigned) used for the backend component to access Key Vault, AI Search, and Azure OpenAI.
- Describe the monitoring strategy by:
    - Listing **at least two** specific metrics or log types for the UI and backend components.
    - Identifying the specific Azure Monitor tools (e.g., Application Insights, Log Analytics Workspace) used.
- Outline the deployment approach by:
    - Specifying the IaC tool (e.g., Bicep).
    - Describing the packaging method for the UI and backend logic (e.g., container image).
    - Listing the key tools involved in the CI/CD process (e.g., `pf` CLI, `az cli`, Docker, ACR, GitHub Actions/Azure DevOps).
- Demonstrate how the overall design explicitly adheres to the constraints identified in Step 1: use of Azure AI Search index and Azure OpenAI, and ensuring all components operate within the private network.

---