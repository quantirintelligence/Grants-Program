# Polymesh Association Grant Proposal

- **Project Name:** Quantir Risk Intelligence for Polymesh Tokenized Assets and Settlement Workflows
- **Team Name:** Quantir Team
- **Level:** 2

## Project Overview :page_facing_up:

### Overview

**Project Name:** Quantir Risk Intelligence for Polymesh Tokenized Assets and Settlement Workflows

Quantir is a DeFi and on-chain risk intelligence platform that continuously collects protocol, market, and transaction activity, computes normalized risk signals, detects abnormal behavior, and delivers machine-readable alerts with human-readable explanations through API and WebSocket interfaces.

For Polymesh, we propose to build an open-source Polymesh-specific monitoring module focused on tokenized assets, settlement workflows, compliance-related activity, governance events, staking/operator conditions, and abnormal network behavior. The goal is to provide ecosystem builders and operators with structured, explainable risk signals rather than raw event streams only.

This project relates to Polymesh because Polymesh is purpose-built for regulated assets, identity, compliance, confidentiality, governance, and settlement. These workflows require strong monitoring, traceability, auditability, and early warning around operational or behavioral anomalies. Quantir can help convert Polymesh activity into integration-ready risk intelligence for dashboards, issuers, service providers, and ecosystem operators.

Our team is interested in this project because Polymesh represents a strong use case for risk intelligence beyond generic DeFi. Tokenized assets and regulated on-chain workflows need clear, explainable monitoring infrastructure. We believe Quantir's existing risk engine can be adapted into useful open-source tooling for the Polymesh ecosystem.

### Project Details

The proposed project will deliver a Polymesh-specific risk monitoring module with the following components:

- Polymesh entity and signal mapping for assets, settlement, compliance-related activity, governance, staking, and operator/network events.
- Data collection using Polymesh SDK and public Polymesh data sources where applicable.
- Event normalization into structured monitoring entities.
- Risk signal taxonomy for tokenized asset workflows and regulated on-chain operations.
- Explainable alert categories for abnormal activity.
- API-compatible and WebSocket-compatible alert payload schemas.
- Open-source documentation, examples, tests, and Docker setup.

The system will produce structured alert objects such as:

```json
{
  "id": "polymesh_alert_001",
  "timestamp": "2026-05-20T00:00:00Z",
  "network": "polymesh",
  "entity_type": "asset",
  "entity_id": "example_asset_id",
  "category": "settlement_anomaly",
  "severity": "medium",
  "risk_score": 64,
  "risk_score_delta": 9,
  "summary": "Settlement activity changed materially compared with recent baseline.",
  "reasons": [
    "unusual settlement frequency",
    "change in participant pattern",
    "increased operational concentration"
  ],
  "evidence": {
    "events": [],
    "accounts": [],
    "asset_ids": [],
    "settlement_ids": []
  },
  "explanation": {
    "text": "The alert was triggered because settlement behavior deviated from the recent activity baseline and showed increased concentration among monitored participants.",
    "key_factors": [
      "settlement activity change",
      "participant concentration",
      "risk score increase"
    ]
  }
}
```

Technology stack:

- Node.js / TypeScript for Polymesh adapters and service logic.
- Polymesh SDK for network interaction where applicable.
- MongoDB or local JSON persistence for development and test datasets.
- Redis Streams-compatible alert pipeline design where applicable.
- API/WebSocket-compatible JSON schemas.
- Docker for local testing and reproducible delivery.
- Markdown documentation and example integration guides.

The project will not provide or implement:

- No custody, trading, brokerage, or investment functionality.
- No regulated financial advice.
- No issuance of tokenized securities.
- No changes to Polymesh runtime or consensus.
- No guarantee that alerts prevent incidents or losses.
- No closed-source dependency for the grant-funded Polymesh-specific functionality.

### Ecosystem Fit

This project fits into the Polymesh ecosystem as monitoring and risk-intelligence infrastructure for tokenized assets, settlement workflows, governance, staking, and regulated on-chain operations.

Target users:

- Polymesh ecosystem builders.
- Issuers and tokenization platforms.
- Dashboard and explorer developers.
- Infrastructure operators.
- Governance and treasury participants.
- Service providers building monitoring or compliance workflows.
- Internal risk and operations teams using Polymesh data.

