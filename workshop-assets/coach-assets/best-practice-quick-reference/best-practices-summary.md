<!-- 
  This file provides a concise, bullet-point summary of Azure AI best practices across key domains such as DevOps, security, cost management, governance, networking, and operations. 
  It is intended as a quick reference for teams designing, deploying, and managing Azure AI workloads.
-->

# Azure AI Best Practices Summary

## DevOps
- Implement CI/CD pipelines to automate deployments and ensure consistent, repeatable releases.
- Leverage Infrastructure as Code (IaC) tools such as Azure Bicep, ARM Templates, or Terraform to manage your Azure AI Landing Zone.
- Include unit tests for both infrastructure and application code as part of your build process to maintain quality.
- Use declarative IaC to maintain your environments and enable rapid, reliable changes.

## Data Classification
- Establish a version control process for grounding data, especially in Retrieval-Augmented Generation (RAG) scenarios.
- Ensure all data ingested into AI models is classified and vetted according to centralized standards.
- Use unified data catalog and classification tools like Microsoft Purview to maintain consistency and compliance.
- Apply content filtering systems, such as Azure AI Content Safety, to detect and prevent the use of sensitive or copyrighted material in AI workloads.

## Cost Management
- Monitor and optimize resource usage by configuring 'Actual' and 'Forecasted' budget alerts.
- Select cost-effective models and deployment types, and allocate provisioning quotas for each model based on expected workloads.
- Use prompt compression tools (e.g., LLMLingua, gprtrim) and batching to reduce costs.
- Set maximum token limits, evaluate billing models (PAYG vs PTU), and enforce policies for automatic shutdown of unused resources.
- Remove unused fine-tuned models to avoid ongoing hosting fees, and use cost tracking systems to inform model and prompt choices.

## Security
- Encrypt data at rest and in transit using Azure's built-in encryption features and enforce RBAC for access control.
- Use managed identities instead of API keys for authentication.
- Store and manage keys securely in Azure Key Vault, and regularly rotate and expire keys.
- Follow secure coding practices to prevent vulnerabilities, enable diagnostic logging, and adhere to the Azure Security Baseline for AI services.
- Conduct regular security audits and penetration testing, and implement strong authentication mechanisms such as multi-factor authentication.

## Monitoring
- Enable comprehensive monitoring and logging for all AI workloads.
- Set up alerts for anomalies and use Azure Monitor to track KPIs and resource health.
- Proactively identify and address performance bottlenecks, and ensure diagnostic logs are enabled for troubleshooting and performance analysis.
- Use tools like Defender for Cloud to discover AI workloads and explore risks, and implement a monitoring system to ensure alignment with business KPIs.

## BCDR (Business Continuity & Disaster Recovery)
- Deploy AI workloads across multiple regions to ensure high availability and resiliency.
- Implement failover and retry policies, and regularly back up critical data using Azure's backup and disaster recovery services.
- Use multi-region API gateways (e.g., APIM + Azure Front Door) for high availability and disaster recovery, and ensure adequate quotas for resiliency.
- Deploy separate fine-tuned models across regions if finetuning is employed, and ensure your AI search service tiers have an SLA.

## Risk Mitigation
- Maintain a detailed and up-to-date inventory of your AI workload resources.
- Regularly evaluate risks using frameworks like MITRE ATLAS, OWASP Machine Learning risk, and OWASP Generative AI risk.
- Conduct red-team testing against generative and non-generative models to assess vulnerabilities.
- Develop and maintain incident response plans, enforce customer-managed keys for data at rest, and provide AI-focused employee training and awareness.

## Access Management & Authentication
- Eliminate static API keys in favor of Microsoft Entra ID for authentication.
- Enforce multi-factor authentication and use Azure RBAC to manage data plane access to resources.
- Periodically review entitlements using Entra ID PIM access reviews, and require clients to authenticate using Entra ID when accessing AI model endpoints.
- Disable key-based access where possible to enforce minimum privilege and granular control.

## Networking
- Isolate AI resources within VNets to enhance security and control traffic flow.
- Use private endpoints to connect securely to AI services, reducing exposure to the public internet.
- Restrict network access to only approved outbound modes, and deploy API gateways for load balancing, rate limiting, and secure connectivity.
- Configure data loss prevention for Azure AI services and limit outbound traffic from AI resources.

## Data Protection & Privacy
- Implement encryption for data at rest and in transit, and use RBAC to restrict access to sensitive data.
- Ensure compliance with regulations like GDPR and HIPAA by implementing privacy controls and obtaining necessary consents.
- Establish data retention and disposal policies, and use masking or redaction techniques for sensitive data in non-production environments.
- Classify data and sensitivity before generating embeddings, and treat embeddings with the same sensitivity as the source data.

## Operations
- Use dynamic sessions in Azure Container Apps to ensure each code execution occurs in a fresh, isolated environment.
- Set resource limits (CPU, memory, disk usage) for code execution environments to prevent excessive resource consumption.
- Implement a monitoring system to ensure AI workloads remain aligned with KPIs, and proactively identify performance bottlenecks and anomalies.
- Standardize compute management, enable resource locks, and automate model promotion and retraining based on performance or business needs.

---

*This summary distills the best practices from the AI Landing Zone checklist and Microsoft’s official Azure OpenAI best practices. For detailed recommendations and implementation guidance, refer to the categorized markdown files and Microsoft documentation links provided in this repository.*
