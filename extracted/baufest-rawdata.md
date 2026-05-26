# Metadata

- Candidate: Alejandro Gomez Salgado  
- Company: Baufest  
- File Name: baufest-rawdata.md  
- Created By: ChatGPT — Interviewer Career Extractor (with Alejandro Gomez Salgado)  
- Created On: 2026-05-25T18:30:00-06:00  
- Last Updated: 2026-05-25T18:30:00-06:00  
- Time Zone: America/Mexico_City  
- Language: English  
- Status: In Review  
- Completeness: High (~90%)

---

# Baufest — Career Raw Data

## Base Information

- Company: Baufest
- Industry: Software Consulting / Fintech / Innovation / Digital Identity / AI
- Location: Remote
- Methodology: Agile / Scrum
- Main Roles:
  - Technical Lead — Lynk Jamaica
  - Architect — Innovation Lab

---

# Period 1 — Lynk Jamaica (Digital Wallet)

## Role
Technical Lead

## Duration
March 2022 – September 2023

## Client
Lynk — Jamaica Digital Wallet Ecosystem

Associated with Jamaica’s digital banking and Central Bank Digital Currency initiatives.

## Business Context

Lynk was a digital wallet platform enabling secure digital financial transactions for end users in Jamaica.

The platform supported:

- wallet account creation
- authentication
- biometric identity verification
- digital onboarding
- customer verification
- remittances
- money movement
- digital signing
- CBDC-related operations

Users could register, verify identity, receive remittances, send money, and operate through digital wallet services integrated with banking systems.

The platform operated in a regulated fintech environment where security, compliance, and reliability were critical.

## Architecture Overview

### Main Architectural Style

- Microservices architecture
- Event-driven communication
- REST APIs
- Webhook-based integrations
- Distributed backend services

### Identity & Verification

Integrated identity providers:

- Auth0
- OnFido

Responsibilities included:

- authentication
- user verification
- biometric validation
- KYC workflows
- digital identity lifecycle

### Payments & Remittances

Backend services supporting:

- remittance workflows
- wallet funding
- transaction processing
- CBDC-related financial operations
- secure money movement integrations

### Event-Driven Backend

Microservices communicated through asynchronous event-driven patterns using Kafka and internal backend event publishing.

Used to support:

- identity status propagation
- remittance execution
- async verification updates
- downstream notification flows

## Technical Responsibilities

### Backend Engineering

- Designed and developed backend microservices for digital wallet operations.
- Implemented REST APIs for authentication and transactional workflows.
- Built event-driven backend services supporting distributed platform operations.
- Developed integrations for identity verification providers.
- Supported secure financial transaction orchestration.

### Auth0 Integration

Implemented and maintained authentication workflows using Auth0, including:

- login flows
- secure token handling
- webhook integration
- identity event processing

### OnFido Integration

Integrated OnFido for customer identity verification and biometric onboarding.

Responsibilities included:

- webhook handling
- document validation flows
- identity verification callbacks
- backend orchestration of verification results
- customer onboarding status propagation

### Webhook Processing

Built backend webhook consumers responsible for:

- receiving provider callbacks
- validating external payloads
- processing identity verification updates
- updating customer verification status
- triggering downstream workflows

### Event-Driven Systems

Designed and maintained event-driven workflows for:

- identity lifecycle updates
- payment/remittance processing
- async backend coordination
- inter-service communication

## Technical Leadership

### Team Leadership

Acted as Technical Lead across engineering teams.

Responsibilities included:

- technical leadership
- backend design decisions
- code reviews
- mentoring engineers
- delivery coordination
- backlog clarification
- cross-team collaboration

### Engineering Process

Led team execution through:

- Agile/Scrum ceremonies
- sprint planning
- refinement sessions
- technical reviews
- CI/CD practices
- release coordination
- production deployment validation

### Production Ownership

Contributed to:

- production deployments
- runtime troubleshooting
- incident analysis
- deployment validation
- post-release monitoring

## Technical Challenges & Key Contributions

### Identity & Verification Reliability

Worked on critical identity verification flows where customer verification status had to remain synchronized between providers and internal wallet services.

Focused on:

- webhook timing consistency
- provider callback validation
- state synchronization
- secure onboarding reliability

### Distributed Financial Transaction Flows

Worked on backend flows supporting remittances and secure financial transactions where reliability and compliance were critical.

Focused on:

- transactional integrity
- distributed backend coordination
- service reliability
- secure financial processing

## Tech Stack

### Languages
- Java

### Frameworks
- Spring Boot
- Spring Framework

### Security / Identity
- Auth0
- OnFido

### Messaging
- Kafka

### Databases
- PostgreSQL

### APIs
- REST APIs
- Webhooks

### DevOps / Delivery
- CI/CD pipelines
- Cloud deployments

---

# Period 2 — Baufest Innovation Lab

## Role
Architect

## Duration
October 2023 – April 2024

## Business Context

Worked within Baufest’s innovation area focused on exploring emerging technologies and validating new technical initiatives.

Main focus areas:

- Generative AI
- Large Language Models
- enterprise chat systems
- embeddings
- AI benchmarking
- developer tooling evaluation
- micro frontend exploration

## Technical Responsibilities

### LLM-Based Chat Platform

Designed and led an initiative to build an enterprise conversational AI platform using Azure AI technologies.

Responsibilities:

- solution design
- LLM experimentation
- prompt evaluation
- architecture validation
- embeddings strategy
- answer quality benchmarking

### AI Benchmarking

Defined evaluation frameworks to compare:

- prompts
- models
- processed knowledge sources
- response quality
- accuracy of generated answers

### Embeddings & Retrieval

Worked on document processing and embeddings-based retrieval for contextual AI responses.

Focus included:

- data ingestion
- embedding generation
- semantic search
- contextual answer generation

### AI Engineering Exploration

Researched and documented emerging AI development tools for engineering productivity.

### Micro Frontend Exploration

Led exploration of micro frontend architectures including:

- feasibility analysis
- documentation
- technical validation
- architectural recommendations

## Tech Stack

- Java
- Python
- Spring
- Angular
- Azure AI
- OpenAI APIs
- embeddings-based retrieval systems

## Leadership Signals

- Technical leadership
- Architecture ownership
- Innovation initiative ownership
- Research & prototyping
- AI experimentation
- Mentoring and technical guidance
- Cross-team collaboration
- Strategic technical evaluation

---

# Revision History

## 2026-05-25T18:30:00-06:00 — Initial Version
- Created Baufest raw data
- Added Lynk Jamaica technical experience
- Added Auth0 / OnFido integrations
- Added digital wallet and remittance context
- Added Innovation Lab LLM initiative
- Added AI benchmarking and embeddings work
- Added leadership and architecture signals