The project meets the need for structured monitoring around regulated asset workflows. Polymesh already provides native identity, compliance, settlement, governance, and asset functionality. Quantir would add an interpretation layer that helps users understand when activity changes, why it may matter, and how it can be consumed by external systems.

We are not aware of a directly equivalent open-source Polymesh-specific risk intelligence layer that combines monitoring, normalized scoring, explainable alerts, and API/WebSocket-compatible outputs. Similar projects exist in broader DeFi ecosystems, but they usually focus on liquidity protocols, lending markets, or price dashboards rather than regulated asset workflows and Polymesh-specific primitives.

## Team :busts_in_silhouette:

### Team members

- Team leader: Ilya Berdar — Senior Blockchain Developer
- Team member: Andriy Boichuk — Senior Software Developer
- Team member: Alex Grishenko — Senior Software Developer

### Contact

- **Contact Name:** Ilya Berdar
- **Contact Email:** founder@quantirintelligence.com
- **Website:** https://landing.quantirintelligence.com/

### Legal Structure

- **Registered Address:** Kyiv, Ukraine
- **Registered Legal Entity:** Quantir Team

### Team's experience

Quantir is built by a three-person technical team based in Kyiv, Ukraine. The team has already built a working multi-service DeFi risk monitoring stack with live collectors, transaction monitoring, normalized risk scoring, alert delivery, explanation services, API/WebSocket interfaces, deployed infrastructure, and a working dashboard.

Ilya Berdar is responsible for blockchain architecture, protocol integrations, smart contract analysis, and technical direction.

Andriy Boichuk is responsible for backend services, infrastructure, data processing, service reliability, and deployment workflows.

Alex Grishenko is responsible for service integration, data workflows, dashboard-facing systems, and product implementation.

Relevant prior work includes the Quantir risk engine, which already contains components for on-chain data ingestion, protocol snapshots, transaction event monitoring, alert routing, explanation generation, forecasting, API delivery, and dashboard support.

No previous Polymesh grant has been received by the team.

### Team Code Repos

- https://github.com/quantirintelligence
- https://github.com/quantirintelligence/quantir-risk-engine

### Team LinkedIn Profiles (if available)

Ilya Berdar https://www.linkedin.com/in/ilya-berdar-6063a11b6/
Andriy Boichuk https://www.linkedin.com/in/andriy-boichuk-519291b/
Alex Grishenko https://www.linkedin.com/in/alex-grishenko-66167b62/

## Development Status :open_book:

Quantir already has a working risk monitoring foundation. The existing repository includes a multi-service architecture for on-chain data collection, protocol snapshots, transaction monitoring, risk scoring, alert delivery, explanation services, forecasting components, API surfaces, WebSocket delivery, and dashboard-facing outputs.

Existing repository:

- https://github.com/quantirintelligence/quantir-risk-engine

Existing platform links:

- https://landing.quantirintelligence.com/
- https://app.quantirintelligence.com/

Current Quantir progress includes:

- Working dashboard.
- Live collectors.
- Transaction monitoring pipeline.
- Risk scoring loop.
- Alert system.
- Explanation system.
- API and WebSocket delivery.
- Deployed infrastructure.
- Support for 11 protocols across 3 chains.

The Polymesh-specific work has not been implemented yet. This grant would fund a focused open-source integration that adapts Quantir's monitoring approach to Polymesh-native concepts such as assets, settlement, compliance-related events, governance, staking, and operator/network activity.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):** 2 FTE average
- **Total Costs:** 30,000 USD

### Milestone 1 — Polymesh Signal Mapping and Technical Design

- **Estimated duration:** 1 month
- **FTE:** 2
- **Costs:** 8,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 or MIT for all grant-funded Polymesh-specific code. |
| 0b. | Documentation | We will provide architecture documentation explaining the Polymesh monitoring scope, supported entities, event categories, risk taxonomy, and data flow. |
| 0c. | Testing Guide | We will provide an initial testing guide describing how to validate schemas, sample payloads, and development setup. |
| 0d. | Docker | We will provide an initial Dockerfile or Docker Compose setup for local development and validation where applicable. |
| 1. | Polymesh entity mapping | We will map the initial Polymesh entities to monitor, including assets, settlement instructions where available, governance events, staking/operator-related activity, and selected network signals. |
| 2. | Risk taxonomy | We will define initial alert categories such as settlement anomaly, asset activity anomaly, governance event warning, staking/operator activity change, and compliance-related signal change. |
| 3. | Data model | We will define JSON schemas for normalized events, risk signals, alert payloads, and explanation objects. |
| 4. | Technical architecture | We will document how the Polymesh adapter will interact with Polymesh SDK or public data sources, how events are normalized, and how alerts are produced. |

