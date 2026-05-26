---
metadata:
  company: Baufest
  document_type: interview-stories
  source_of_truth: baufest-rawdata.md
  created_at: 2026-05-25T23:45:00Z
  updated_at: 2026-05-25T23:45:00Z
  created_by: Career Database Structurer GPT
  last_updated_by: Career Database Structurer GPT
  status: active
  version: 1.0
  review_status: draft
---
# Baufest — Interview Stories

# 1. Building a Digital Wallet Platform in a Regulated Fintech Environment

## Interview Themes
Distributed systems, fintech, backend engineering, technical leadership

## Situation
Worked on Lynk Jamaica, a digital wallet platform supporting onboarding, identity verification and secure money movement.

## Problem / Risk
Financial and identity operations required strong reliability, compliance and secure orchestration across multiple external providers.

## Task
Build and maintain backend services supporting wallet operations and customer lifecycle flows.

## Constraints
- regulated fintech environment
- distributed services
- external provider dependencies
- asynchronous callback timing

## Actions
- built Spring Boot microservices
- implemented REST APIs
- designed event-driven workflows
- integrated Auth0 and OnFido
- supported production rollout and troubleshooting

## Technical Decisions
Used Kafka and webhook-based asynchronous communication to decouple services.

## Tradeoffs
Operational flexibility and scalability vs increased distributed coordination complexity.

## Result
Delivered stable wallet backend capabilities supporting secure digital financial operations.

## Key Signals
Distributed systems ownership, fintech reliability, technical leadership

## Reusable Talking Points
“How I built backend services for a regulated digital wallet platform.”

---

# 2. Identity Verification Synchronization with OnFido

## Interview Themes
Integrations, reliability engineering, problem solving

## Situation
Identity verification status needed to stay synchronized between OnFido and internal wallet services.

## Problem / Risk
Asynchronous callbacks and provider timing could create inconsistent verification states.

## Task
Design reliable backend processing for verification lifecycle updates.

## Constraints
- webhook timing variability
- provider dependency
- state synchronization requirements

## Actions
- built webhook consumers
- validated callback payloads
- orchestrated backend status propagation
- coordinated downstream workflow triggering

## Technical Decisions
Webhook-first event processing with internal propagation after validation.

## Tradeoffs
Higher orchestration complexity in exchange for reliable external integration.

## Result
Improved consistency and reliability of onboarding and verification workflows.

## Key Signals
Reliability mindset, integrations experience, backend orchestration

## Reusable Talking Points
“How I solved state synchronization challenges with third-party identity providers.”

---

# 3. Designing an Enterprise LLM-Based Chat Platform

## Interview Themes
Architecture, AI engineering, ambiguity, innovation leadership

## Situation
Baufest Innovation Lab explored enterprise use cases for LLM-powered conversational systems.

## Problem / Risk
Emerging technology with unclear architecture patterns and rapidly evolving tooling.

## Task
Design and validate a scalable technical solution.

## Constraints
- evolving ecosystem
- multiple models and prompts
- uncertain quality benchmarks

## Actions
- defined solution architecture
- led experimentation
- evaluated prompts and models
- designed retrieval strategy using embeddings
- created evaluation framework

## Technical Decisions
Use embeddings-based retrieval to improve contextual relevance of generated responses.

## Tradeoffs
Higher implementation complexity for improved answer quality and contextual grounding.

## Result
Validated architecture and created reusable AI engineering knowledge.

## Key Signals
Architecture ownership, innovation, technical strategy

## Reusable Talking Points
“How I architected and evaluated an enterprise conversational AI platform.”

---

# 4. AI Benchmarking Across Prompts and Models

## Interview Themes
Decision-making, experimentation, systems evaluation

## Situation
Needed a repeatable way to compare LLM responses and knowledge retrieval quality.

## Problem / Risk
Subjective evaluation could lead to poor architecture decisions.

## Task
Define a benchmarking strategy.

## Constraints
- non-deterministic model behavior
- multiple evaluation variables
- emerging best practices

## Actions
- defined comparison criteria
- evaluated prompts
- compared model outputs
- benchmarked processed knowledge sources

## Technical Decisions
Treat evaluation as a measurable architecture decision rather than ad-hoc experimentation.

## Tradeoffs
More upfront effort in exchange for stronger technical decision-making.

## Result
Improved confidence in model and architecture selection.

## Key Signals
Analytical thinking, architecture evaluation, experimentation rigor

## Reusable Talking Points
“How I created an evaluation framework for LLM and prompt benchmarking.”