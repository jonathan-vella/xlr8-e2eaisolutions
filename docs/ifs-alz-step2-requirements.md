---
layout: default
title: Step 2 - Capture the Requirements
parent: AI Foundations Challenge
nav_order: 2
---

## Step 2: Define High-Level Requirements (45 minutes)

**Activity:** Based on the customer story and the goals of building a foundation for trustworthy AI adoption, define the key business and technical requirements. Focus on *what* needs to be achieved, not *how*.

**Outcome:** Document requirements covering the following areas:

* **Foundation & Governance:**
    * How will you establish standardized environments for different workload types (e.g., core infrastructure, applications, data analytics, AI)?
    * What approach will you use to implement centralized management and consistent governance policies across all cloud resources?
    * How will you ensure clear separation of duties and environments for platform operations versus application development?
    * How will you provide robust identity and access management integrated with existing enterprise systems?

* **Security & Compliance:**
    * What security controls will you enforce to meet financial industry regulations (PCI DSS, GDPR, etc.) and protect sensitive customer data?
    * How will you ensure all network traffic between critical components is private and isolated from public exposure?
    * How will you implement comprehensive monitoring for security threats and compliance deviations?
    * How will you adhere to data sovereignty and residency requirements?

* **Connectivity:**
    * How will you enable secure and reliable connectivity between on-premises data centers and Azure environments?
    * How will you segment network traffic effectively between different environments and workloads?

* **AI Service Enablement:**
    * How will you provide a controlled, centralized mechanism for discovering, accessing, and managing approved AI services?
    * How will you ensure AI services can be accessed securely by internal applications without direct exposure to external networks?
    * How will you implement governance for AI model lifecycle management (deployment, versioning, monitoring)?
    * How will you track and potentially charge back the usage of shared AI services to different business units?

* **Scalability & Operations:**
    * How will your architecture scale to accommodate significant growth in data volume, users, and AI workload complexity?
    * How will you optimize for operational efficiency, potentially through automation and standardized deployment patterns?
    * How will you achieve target levels for reliability and disaster recovery for critical systems?

---

**Success Criteria:**  
By the end of this step, participants should be able to:
- Draft **at least two** high-level requirement questions for each of the five specified areas (Foundation & Governance, Security & Compliance, Connectivity, AI Service Enablement, Scalability & Operations).
- Categorize each requirement question accurately under its respective area.
- For **at least one** requirement question in each category, explicitly mention a specific IFS business objective (e.g., reduce fraud, improve customer satisfaction) or regulatory obligation (e.g., PCI DSS, GDPR) from the customer story.
- Present the final list of requirement questions in a **table** with columns for 'Category' and 'Requirement Question'.
- Provide a **brief written justification (1-2 sentences)** for each requirement question, explaining how it contributes to building a trustworthy, secure, and scalable Azure AI platform for IFS.

---