### Milestone 2 — Polymesh Monitoring Adapter and Risk Signal Prototype

- **Estimated duration:** 1 month
- **FTE:** 2
- **Costs:** 12,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 or MIT for all grant-funded Polymesh-specific code. |
| 0b. | Documentation | We will provide inline documentation and developer documentation explaining how to run the adapter and generate sample alerts. |
| 0c. | Testing Guide | We will provide unit and integration test instructions for the adapter, event normalization, and alert generation logic. |
| 0d. | Docker | We will provide Docker configuration for running the prototype locally. |
| 1. | Polymesh adapter prototype | We will implement a TypeScript adapter that can collect or process selected Polymesh-related data using Polymesh SDK and/or public data sources. |
| 2. | Event normalization | We will normalize collected Polymesh activity into a structured internal event format suitable for monitoring and alert generation. |
| 3. | Initial risk scoring | We will implement simple normalized scoring logic for the first alert categories. The scoring will focus on relative changes and abnormal activity patterns, not financial advice. |
| 4. | Alert generation | We will generate structured alert payloads with severity, risk score, score delta, reasons, evidence fields, and human-readable explanation text. |
| 5. | Sample dataset and examples | We will provide sample events and generated alert examples so reviewers can test the functionality without requiring production access. |

### Milestone 3 — API Outputs, Validation, Documentation, and Release

- **Estimated duration:** 1 month
- **FTE:** 2
- **Costs:** 10,000 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 or MIT for all grant-funded Polymesh-specific code. |
| 0b. | Documentation | We will provide final documentation, API schema documentation, setup instructions, and an integration guide for developers. |
| 0c. | Testing Guide | We will provide a final test guide covering setup, sample data, adapter execution, alert generation, and output validation. |
| 0d. | Docker | We will provide final Docker configuration for testing the delivered software. |
| 0e. | Article | We will publish a short article or technical walkthrough explaining the Polymesh risk monitoring module, what was built, and how developers can use it. |
| 1. | API-compatible alert outputs | We will expose alert payload formats that can be consumed by dashboards, bots, monitoring systems, or future API/WebSocket services. |
| 2. | Reference integration example | We will provide a small example showing how a developer can consume generated Polymesh risk alerts. |
| 3. | Validation cases | We will provide validation examples showing how selected sample events produce corresponding risk signals and explanations. |
| 4. | Final open-source release | We will prepare the repository for review with clean documentation, examples, tests, and delivery notes. |

## Future Plans

After completion of the grant, Quantir plans to maintain the Polymesh-specific integration as an open-source module. We intend to improve the adapter based on feedback from Polymesh developers and ecosystem participants, add more monitored entities over time, and keep the documentation useful for external builders.

In the short term, the project can support dashboards, monitoring tools, and developer experiments around Polymesh assets, settlement, governance, and network activity.

In the long term, this work can become part of a broader risk intelligence layer for tokenized assets and regulated on-chain workflows. Potential future extensions include deeper Polymesh Private support, more advanced risk modeling, richer alert delivery, dashboard integration, and enterprise monitoring workflows for issuers or service providers building on Polymesh.

## Additional Information :heavy_plus_sign:

**How did you hear about the Grants Program?** Polymesh Website and GitHub Grants Program repository.

Quantir's differentiator is that it combines monitoring, scoring, explainability, and alert delivery in one workflow. It does not only show charts or raw events; it translates protocol behavior into actionable, interpretable, machine-readable outputs.

The Polymesh-specific grant deliverables will be open source and independently reviewable. Quantir's broader platform may remain separate, but the grant-funded Polymesh adapter, schemas, examples, tests, Docker setup, and documentation will be public.

Additional links:

- Quantir landing page: https://landing.quantirintelligence.com/
- Quantir app: https://app.quantirintelligence.com/
- Quantir GitHub: https://github.com/quantirintelligence/quantir-risk-engine

