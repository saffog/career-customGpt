# Kroger — Raw Data

---

# Metadata

- Candidate: Alejandro Gomez Salgado
- Company: Kroger
- File Name: kroger-rawdata.md
- Created By: ChatGPT — Interviewer Career Extractor (with Alejandro Gomez Salgado)
- Created On: 2026-05-23T14:27:00-06:00
- Last Updated: 2026-05-23T15:09:00-06:00
- Time Zone: America/Mexico_City
- Language: English
- Status: Final
- Completeness: Complete (~95%)

---

# Source Materials

This file was compiled using the following sources:

- Direct interview sessions with Alejandro Gomez Salgado
- Career database notes for Kroger
- Kroger interview stories
- Kroger system design notes
- Kroger resume experience notes
- Existing English CV versions
- Technical memory recall and follow-up clarification sessions

---

# Purpose

This document is the source-of-truth knowledge base for Alejandro Gomez Salgado’s experience at Kroger.

Primary intended use:

- Resume tailoring
- Interview preparation
- STAR story generation
- System design interview preparation
- Technical leadership storytelling
- Company-specific experience recall
- Future LinkedIn or resume updates

---

# Notes

- Information is based on direct recollection and validated against existing documentation whenever possible.
- Technical descriptions prioritize accuracy while remaining interview-friendly.
- Metrics are approximate unless explicitly stated.
- This file should be updated whenever new details are remembered, corrected, or expanded.

---

# Base Information

- Company: Kroger
- Role: Senior Backend Software Engineer
- Duration:
  - Pricing Division: July 2024 – December 2025
  - Payments Division: January 2026 – May 2026
- Industry: Retail / Pricing Optimization / Payments
- Location: Remote
- Methodology: Agile / Scrum

---

# Business Context

Worked as Senior Backend Engineer supporting enterprise-scale pricing and payments platforms used across Kroger retail operations.

Main domains supported:

## Pricing
- Regular Pricing Optimization (RPO)
- Pricing hierarchy management
- configurable pricing rules
- floor/ceiling pricing validation
- regional pricing strategies
- competitor pricing comparison
- pricing execution orchestration
- scheduled pricing workflows

## Payments
- payment authorization
- item eligibility validation
- food benefit card processing
- tender validation
- payment coverage calculations
- external provider integrations

Most pricing APIs were internal-facing and configuration-driven rather than customer-facing, but pricing correctness was business-critical because changes directly impacted store operations.

Pricing workflows were commonly tied to:

- weekly pricing cycles
- promotional windows
- seasonal campaigns
- monthly pricing periods

---

# Architecture Overview

Kroger platforms commonly followed a layered service architecture:

Frontend → Interface Service → Data Service → Database

## Characteristics

- Spring Boot microservices
- REST APIs
- event-driven architecture
- Kafka producers and consumers
- JWT Bearer authorization
- Feign-based inter-service communication
- PostgreSQL / DB2 persistence
- Kubernetes deployments
- CI/CD automation

---

# Pricing Division

## Main Systems

Primary systems:

- RPO Settings
- RPO Upkeep
- Regular Pricing Rules
- Unified Pricing Engine (UPE)

Main services:

- `rpo-settings-interface`
- `rpo-settings-data`
- `regular-pricing-rules-interface`
- `regular-pricing-rules-data`

## Responsibilities

- building backend APIs
- maintaining pricing workflows
- pricing rule execution
- scheduled processing
- downstream pricing integrations
- pricing settings management
- internal pricing orchestration

---

# Unified Pricing Engine (Drools POC)

## Overview

One of the most representative initiatives during Kroger was contributing to the **Unified Pricing Engine proof of concept**, built using Drools.

Goal:

Evaluate whether Drools could support configurable pricing rules in a scalable and maintainable way while replacing legacy pricing logic with a modern rule-driven platform.

---

## Responsibilities

### Technical Learning & Prototyping
- Learned Drools from scratch.
- Built proofs of concept around:
  - rule execution lifecycle
  - spreadsheet-driven rule definitions
  - rule compilation
  - backend integration patterns

### Legacy Analysis
- analyzed legacy pricing systems
- reverse-engineered business rules
- identified pricing conditions, fields, inputs, and outputs
- transformed pricing logic into Drools-compatible execution models

### Rule Modeling
- translated pricing rules into spreadsheet-based configurations
- defined mapping between spreadsheet fields and Drools execution
- supported business-managed configurable pricing rule modeling

### Technical Collaboration
- worked closely with Tech Lead and Product Owner
- refined stories for the POC
- contributed to functional scope and technical feasibility

### Knowledge Sharing
- explained Drools concepts to developers and technical leadership
- documented architecture and rule modeling approach

### Delivery
- implemented backend stories
- participated in QA validation
- helped deliver end-to-end demo for Kroger stakeholders

---

## Outcome

- validated Drools as a viable pricing rule engine
- modernized representation of legacy pricing logic
- enabled spreadsheet-driven rule configuration
- delivered working stakeholder demo
- generated reusable technical knowledge across the team

---

# Async & Reactive Processing

Pricing workflows required scheduled and concurrent backend execution.

Implemented using:

- `CompletableFuture`
- `Spring WebFlux`
- `Flux`
- `@Scheduled`

Used for:

- pricing batch orchestration
- concurrent processing
- scheduled pricing execution
- asynchronous backend workflows
- automated rule execution

---

# Kafka Migration — Enterprise Kafka to Kafka as a Service

## Overview

Participated in Kroger’s migration from **Enterprise Kafka (EK)** to **Kafka as a Service (KaaS)**.

---

## Key Contributions

