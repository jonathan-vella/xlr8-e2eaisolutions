---
layout: default
title: Step 2 - Define Requirements
parent: AI Foundation & Hub Challenge
nav_order: 2
---

## Step 2: Define High-Level Requirements (45 minutes)

**Activity:** Based on the customer story and the goals of building a foundation for secure AI adoption, define the key business and technical requirements. Focus on *what* needs to be achieved, not *how*.

**Outcome:** Document requirements covering the following areas:

* **Foundation & Governance:**
    * Requirement: Establish standardized environments for different workload types (e.g., core infrastructure, applications, data analytics, AI)
    * Requirement: Implement centralized management and consistent governance policies across all cloud resources
    * Requirement: Ensure clear separation of duties and environments for platform operations vs. application development
    * Requirement: Provide robust identity and access management integrated with existing enterprise systems
* **Security & Compliance:**
    * Requirement: Enforce stringent security controls to meet financial industry regulations (PCI DSS, GDPR, etc.) and protect sensitive customer data
    * Requirement: Ensure all network traffic between critical components is private and isolated from public exposure
    * Requirement: Implement comprehensive monitoring for security threats and compliance deviations
    * Requirement: Adhere to data sovereignty and residency requirements
* **Connectivity:**
    * Requirement: Enable secure and reliable connectivity between on-premises data centers and Azure environments
    * Requirement: Segment network traffic effectively between different environments and workloads
* **AI Service Enablement:**
    * Requirement: Provide a controlled, centralized mechanism for discovering, accessing, and managing approved AI services
    * Requirement: Ensure AI services can be accessed securely by internal applications without direct exposure to external networks
    * Requirement: Implement governance for AI model lifecycle management (deployment, versioning, monitoring)
    * Requirement: Track and potentially charge back the usage of shared AI services to different business units
* **Scalability & Operations:**
    * Requirement: The architecture must scale to accommodate significant growth in data volume, users, and AI workload complexity
    * Requirement: Optimize for operational efficiency, potentially through automation and standardized deployment patterns
    * Requirement: Achieve target levels for reliability and disaster recovery for critical systems