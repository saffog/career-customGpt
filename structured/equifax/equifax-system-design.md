---
metadata:
  company: Equifax
  document_type: system-design
  source_of_truth: equifax-rawdata.md
  created_at: 2026-05-26T00:35:00Z
  updated_at: 2026-05-26T00:35:00Z
  created_by: Career Database Structurer GPT
  last_updated_by: Career Database Structurer GPT
  status: active
  version: 1.0
  review_status: draft
---
# Equifax — System Design

# Business Purpose

Equifax Collections & Recoveries platforms supported enterprise financial operations focused on debt collection, recoveries management, workflow execution, and account processing at large scale.

Core platform goals included:

- high-volume account processing
- collections workflow orchestration
- recoveries execution
- decision network configuration
- operational reliability
- maintainability of critical business logic
- modernization of long-lived enterprise systems

These systems were business-critical and directly tied to daily financial operations across enterprise clients.

---

# Architecture Overview

Primary platform architecture evolved over time from legacy monolithic and batch-based systems into more distributed and modern service-oriented platforms.

Typical architecture patterns included:

## Batch Processing Layer

Data Sources → Batch Jobs → Business Rule Execution → Account Processing → Output Generation → Downstream Operational Systems

## Application Layer

Frontend UI → Business Services → Processing Services → Persistence Layer

## Modernized Distributed Processing Layer

Input Data → Distributed Processing (Apache Spark) → Transformation Logic → Business Rules Execution → Output Pipelines

---

# Core Components

# Collections & Recoveries Processing

Core responsibilities included:

- customer account ingestion
- collections execution
- recoveries workflows
- decision network processing
- nightly operational batch execution

---

# Batch Processing Platform

Critical platform for:

- large-scale account processing
- ETL-style transformations
- business rule execution
- scheduled overnight operations

Characteristics:

- millions of records processed
- daily execution cycles
- high dependency on correctness and repeatability

---

# Decision Network Configuration Platform

Business-facing platform for configuring decision flows used within Collections & Recoveries.

Supported:

- workflow configuration
- decision network visualization
- business rule representation
- operational decision management

---

# Communication Patterns

Communication varied by platform generation.

Primary patterns included:

- scheduled batch execution
- database-driven processing
- workflow orchestration across dependent systems
- service-to-service communication in modernized components
- UI-driven configuration changes persisted to backend systems

Batch processing relied heavily on deterministic sequential execution, while modernization introduced more distributed parallel execution models.

---

# Data Flow

# Batch Modernization Flow

Typical flow:

Source Data Extraction → Data Transformation → Business Rule Evaluation → Account Processing → Output Generation → Downstream Consumers

Migration required preserving exact functional behavior from legacy jobs while improving scalability and maintainability.

---

# Decision Network Flow

Typical flow:

Business User Configuration → UI Interaction → Workflow Definition → Persisted Configuration → Runtime Decision Execution

This enabled business teams to configure collections behavior visually without directly modifying backend logic.

---

# Scalability & Concurrency

# Batch Processing

Primary scalability challenges:

- millions of accounts processed daily
- overnight execution windows
- large transformation pipelines
- strict runtime completion expectations

Apache Spark was introduced to improve:

- parallel execution
- distributed workload processing
- scalability across large datasets
- performance of ETL operations

---

# UI Platform

Decision network UI required:

- maintainable frontend architecture
- scalable visualization of complex business workflows
- manageable evolution of business configuration capabilities

---

# Reliability Strategy

Reliability was critical because systems directly impacted financial operations.

Main reliability priorities:

- preserving business behavior during legacy modernization
- deterministic execution of nightly processing
- avoiding data loss or transformation regressions
- maintaining operational continuity during migrations
- minimizing disruption to collections and recoveries operations

Reliability approaches included:

- reverse engineering and documenting legacy logic before migration
- validating business rules against existing outputs
- dependency analysis
- staged implementation and rollout planning
- close collaboration with domain experts and engineering teams

---

# Security

Security considerations were primarily centered around enterprise financial data handling.

Included:

- secure access to internal systems
- protection of customer financial data
- controlled access to collections and recoveries workflows
- role-based access within internal operational platforms

As these were internal enterprise systems, emphasis was placed more on operational integrity and controlled access than public-facing API security.

---

# Design Decisions & Tradeoffs

# Legacy Batch Migration — Pro*C to Java + Apache Spark

## Decision

Modernize legacy structured-programming batch jobs into distributed object-oriented processing using Java and Apache Spark.

## Why

Legacy implementation created long-term maintainability and scalability limitations.

Spark introduced:

- distributed processing capabilities
- improved scalability
- more modern engineering practices
- easier future extensibility

## Tradeoffs

### Pros

- improved scalability
- easier maintainability
- object-oriented extensibility
- better long-term platform evolution

### Cons

- high migration complexity
- required reverse engineering of legacy business rules
- steep learning curve for Spark adoption
- strict requirement to preserve existing functional behavior

---

# Decision Network UI Modernization — Flex to Angular

## Decision

Replace Flex-based UI with Angular and TypeScript.

## Why

Flex was increasingly difficult to maintain and evolve.

Angular provided:

- modern frontend architecture
- stronger maintainability
- better long-term ecosystem support

## Tradeoffs

### Pros

- improved maintainability
- better developer ecosystem
- easier future evolution

### Cons

- migration effort
- required upskilling teams on Angular and TypeScript
- temporary complexity while transitioning platforms

---

# Operational Concerns

Key operational concerns included:

- nightly batch execution reliability
- runtime performance under large workloads
- legacy dependency management
- migration risk reduction
- documentation of hidden business rules
- knowledge transfer across teams
- maintaining continuity during organizational and technical transitions

---

# Testing Strategy

Testing and validation focused heavily on behavior preservation and operational correctness.

Approaches included:

- legacy output comparison during migration
- business rule validation
- functional verification against existing processes
- dependency validation
- integration validation across processing pipelines
- cross-team review with domain experts
- staged rollout verification

Because many systems encoded years of business behavior, validation required both technical testing and domain-level confirmation.

---

# Technologies Used

## Languages

- Java
- SQL
- Pro*C
- TypeScript
- JavaScript

## Frameworks / Libraries

- Apache Spark
- Spring Boot
- Angular
- GoJS

## Databases

- Oracle Database
- PostgreSQL

## Infrastructure

- AWS

## Delivery

- CI/CD

## Methodologies

- Agile
- Scrum