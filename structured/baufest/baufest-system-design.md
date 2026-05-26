---
metadata:
  company: Baufest
  document_type: system-design
  source_of_truth: baufest-rawdata.md
  created_at: 2026-05-25T23:45:00Z
  updated_at: 2026-05-25T23:45:00Z
  created_by: Career Database Structurer GPT
  last_updated_by: Career Database Structurer GPT
  status: active
  version: 1.0
  review_status: draft
---
# Baufest — System Design

# Business Purpose

Baufest initiatives focused on two primary domains:

## Fintech / Digital Wallet

Enable secure digital financial transactions through a wallet platform supporting:

- digital onboarding
- authentication
- biometric identity verification
- remittances
- money movement
- CBDC-related operations

## Innovation / AI Platforms

Evaluate and design scalable architectures for:

- enterprise LLM chat platforms
- retrieval-augmented conversational systems
- embeddings-based document search
- micro frontend architecture

# Architecture Overview

## Lynk Jamaica

Typical backend architecture:

Client Applications → API Layer → Microservices → Databases / External Providers

Integrated with:

- Auth0
- OnFido
- banking systems
- asynchronous event streams

Core architectural characteristics:

- microservices
- REST APIs
- event-driven communication
- webhook-driven integrations
- distributed backend orchestration

---

## Innovation Lab AI Platform

Typical architecture:

User Interface → API Layer → Prompt Orchestration → Embeddings Retrieval → LLM Provider → Response Generation

Core components included:

- document ingestion pipeline
- embeddings generation
- semantic retrieval
- LLM prompt orchestration
- response benchmarking layer

# Core Components

## Fintech Platform

- Wallet Services
- Authentication Services
- Identity Verification Services
- Webhook Consumers
- Remittance Processing Services
- Event Publishing / Consumption Layer

## AI Platform

- Prompt Evaluation Layer
- Model Benchmarking Layer
- Knowledge Processing Pipeline
- Embeddings Index
- Semantic Search Layer
- LLM Integration Layer

# Communication Patterns

- synchronous REST APIs between services
- asynchronous communication via Kafka
- webhook-based external callback processing
- provider-driven event notifications
- internal backend event propagation

# Data Flow

## Digital Wallet

User Registration → Authentication → Identity Verification → Verification Callback → Wallet Activation → Transaction Processing

## AI Platform

Document Ingestion → Embedding Generation → Indexing → Semantic Retrieval → Prompt Composition → LLM Response Generation → Evaluation

# Scalability & Concurrency

Key design considerations:

- distributed service coordination
- async callback handling
- event-driven decoupling
- external provider reliability
- secure financial transaction consistency
- scalable retrieval of contextual AI knowledge

# Reliability Strategy

- provider callback validation
- state synchronization between external identity providers and internal services
- asynchronous retry-safe workflows
- event-driven coordination
- deployment validation
- production monitoring

# Security

- secure authentication with Auth0
- identity verification with OnFido
- protected token-based communication
- secure handling of customer verification lifecycle
- compliance-sensitive financial data processing

# Design Decisions & Tradeoffs

## Event-Driven Wallet Architecture

Decision:
Use asynchronous event-driven communication across wallet services.

Tradeoffs:

Pros:
- service decoupling
- better scalability
- async processing support

Cons:
- increased coordination complexity
- eventual consistency handling

---

## Webhook-Based Identity Verification

Decision:
Integrate external identity providers through webhook callbacks.

Tradeoffs:

Pros:
- near real-time verification updates
- strong integration flexibility

Cons:
- callback timing variability
- synchronization complexity

---

## Embeddings-Based Retrieval for AI Platform

Decision:
Use embeddings and semantic search for contextual AI responses.

Tradeoffs:

Pros:
- better contextual relevance
- improved answer grounding

Cons:
- additional ingestion complexity
- evaluation and benchmarking overhead

# Operational Concerns

- deployment validation
- provider availability dependency
- callback reliability
- runtime monitoring
- production troubleshooting
- AI response quality benchmarking
- experimentation repeatability

# Testing Strategy

- backend API testing
- webhook validation testing
- integration testing with external providers
- event-driven workflow validation
- prompt benchmarking
- model comparison testing
- architecture prototyping

# Technologies Used

Java, Spring Boot, Python, Kafka, PostgreSQL, Auth0, OnFido, Azure AI, OpenAI APIs, Angular