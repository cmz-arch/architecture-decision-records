# Architecture Decision Records

Consulting-style Architecture Decision Record (ADR) templates and examples for documenting architecture decisions, trade-offs, and consequences.

This repository is designed for software architects, solutions architects, staff engineers, engineering managers, and technical consultants who want to make important technical decisions explicit, reviewable, and traceable.

---

## Purpose

Architecture decisions shape the long-term maintainability, scalability, reliability, security, and delivery flow of a software system.

However, many important decisions are made in meetings, chat threads, or pull request discussions and then forgotten.

This repository helps teams:

- Document important architecture decisions
- Make trade-offs explicit
- Capture context and constraints
- Record alternatives considered
- Explain consequences and risks
- Improve technical alignment across teams
- Create a decision history for future maintainers
- Support architecture reviews and consulting assessments

---

## What Is an ADR?

An Architecture Decision Record is a lightweight document that captures an important technical or architectural decision.

A good ADR answers:

- What problem are we solving?
- What context and constraints matter?
- What options did we consider?
- What decision did we make?
- Why did we choose this option?
- What trade-offs are we accepting?
- What consequences should future teams understand?

ADRs are not meant to be long design documents. They are concise records of decisions that should remain understandable over time.

---

## Repository Structure

```text
architecture-decision-records/
  README.md

  templates/
    adr-template.md
    lightweight-adr-template.md
    rfc-template.md
    decision-log-template.md

  examples/
    0001-use-modular-monolith-first.md
    0002-adopt-ai-assisted-code-review.md
    0003-introduce-event-driven-integration.md
    0004-extract-billing-service.md
    0005-adopt-observability-platform.md
    0006-use-postgresql-as-primary-database.md

  guidance/
    how-to-write-good-adrs.md
    when-to-use-adr-vs-rfc.md
    adr-review-checklist.md
    tradeoff-analysis-guide.md
```

---

## When to Write an ADR

Write an ADR when a decision has meaningful long-term impact.

Typical ADR topics include:

- Choosing an architectural style
- Moving from monolith to microservices
- Introducing event-driven integration
- Choosing a database or storage technology
- Defining service boundaries
- Adopting an API standard
- Introducing a new platform capability
- Changing deployment or delivery strategy
- Adopting AI-assisted development workflows
- Introducing observability, security, or governance standards
- Making a decision that is difficult or expensive to reverse

You do not need an ADR for every implementation detail. Use ADRs for decisions that future teams will need to understand.

---

## ADR Template

A standard ADR should include the following sections.

```markdown
# ADR-0000: Decision Title

## Status

Proposed | Accepted | Deprecated | Superseded

## Date

YYYY-MM-DD

## Context

What is the situation, problem, or opportunity?

## Problem

What decision needs to be made?

## Constraints

What technical, business, organizational, operational, or regulatory constraints matter?

## Options Considered

### Option 1: Description

Pros:

- ...

Cons:

- ...

### Option 2: Description

Pros:

- ...

Cons:

- ...

## Decision

What option did we choose?

## Rationale

Why did we choose this option?

## Consequences

What are the expected positive and negative consequences?

## Risks

What risks remain after the decision?

## Follow-up Actions

What must happen next?

## Related Documents

Links to related issues, pull requests, design docs, diagrams, or previous ADRs.
```

---

## Example ADR Topics

This repository includes example ADRs for common architecture decisions.

### Use Modular Monolith First

A decision record explaining why a team may choose a modular monolith before introducing microservices.

Key themes:

- Team maturity
- Domain boundaries
- Deployment complexity
- Operational readiness
- Evolutionary architecture

### Adopt AI-Assisted Code Review

A decision record for introducing AI-supported code review workflows.

Key themes:

- Developer productivity
- Review quality
- Human accountability
- Security and correctness
- Governance of AI-generated suggestions

### Introduce Event-Driven Integration

A decision record for using events to decouple parts of a system.

Key themes:

- Service coupling
- Async communication
- Event contracts
- Observability
- Failure handling

### Extract Billing Service

A decision record for extracting a business capability from a monolith.

Key themes:

- Domain ownership
- Data ownership
- Migration strategy
- API contracts
- Operational readiness

### Adopt Observability Platform

A decision record for standardizing logs, metrics, traces, dashboards, and alerting.

Key themes:

- Production visibility
- Incident response
- Reliability
- Operational ownership
- Platform standards

---

## ADR Statuses

Use simple statuses to track the lifecycle of a decision.

### Proposed

The decision is being discussed but has not been accepted.

### Accepted

The decision has been approved and should guide implementation.

### Deprecated

The decision is no longer recommended, but may still exist historically.

### Superseded

The decision has been replaced by a newer ADR.

When superseding an ADR, link to the new decision record.

---

## ADR Numbering

Use a simple numeric format:

```text
0001-use-modular-monolith-first.md
0002-adopt-ai-assisted-code-review.md
0003-introduce-event-driven-integration.md
```

Recommended naming rules:

- Use four-digit numbers
- Use lowercase file names
- Use hyphens between words
- Keep titles clear and specific
- Do not renumber old ADRs
- Preserve historical decisions even if they are later replaced

---

## ADR vs RFC

Use an ADR when the main purpose is to record a decision.

Use an RFC when the main purpose is to propose, discuss, and refine a larger design before a decision is made.

### Use an ADR for:

- A single important decision
- A decision that has already been made
- A record of trade-offs and consequences
- A lightweight decision history

### Use an RFC for:

- A larger design proposal
- A decision that needs broad feedback
- A complex cross-team change
- A technical strategy that requires review before approval

In many teams, an RFC can lead to one or more ADRs.

---

## Decision Quality Checklist

Before accepting an ADR, review whether it clearly answers the following questions:

- Is the problem clearly stated?
- Is the context understandable to someone outside the original discussion?
- Are the key constraints documented?
- Were realistic alternatives considered?
- Are the trade-offs explicit?
- Is the rationale clear?
- Are consequences and risks described?
- Are follow-up actions defined?
- Are related documents linked?
- Would this ADR still be useful one year from now?

---

## Common ADR Mistakes

Avoid these common mistakes:

### Writing only the final answer

An ADR should explain why the decision was made, not just what was chosen.

### Ignoring rejected options

Rejected options often contain the most useful learning for future teams.

### Hiding trade-offs

Every meaningful architecture decision has costs and risks.

### Writing too much

An ADR should be concise. If it becomes too large, consider writing an RFC or design document.

### Treating ADRs as permanent truth

Architecture decisions can change. When they do, supersede old ADRs instead of deleting them.

### Writing ADRs after everyone forgets the context

Document decisions close to the time they are made.

---

## Principles

The ADR practice in this repository is based on the following principles.

### 1. Decisions should be traceable

Future teams should understand why a decision was made.

### 2. Trade-offs matter more than opinions

Good architecture documentation explains constraints, options, and consequences.

### 3. Lightweight documentation is better than undocumented decisions

ADRs should be easy enough that teams actually write them.

### 4. Decisions evolve

Old ADRs should remain visible, but they can be deprecated or superseded.

### 5. Architecture is a social process

ADRs help align engineers, product managers, security teams, operations teams, and leadership.

### 6. Context is part of the decision

The same technical choice can be good or bad depending on the context.

---

## Example Use Cases

This repository can help when you need to:

- Start using ADRs in an engineering team
- Create an architecture decision history
- Improve architecture review quality
- Document cloud, data, API, or platform decisions
- Support legacy modernization work
- Prepare consulting-style architecture assessments
- Explain technical trade-offs to stakeholders
- Create a repeatable architecture governance process
- Improve onboarding for future engineers

---

## Suggested Reading Path

If you are new to ADRs, start here:

1. `guidance/how-to-write-good-adrs.md`
2. `templates/adr-template.md`
3. `templates/lightweight-adr-template.md`
4. `guidance/adr-review-checklist.md`
5. `examples/0001-use-modular-monolith-first.md`
6. `examples/0002-adopt-ai-assisted-code-review.md`
7. `guidance/when-to-use-adr-vs-rfc.md`

---

## Who This Is For

This repository is designed for:

- Software architects
- Solutions architects
- Staff and principal engineers
- Engineering managers
- Platform engineering teams
- Technical consultants
- Teams adopting architecture governance
- Teams modernizing legacy systems
- Teams improving technical decision-making

---

## Current Status

This repository is a living collection of ADR templates, examples, and guidance.

Planned content:

- Standard ADR template
- Lightweight ADR template
- RFC template
- Decision log template
- ADR review checklist
- Trade-off analysis guide
- Modular monolith ADR example
- AI-assisted engineering ADR example
- Event-driven architecture ADR example
- Service extraction ADR example
- Observability platform ADR example
- Database selection ADR example

---

## Consulting Themes

The materials in this repository are aligned with the following consulting themes:

- Architecture decision-making
- Architecture governance
- Legacy modernization
- Modular monolith design
- Microservices migration
- AI-assisted software engineering adoption
- Cloud-native architecture
- Platform engineering
- Technical assessment and review
- Engineering maturity improvement

---

## About Me

I am a Solutions Architect based in Berlin, focused on:

- AI-assisted software engineering
- Legacy modernization
- Cloud-native architecture
- Modular monoliths and microservices migration
- Architecture decision-making
- Software delivery improvement

I help engineering teams adopt AI-assisted development practices, improve delivery flow, and modernize legacy systems into scalable, maintainable, cloud-native architectures.

---

## License

This repository is licensed under the MIT License.

You are free to use, adapt, and share the materials, with attribution appreciated.
