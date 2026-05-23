# Kroger — Raw Data

---

# Metadata

- Candidate: Alejandro Gomez Salgado
- Company: Kroger
- File Name: kroger-rawdata.md
- Created By: ChatGPT — Interviewer Career Extractor (with Alejandro Gomez Salgado)
- Created On: 2026-05-23T14:27:00-06:00
- Last Updated: 2026-05-23T14:27:00-06:00
- Time Zone: America/Mexico_City
- Language: English
- Status: In Review
- Completeness: High (~95%)

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

# Revision History

## 2026-05-23T14:27:00-06:00 — Initial Consolidated Version

Added and consolidated:

- Regular Pricing Optimization responsibilities
- Unified Pricing Engine (Drools) proof of concept
- Enterprise Kafka → Kafka as a Service migration work
- Kafka shared library configuration simplification
- National services decommission ownership
- SQL performance optimization (~4x improvement)
- Payment Estimator contributions
- WireMock integration testing
- mentoring and knowledge transfer in Drools and Kafka
- leadership and cross-team collaboration signals

Pending review:

- Final wording validation by Alejandro
- Optional business metrics if remembered later
- Optional additional examples from Payments division

---

## Base Information

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

Kroger operates large-scale internal pricing and payment platforms supporting retail operations across multiple store divisions.

The systems I worked on supported:

- pricing configuration management
- pricing optimization workflows
- configurable pricing rules
- floor/ceiling price validations
- competitor pricing comparison
- payment authorization and tender validation
- benefit card eligibility
- internal pricing execution and orchestration

Most pricing APIs were internal-facing and configuration-oriented rather than customer-facing.

These APIs were mainly used for:

- pricing settings management
- rule administration
- scheduled workflows
- batch-oriented processing

Traffic volume was relatively low compared to customer-facing APIs, but business correctness and pricing accuracy were critical since pricing changes directly impacted store operations.

Pricing rules were typically updated based on:

- weekly business cycles
- promotional windows
- seasonal campaigns
- monthly pricing periods

---

# Architecture Overview

Kroger commonly follows a layered service architecture:

Frontend → Interface Service → Data Service → Database

Characteristics:

- Spring Boot microservices
- REST APIs
- Event-driven integrations
- Kafka producers and consumers
- JWT Bearer Token authorization
- Feign-based service communication
- PostgreSQL / DB2 persistence
- Kubernetes deployment
- CI/CD automation

---

# Pricing Division

## Main Systems

Worked primarily on:

- RPO Settings
- RPO Upkeep
- Regular Pricing Rules
- Unified Pricing Engine (UPE)

Microservices included:

- rpo-settings-interface
- rpo-settings-data
- regular-pricing-rules-interface
- regular-pricing-rules-data

Responsibilities included:

- building APIs
- maintaining pricing workflows
- rule processing
- scheduled backend execution
- integration with internal pricing systems
- backend support for downstream pricing consumers

---

# Unified Pricing Engine (Drools POC)

## Overview

The most representative project during my time at Kroger was the Unified Pricing Engine proof of concept based on Drools.

The goal was to evaluate whether Drools could support configurable pricing rules in a maintainable and scalable way, replacing part of the legacy pricing logic with a modern rule-based platform.

---

## Responsibilities

### Technical Learning & Prototyping
- Learned Drools from scratch.
- Built several proofs of concept to understand:
  - rule execution lifecycle
  - spreadsheet-driven rule definitions
  - rule compilation
  - backend integration patterns

---

### Legacy Analysis
- Analyzed legacy pricing systems to understand existing pricing rules.
- Reverse-engineered pricing conditions, fields, inputs, and outputs.
- Identified how to transform existing business rules into Drools-compatible logic.

---

### Rule Modeling
- Translated pricing rules into spreadsheet-based rule definitions.
- Helped define the mapping between spreadsheet fields and Drools execution.
- Supported configurable business-managed pricing rule modeling.

---

### Technical Collaboration
- Worked closely with Tech Lead and Product Owner to refine user stories for the proof of concept.
- Helped shape functional scope and technical feasibility for stakeholder demos.

---

### Knowledge Sharing
- Explained Drools concepts and implementation approach to other developers and technical leadership.
- Shared architecture and rule modeling approach with team members.

---

### Delivery
- Implemented backend stories for the POC.
- Participated in QA validation and functional testing.
- Helped prepare and demonstrate a working end-to-end demo for Kroger stakeholders.

---

## Outcome

The proof of concept successfully demonstrated that Drools could be used as a configurable pricing rule engine inside Kroger.

