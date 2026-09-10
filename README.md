Vinod Patil

Lead Data & AI Engineer

19+ years delivering enterprise production systems on Azure and .NET — now specialising in Microsoft Fabric and Azure AI, bringing two decades of regulated-delivery discipline to data and AI engineering where compliance is non-negotiable.

Regulated financial services is the throughline: MAR trade surveillance, SWIFT payment integration, and PE/VC analytics for clients including LGT Capital Partners, BNY Mellon, and Uniper.


🔧 Building in public

I build reference architectures with the design reasoning and evaluation kept in the open — not just working code, but the decisions behind it and the evidence that it works.

fabric-pe-vc-analytics

A Microsoft Fabric medallion reference architecture for private-equity / venture-capital analytics, validated end-to-end on a live Fabric tenant.


Conformed bitemporal Delta build → Gold star schema (Lakehouse Delta, Type-2 dimensions, point-in-time joins) → DirectLake semantic model → Power BI report
AI layer: RAG over an Azure AI Foundry vector store + function-calling structured retrieval over the semantic model, composed by a route-then-invoke fusion agent — with an oracle-based evaluation harness (structured leg 6/6 grounded; document leg 5/6, with a documented citation-accuracy finding)
CI/CD promotion across dev / test / prod via Fabric deployment pipelines and Git integration
17 documented design decisions (DD-01 → DD-17) in docs/design_decisions.md



Scope: a portfolio-scale reference build on a trial tenant against a synthetic LP corpus — not delivered to a named client. What's built vs. what production additionally requires is labelled throughout.



ai-business-analyst-agent

A .NET 8 / Azure Functions insight application on a deterministic-before-probabilistic design — statistics and anomalies computed in code, Azure OpenAI narrating a bounded, pre-computed summary.


Secretless authentication end-to-end (user-assigned Managed Identity, least-privilege RBAC)
Append-only audit trail — persists the exact input the model saw, the prompt version, the raw response, and token counts per run
Two named pipeline stages, deterministic core — no orchestration loop, no multi-agent framework, by design



Scope: a portfolio project, not a production deployment.




Core stack

Azure Data & Fabric · Microsoft Fabric (DP-700) · Data Factory · OneLake / ADLS · Delta Lake · DirectLake · Power BI

AI Engineering · Azure OpenAI · Azure AI Foundry (RAG, vector store) · function-calling & tool routing · RAG evaluation (groundedness, citation-accuracy)

Platform & .NET · .NET / C# · Azure Functions · Service Bus · AKS · Service Fabric · event-driven microservices

IaC & DevOps · Terraform · ARM Templates · Azure DevOps · CI/CD · PowerShell

Security · Managed Identity · RBAC · Key Vault · Private Endpoints


Background

Two decades across regulated financial services and enterprise clients — private equity & investment management, alternative investments (BNY Mellon), energy-trading compliance (Uniper), and connected-vehicle telemetry at Microsoft. SQL and relational data modelling since 2006; twelve years on Azure across event-driven, serverless, and microservices systems.

Certifications: DP-700 (Fabric Data Engineer Associate) · MCSE: Cloud Platform & Infrastructure · MCSD: Azure Solutions Architect


Open to work

Remote Microsoft Fabric + Azure AI engagements — contract or senior permanent. Regulated financial services a particular focus.
