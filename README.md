# Vinod Patil

**Lead Data & AI Engineer** · Azure · .NET · Microsoft Fabric

20 years building enterprise production systems on the Microsoft stack — 15 of them on Azure — for regulated environments where compliance is not optional. Now working at the boundary where AI features have to reach production **safely**: deterministic guardrails, auditability, and honest scoping.

📍 Based in Germany · **permanent residence (Niederlassungserlaubnis)** — unrestricted employment and self-employment, no sponsorship required
🌐 English-speaking teams · remote-first, open to hybrid

---

## Building in public

I publish reference architectures with the design reasoning and the evaluation kept in the open — not just working code, but the decisions behind it and the evidence that it works. Both repos label what is built versus what production would additionally require.

### [`ai-business-analyst-agent`](https://github.com/vinodrpatil-datafusion/ai-business-analyst-agent)

*.NET 8 · Azure Functions · Azure OpenAI · React* — a serverless pipeline turning business data into executive insight, on a **deterministic-before-probabilistic** design: statistics and anomalies are computed in C#, and the model narrates a bounded, pre-computed summary. **Raw rows never reach the LLM.**

- **Secretless end to end** — user-assigned managed identity for OpenAI, Blob and SQL; user-delegation SAS for uploads, so no account key exists anywhere in the path
- **Prompt-injection mitigation** — user-derived strings sanitised and fenced as untrusted data, with a fence-breakout regression test
- **Append-only audit trail** — every attempt persists its signals, the exact summary the model saw, the raw response, the prompt version and token counts
- **Production-shaped reliability** — atomic job-state transitions, idempotent triggers, lease-based recovery of crash-orphaned jobs, retry caps, adaptive token budgeting
- **Tests gate deployment** — xUnit over the deterministic core; GitHub Actions runs them on every push and deploys only if they pass, via OIDC federated identity with no deployment secrets

### [`fabric-pe-vc-analytics`](https://github.com/vinodrpatil-datafusion/fabric-pe-vc-analytics)

*Microsoft Fabric · Delta Lake · DirectLake · Azure AI Foundry* — a medallion reference architecture for private-equity / venture-capital analytics, built and validated end to end on a live Fabric tenant.

- **Bitemporal conformed layer** — `effective_date` versus `ingestion_date`, Type-2 SCD for restatements, so "as-of" queries are first-class
- **Reconciliation that surfaces conflicts** rather than silently picking winners — scored 1.000/1.000 against a synthetic conflict oracle
- **Gold star schema → DirectLake semantic model → Power BI**, with a published measure contract covering definitions, valid grain and caveats
- **AI layer** — route-then-invoke fusion agent over an Azure AI Foundry vector store and function-calling retrieval against the semantic model, with an **oracle-based** evaluation harness rather than LLM-as-judge (structured leg 6/6 grounded; document leg 4/6, with citation-accuracy and annotation coverage reported separately)
- **17 numbered design decisions** (DD-01 → DD-17), including decisions that were later revised, with the revision reasoning kept

> Portfolio-scale build on a trial tenant against a synthetic corpus — not client work, and labelled as such throughout.

---

## Core stack

| | |
|---|---|
| **Platform & .NET** | .NET / C# · Azure Functions · Service Bus · AKS · Service Fabric · event-driven microservices |
| **Azure Data & Fabric** | Microsoft Fabric (DP-700) · Data Factory · OneLake / ADLS · Delta Lake · DirectLake · Power BI |
| **AI Engineering** | Azure OpenAI · Azure AI Foundry (RAG, vector stores) · function-calling and tool routing · RAG evaluation — groundedness, citation-accuracy |
| **Security & Governance** | Managed Identity · least-privilege RBAC · Key Vault · Private Endpoints · prompt-injection mitigation · model-input audit trails |
| **IaC & DevOps** | Terraform · ARM · Azure DevOps · GitHub Actions · PowerShell |

## Background

Two decades across regulated financial services and enterprise clients — private equity and investment management, alternative investments, global custody, energy-trading compliance and MAR trade surveillance, SWIFT payment integration, and connected-vehicle telemetry. SQL and relational modelling since 2006; 15 years on Azure across event-driven, serverless and microservices systems.

**Certifications:** DP-700 (Fabric Data Engineer Associate) · MCSE: Cloud Platform & Infrastructure · MCSD: Azure Solutions Architect

## Open to work

Contract or senior permanent, remote-first — **Azure and .NET platform engineering, data platform, and applied AI**. Regulated financial services is where I have the deepest domain context, but the stack matters more than the sector.

[LinkedIn](https://www.linkedin.com/in/vinodrpatil/) · vinodrpatil@outlook.com