- reviewed Kafka YAML configuration structures
- analyzed mapping between internal shared library parameters and native Kafka properties
- identified duplicated configuration across shared libraries
- proposed simplification strategy with Tech Lead
- refactored shared `kafka-message-lib`
- simplified producer/consumer configuration
- improved SSL configuration handling
- improved topic routing
- standardized multi-environment configuration
- supported migration validation across teams

---

## Result

- reduced duplicated configuration
- improved maintainability
- simplified YAML setup
- improved consistency across environments
- easier adoption of KaaS migration by dependent teams

---

# National Services Decommission

## Business Context

National was a legacy pricing-related business domain with dedicated architecture:

- frontend application
- interface service
- data service
- dedicated database

Also participated in Kafka-based event workflows integrated with ETL processes and downstream consumers.

---

## Ownership

Had direct ownership of technical analysis and decommission coordination.

Responsibilities:

- mapping service dependencies
- identifying system interactions
- analyzing Kafka producers and consumers
- validating ETL-generated event dependencies
- reviewing downstream impact
- coordinating rollout planning across teams

---

## Collaboration

Worked with:

- backend engineering teams
- ETL teams
- QA
- support teams
- service owners from dependent platforms

---

## Result

- safe retirement of legacy National components
- reduced technical debt
- removed unused dependencies
- minimized operational risk during rollout

---

# Payments Division

## Main System

`payment-estimator`

Responsibilities included:

- item eligibility validation
- tender authorization
- food benefit card validation
- payment coverage calculations
- external provider integration workflows

---

## Provider Modules

- `nations-transactions`
- `solutran-transactions`

---

## Technical Contributions

- implemented provider-specific transaction processing
- validated payload contracts
- collaborated with external teams on integration verification
- supported mocked payment workflows for testing
- improved maintainability using SOLID principles

---

# Performance Optimization

## SQL Optimization

One of the strongest backend optimization contributions involved simplifying a complex SQL query used in pricing workflows.

### Actions
- analyzed existing implementation
- removed unnecessary joins and redundant logic
- preserved existing functional behavior

### Result
- reduced runtime to ~25% of original execution time
- approximately **4x performance improvement**

---

# Testing & Quality

Worked extensively with:

- JUnit
- Mockito
- WireMock
- Postman
- integration testing

---

## WireMock Integration Testing

WireMock JRE8 was heavily used for payment integrations.

Implemented:

- third-party provider emulation
- request-driven payload extraction
- dynamic JSON mock response generation
- provider-specific authorization simulation
- isolated backend validation without external dependency

Impact:

- improved testing reliability
- enabled isolated integration testing
- accelerated validation workflows for payment providers

---

# Operational & DevOps Exposure

Worked with:

- GitHub Actions
- SonarQube
- Harness
- Rancher
- Rancher Desktop
- Kubernetes logs
- Dynatrace dashboards
- deployment validation
- runtime diagnostics

---

## Observability

Created and maintained Dynatrace dashboards monitoring:

- HTTP traffic
- successful transaction rates
- 4xx error windows
- 5xx error windows
- runtime diagnostics
- backend service health

---

# Leadership & Technical Influence

Examples of senior-level ownership and technical influence:

- ownership of National decommission initiative
- ownership of Kafka shared library refactor
- mentoring team members on Drools architecture
- mentoring on Kafka integrations
- peer code reviews
- sprint refinement participation
- QA validation planning
- technical documentation
- cross-team coordination with engineering and ETL
- stakeholder-facing technical demo participation
- collaboration with tech leads on architecture decisions

---

# Technical Stack

## Languages
- Java 11
- Java 17
- SQL

## Frameworks
- Spring Boot
- Spring MVC
- Spring Data
- Spring Security
- Spring WebFlux
- JPA
- Hibernate
- Feign
- Resilience4j
- Lombok

## Rule Engine
- Drools

## Databases
- PostgreSQL
- IBM DB2
- Azure Cosmos DB

## Messaging
- Kafka
- Enterprise Kafka
- Kafka as a Service

## Testing
- JUnit
- Mockito
- WireMock
- Postman

## DevOps / Infrastructure
- Kubernetes
- Rancher
- Helm
- Harness
- GitHub Actions
- SonarQube

## Monitoring
- Dynatrace

## Documentation / Collaboration
- Jira
- Confluence
- draw.io
- Swagger / OpenAPI

---

# Strongest Technical Themes

- Java backend engineering
- Spring Boot microservices
- distributed systems
- event-driven architecture
- Kafka modernization
- configurable rule engines
- pricing optimization platforms
- payment authorization systems
- backend integrations
- system modernization
- system decommission strategy
- performance optimization
- reactive processing
- async orchestration
- technical mentoring
- platform maintainability
- cross-team technical leadership

---

# Revision History

## 2026-05-23T14:27:00-06:00 — Initial Consolidated Version

Added and consolidated:

- Regular Pricing Optimization responsibilities
- Unified Pricing Engine (Drools) proof of concept
- Enterprise Kafka → Kafka as a Service migration
- Kafka shared library simplification
- National services decommission ownership
- SQL optimization (~4x improvement)
- Payment Estimator contributions
- WireMock integration testing
- mentoring and knowledge transfer
- leadership and cross-team collaboration

---

## 2026-05-23T15:09:00-06:00 — Final Consolidated Version

Expanded and finalized:

- business context for Pricing and Payments
- architecture overview
- async processing using CompletableFuture / Flux / Scheduled jobs
- detailed Drools responsibilities and outcomes
- deeper Kafka migration details
- Payment Estimator provider integration work
- Dynatrace observability responsibilities
- operational and DevOps exposure
- stronger technical leadership and ownership narrative
- normalized technical stack and strongest technical themes