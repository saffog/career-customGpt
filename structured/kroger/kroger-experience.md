---
metadata:
  company: Kroger
  document_type: experience
  source_of_truth: kroger-rawdata.md
  created_at: 2026-05-23T20:00:00Z
  updated_at: 2026-05-23T20:00:00Z
  created_by: Career Database Structurer GPT
  last_updated_by: Career Database Structurer GPT
  status: active
  version: 1.0
  review_status: draft
---
# Kroger — Experience

# Company Information

- Company: Kroger
- Role: Senior Backend Software Engineer
- Dates:
  - Pricing Division: July 2024 – December 2025
  - Payments Division: January 2026 – May 2026
- Industry: Retail / Pricing Optimization / Payments
- Work Model: Remote
- Methodology: Agile / Scrum

# Team Structure

Cross-functional engineering organization working with:

- Backend Engineers
- Tech Leads
- Product Owners
- QA Engineers
- ETL Teams
- Support Teams
- Platform Owners

# Business Context

Worked on large-scale internal platforms supporting pricing operations and payment processing across Kroger store divisions.

Primary domains included:

- pricing configuration management
- rule execution and pricing optimization workflows
- floor and ceiling price validations
- competitor pricing comparison
- payment authorization
- benefit card eligibility
- payment coverage calculations

Most systems were internal-facing and business-critical, where correctness and operational reliability were prioritized over raw traffic throughput.

# Core Responsibilities

- Designed and maintained Spring Boot microservices
- Built and enhanced REST APIs
- Developed backend integrations with internal and external systems
- Supported event-driven workflows using Kafka
- Built and maintained pricing workflow services
- Supported payment estimator backend integrations
- Performed performance optimization and SQL tuning
- Contributed to testing automation and QA validation
- Participated in production monitoring and deployment validation

# Major Initiatives

## Unified Pricing Engine (Drools POC)

### Objective

Evaluate Drools as a configurable rule engine to modernize Kroger pricing rule execution.

### Contributions

- Learned Drools from scratch and led early technical exploration
- Built multiple proof-of-concepts around rule execution lifecycle
- Reverse-engineered legacy pricing logic
- Translated pricing rules into spreadsheet-driven rule definitions
- Implemented backend stories supporting the proof of concept
- Collaborated with Tech Lead and Product Owner on functional scope
- Supported QA validation and stakeholder demo preparation
- Shared implementation knowledge across the team

### Impact

- Validated Drools as a viable pricing rule engine
- Delivered a functional end-to-end proof of concept
- Created reusable technical knowledge for future pricing initiatives

### Technologies

Java, Spring Boot, Drools, PostgreSQL

---

## Kafka Migration — Enterprise Kafka to Kafka as a Service

### Objective

Support enterprise migration from Enterprise Kafka to Kafka as a Service.

### Contributions

- Reviewed shared Kafka configuration structure
- Identified redundant configuration between library abstractions and native Kafka properties
- Proposed simplification approach
- Refactored shared Kafka configuration
- Consolidated producer and consumer configuration setup

### Impact

- Reduced duplicated configuration
- Improved maintainability
- Simplified adoption across teams during migration

### Technologies

Kafka, Enterprise Kafka, Kafka as a Service, Spring Boot

---

## National Services Decommission

### Objective

Safely retire legacy National pricing-related services and dependencies.

### Contributions

- Led dependency analysis across services
- Reviewed producers, consumers and ETL dependencies
- Validated downstream impact
- Coordinated rollout planning across multiple teams
- Supported execution planning for decommission

### Impact

- Successful decommission of legacy services
- Reduced technical debt
- Removed unused dependencies while minimizing operational risk

### Technologies

Spring Boot, Kafka, ETL workflows, PostgreSQL

---

## Payment Estimator

### Objective

Support backend payment estimation workflows for tender validation and benefit eligibility.

### Contributions

- Built and maintained backend logic for item eligibility validation
- Supported payment authorization workflows
- Worked on benefit card validations
- Supported provider integrations
- Implemented and validated third-party integration testing using WireMock

### Impact

- Improved payment workflow reliability
- Strengthened test coverage for provider integrations

### Technologies

Java, Spring Boot, WireMock, JUnit, Mockito

# Leadership & Collaboration

- Technical ownership of National decommission analysis
- Ownership of Kafka shared library simplification initiative
- Mentored developers on Drools implementation patterns
- Mentored peers on Kafka integration practices
- Participated in code reviews
- Story refinement and technical planning
- QA validation discussions
- Cross-team coordination across engineering and ETL teams
- Participated in stakeholder-facing technical demos

# Operational Exposure

- GitHub Actions CI/CD pipelines
- SonarQube quality validation
- Harness deployments
- Rancher
- Kubernetes runtime diagnostics
- Dynatrace monitoring dashboards
- deployment validation
- application log analysis

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

## DevOps & Infrastructure
- Kubernetes
- Rancher
- Harness
- GitHub Actions
- SonarQube

## Monitoring
- Dynatrace

# Key Achievements

- Delivered successful Drools-based pricing engine proof of concept
- Led technical analysis for National platform decommission
- Simplified Kafka shared configuration during enterprise migration
- Achieved ~4x SQL performance improvement in pricing workflows
- Supported reliable payment provider integrations through automated testing