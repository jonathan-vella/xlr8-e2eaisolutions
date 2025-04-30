---
layout: default
title: Step 5 - Present and Justify
parent: RAG Chatbot Challenge
nav_order: 5
---

## Step 5: Present and Justify (30 minutes)

**Activity:** Prepare and deliver a concise presentation of your integrated RAG application design.

**Outcome:** Successfully present the design to stakeholders, clearly articulating the architecture, integration points, and rationale, demonstrating alignment with ALZ principles.

---

**Success Criteria:**

*   **Clear Architecture Diagram:** Present an accurate diagram showing RAG components within the entire Azure Landing Zones environment (both Platform and Application Landing Zones).
*   **Component & Hosting Rationale:** Clearly identify the chosen Azure services and hosting options (e.g., App Service, Container Apps) with justifications based on requirements and guidelines (scalability, cost, compliance, etc.).
*   **Network Integration Articulated:** Explain network integration, use of Private Endpoints, DNS Zones, ingress and egress traffic,  user to UI, etc. and how these can be enforced by using ALZ policies.
*   **Security Measures Described:** Outline the use of identities (be specific on the type of identity used), secrets management, key rotation, private traffic flow enforcement, content safety, and data protection measures.
*   **Monitoring Plan Summarized:** Briefly describe sending logs/metrics to the central Log Analytics workspace and key alert types.
*   **Deployment Strategy Outlined:** Summarize the IaC approach and CI/CD integration within ALZ, including identity type and permissions.
*   **Presentation Clarity:** Deliver the design and justifications clearly and concisely within the time limit.

---

**Note for Further Evolution:**
While this RAG chatbot implementation meets the current requirements, the team should consider what limitations this approach might have as IFS scales to multiple AI workloads across different departments. This initial implementation will provide valuable insights that can inform the creation of a more centralized AI Hub in the future.