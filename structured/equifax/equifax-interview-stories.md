---
metadata:
  company: Equifax
  document_type: interview-stories
  source_of_truth: equifax-rawdata.md
  created_at: 2026-05-26T00:50:00Z
  updated_at: 2026-05-26T00:50:00Z
  created_by: Career Database Structurer GPT
  last_updated_by: Career Database Structurer GPT
  status: active
  version: 1.0
  review_status: draft
---
# Equifax — Interview Stories

# 1. Modernizing Critical Batch Processing from Pro*C to Apache Spark

## Interview Themes

Architecture modernization, legacy transformation, distributed systems, technical leadership

## Situation

Equifax had critical Collections & Recoveries batch processes implemented in legacy Pro*C with years of accumulated business logic.

These jobs processed millions of accounts daily and were core to operational debt collection workflows.

## Problem / Risk

The platform had strong dependency on legacy structured programming that was difficult to scale, maintain, and evolve.

Any modernization effort risked breaking complex business rules embedded over many years.

## Task

Lead the analysis and modernization effort to migrate the batch platform to Java and Apache Spark while preserving existing behavior.

## Constraints

- large legacy codebase
- undocumented business rules
- millions of daily records
- strict overnight execution windows
- zero tolerance for business logic regressions

## Actions

- reverse-engineered existing Pro*C processes
- documented inputs, outputs, dependencies, and hidden business rules
- translated procedural logic into object-oriented architecture
- learned Apache Spark quickly to support implementation
- wrote user stories for engineering execution
- collaborated with development teams throughout delivery
- validated behavior against legacy execution results

## Technical Decisions

Selected Java and Apache Spark to enable distributed scalable processing while improving maintainability.

Designed migration around behavior preservation before optimization.

## Tradeoffs

Preserved existing business behavior first, even when cleaner redesign opportunities existed.

This increased migration effort but reduced operational risk significantly.

## Result

Successfully modernized critical batch workflows while maintaining functional continuity across enterprise collections processing.

## Key Signals

Legacy modernization, architecture ownership, distributed systems, risk management

## Reusable Talking Points

“How I led modernization of a critical legacy batch platform while preserving years of embedded business logic.”

---

# 2. Learning Apache Spark Under Tight Delivery Constraints

## Interview Themes

Learning velocity, adaptability, technical execution under pressure

## Situation

As part of the batch modernization initiative, Apache Spark became a required technology despite limited prior experience internally.

## Problem / Risk

The project timeline required rapid delivery while adopting a new distributed processing framework.

There was little room for long experimentation cycles.

## Task

Ramp up on Spark quickly enough to contribute to architecture and implementation decisions.

## Constraints

- unfamiliar technology
- delivery deadlines
- production-critical workloads
- enterprise-scale datasets

## Actions

- studied Spark architecture and processing model independently
- connected Spark concepts to existing batch processing knowledge
- applied learning directly to implementation work
- collaborated closely with engineering teams while ramping up
- validated technical feasibility through practical execution

## Technical Decisions

Focused on understanding distributed processing fundamentals first rather than framework-specific details only.

Used prior batch-processing domain knowledge as a bridge into Spark.

## Tradeoffs

Fast practical adoption over theoretical specialization.

## Result

Successfully contributed to delivery of Spark-based modernization effort within project timelines.

## Key Signals

Fast learner, adaptability, execution in ambiguity

## Reusable Talking Points

“How I learned Apache Spark quickly under delivery pressure and applied it to a production modernization effort.”

---

# 3. Modernizing Decision Network UI from Flex to Angular

## Interview Themes

Modernization, frontend architecture, continuous learning

## Situation

Equifax needed to modernize a central UI platform used to configure decision networks for Collections & Recoveries.

## Problem / Risk

The existing Flex-based platform had growing maintainability limitations and aging technology support.

## Task

Help migrate the platform to Angular while preserving core business capabilities.

## Constraints

- legacy UI complexity
- business-critical workflows
- new frontend technology stack
- ongoing operational usage

## Actions

- learned Angular and TypeScript during implementation
- worked with GoJS for visual workflow rendering
- implemented new UI functionality
- supported migration of configuration workflows
- collaborated with product and technical stakeholders

## Technical Decisions

Used Angular + TypeScript for maintainability and long-term platform evolution.

GoJS enabled visual modeling of decision workflows.

## Tradeoffs

Migration complexity and learning curve in exchange for long-term maintainability.

## Result

Delivered modernization of a core business configuration platform while improving usability and future extensibility.

## Key Signals

Adaptability, modernization experience, frontend architecture exposure

## Reusable Talking Points

“How I helped modernize a business-critical legacy UI platform into Angular.”

---

# 4. Leading Knowledge Transfer with Dublin Engineering Teams

## Interview Themes

Mentoring, cross-functional leadership, communication, global collaboration

## Situation

Equifax needed to expand platform knowledge beyond the Mexico-based teams and support engineering growth in Dublin.

## Problem / Risk

A large amount of business and technical knowledge existed only with a limited group of engineers.

This created operational and delivery dependency risks.

## Task

Lead technical and functional knowledge transfer for the Dublin engineering organization.

## Constraints

- complex business domain
- multiple Scrum teams
- international collaboration
- technical and functional context needed simultaneously

## Actions

- led technical walkthroughs
- explained Collections & Recoveries workflows
- documented platform behavior
- mentored engineers
- answered domain and architecture questions
- supported onboarding across multiple teams

## Technical Decisions

Structured knowledge transfer around business workflows and system behavior rather than code-only explanations.

## Tradeoffs

Higher upfront time investment in enablement in exchange for stronger long-term organizational scalability.

## Result

Reduced dependency on localized knowledge and improved collaboration between Mexico and Ireland teams.

## Key Signals

Mentoring, organizational leadership, communication, international collaboration

## Reusable Talking Points

“How I transferred complex platform knowledge across international engineering teams.”

---

# 5. Leading Two Hybrid Engineering Teams in Mexico

## Interview Themes

People leadership, delivery execution, team management

## Situation

Later in Equifax, responsibility expanded from technical execution into delivery leadership across multiple teams.

## Problem / Risk

Multiple teams required alignment across backlog execution, delivery planning, technical coordination, and stakeholder expectations.

## Task

Lead engineering execution across two hybrid teams.

## Constraints

- multiple teams
- parallel workstreams
- delivery commitments
- coordination across roles and stakeholders

## Actions

- managed delivery planning and follow-up
- mentored engineers
- supported Product Owners
- facilitated Agile ceremonies
- coordinated technical alignment
- supported releases and execution planning
- worked with stakeholders on delivery visibility

## Technical Decisions

Balanced technical depth with operational leadership, staying close enough to engineering to unblock teams while driving execution.

## Tradeoffs

Balancing hands-on technical involvement vs management responsibilities.

## Result

Successfully led delivery across multiple teams while maintaining strong engineering collaboration and execution consistency.

## Key Signals

Engineering leadership, delivery management, mentoring, organizational execution

## Reusable Talking Points

“How I led multiple hybrid engineering teams while balancing delivery, people leadership, and technical execution.”