Main outcomes:

- validated Drools as a rule engine option for pricing workflows
- modernized representation of legacy pricing logic
- enabled spreadsheet-driven rule configuration
- delivered a working demo to stakeholders
- generated reusable technical knowledge inside the team

---

# Kafka Migration — Enterprise Kafka to Kafka as a Service

## Overview

Participated in Kroger’s Enterprise Kafka (EK) to Kafka as a Service (KaaS) migration.

---

## Key Contribution

While reviewing shared Kafka configuration YAML files, I identified redundant configuration between:

- custom library-level parameters
- actual Kafka producer/consumer configuration properties

The shared Kafka library exposed internal custom parameters which were later translated into native Kafka configuration values.

This created unnecessary duplication and additional maintenance complexity.

---

## Actions

- reviewed Kafka YAML configuration structure
- analyzed how library parameters mapped into Kafka runtime configuration
- discussed findings with the Technical Lead
- proposed simplifying configuration by removing redundant abstraction layers
- refactored shared Kafka library configuration
- consolidated shared producer and consumer configuration parameters

---

## Result

- reduced duplicated configuration
- simplified YAML setup
- improved maintainability
- easier migration adoption across teams
- improved consistency across environments

---

# National Services Decommission

## Business Context

National was a pricing-related business division / store segmentation inside Kroger.

The National platform had its own dedicated architecture composed of:

- frontend application
- interface service
- data service
- database instance

The interface service also participated in event-driven workflows by consuming and producing events connected to ETL processes.

ETL jobs generated events consumed by National services and additional downstream services depended on those event flows.

---

## Ownership

I had direct ownership of the technical decommission analysis and coordination.

Responsibilities included:

- mapping system dependencies
- identifying service interactions
- analyzing Kafka producers and consumers
- validating ETL-generated event dependencies
- reviewing downstream impact
- coordinating rollout planning across teams

---

## Cross-Team Collaboration

Worked with:

- backend engineering teams
- ETL teams
- support teams
- QA teams
- service owners from dependent systems

Each team owned different parts of the workflow, so decommission required coordinated execution across multiple ownership boundaries.

---

## Result

- safe retirement of legacy National pricing components
- reduction of technical debt
- removal of unused dependencies
- controlled rollout with minimized operational risk

---

# Payments Division

## Main System

payment-estimator

Main responsibilities:

- item eligibility validation
- payment tender authorization
- food benefit card validations
- payment coverage calculation
- provider integration workflows

Provider modules included:

- nations-transactions
- solutran-transactions

---

# Performance Optimization

## SQL Optimization

One of the most relevant performance improvements involved simplifying a complex SQL query used in pricing workflows.

Actions:
- analyzed the original SQL implementation
- removed unnecessary complexity and redundant query logic
- preserved functional behavior while improving execution efficiency

Result:
- execution time reduced to approximately 25% of the original runtime
- roughly 4x performance improvement

---

# Testing & Quality

Worked with:

- JUnit
- Mockito
- WireMock
- integration testing
- Postman

WireMock was used extensively in payment integrations to simulate third-party providers using dynamic request-driven responses.

---

# Operational & DevOps Exposure

Worked with:

- GitHub Actions
- SonarQube
- Harness
- Rancher
- Kubernetes logs
- Dynatrace dashboards
- deployment validation
- runtime diagnostics

No major production incidents occurred during my time supporting these components, reflecting a mature engineering lifecycle with strong QA, staged rollout validation, and operational monitoring.

---

# Leadership & Technical Influence

Examples of technical leadership:

- ownership of National decommission initiative
- ownership of Kafka shared library refactor
- mentoring team members on Drools
- mentoring team members on Kafka integration
- peer code reviews
- story refinement
- QA validation discussions
- technical documentation
- cross-team coordination with engineering and ETL teams
- stakeholder-facing technical demo participation

---

# Technical Stack

## Languages
- Java 11
- Java 17

## Frameworks
- Spring Boot
- Spring MVC
- Spring Data
- Spring Security
- Spring WebFlux
- Feign
- Resilience4j
- JPA / Hibernate
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
- Harness
- GitHub Actions
- SonarQube

## Monitoring
- Dynatrace

## Documentation / Collaboration
- Jira
- Confluence
- draw.io

---

# Strongest Technical Themes

- Java backend engineering
- Spring Boot microservices
- event-driven systems
- pricing optimization platforms
- configurable rule engines
- payment authorization systems
- Kafka modernization
- distributed systems
- backend integrations
- system decommission strategy
- performance optimization
- technical mentoring
- platform maintainability