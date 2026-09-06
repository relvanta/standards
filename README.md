# Relvanta Engineering Standards
**Status:** Foundational
This repository is the canonical engineering knowledge source for Relvanta.
It defines the durable engineering intent, principles, standards, shared vocabulary, and reusable practices that should guide Relvanta repositories.
It is deliberately **not** a technology catalog, framework preference list, or implementation repository.
## Purpose
Relvanta builds software systems, products, experiments, and engineering tools. As the repository ecosystem grows, engineering intent must remain understandable and reusable across projects.
This repository exists to make that intent explicit and machine-consumable over time.
The goal is not to create a large rulebook.
Standards should be introduced when they:
- solve a real engineering problem
- reduce ambiguity
- establish a durable expectation
- enable reliable automation
- capture validated engineering knowledge
## Knowledge hierarchy

Human Intent
     ↓
Engineering Philosophy
     ↓
Engineering Principles
     ↓
Engineering Standards
     ↓
Architecture & Patterns
     ↓
Templates / Automation / Playbooks
     ↓
Projects & Experiments
     ↓
Operational Evidence
     ↓
Engineering Knowledge
     ↓
Engineering Intelligence

###The layers have different responsibilities:

* Philosophy — why we engineer the way we do.
* Principles — durable statements about what should generally be true.
* Standards — explicit expectations that projects can be evaluated against.
* Architecture & patterns — proven ways of implementing recurring engineering concerns.
* Templates, automation and playbooks — reusable mechanisms that make intent easier to apply.
* Projects & experiments — where ideas are implemented and tested.
* Operational evidence — what actually happened in real systems.
* Engineering knowledge — validated learning that can be reused.
* Engineering Intelligence — systems that consume this knowledge together with repository and operational context to analyze, reason, and support controlled action.

###Repository boundaries

Relvanta deliberately separates engineering intent from the mechanisms that implement it.

relvanta/.github
    GitHub-specific organization behavior
relvanta/standards
    Engineering intent, knowledge and standards
relvanta/infra
    Private infrastructure and technical enforcement
Product repositories
    Product-specific implementation
Experimental repositories
    Research, prototypes and architectural experiments

For example, a standard may say that a production service must expose an appropriate health signal.

The infrastructure repository may provide CI/deployment mechanisms that enforce or support that requirement, while an individual product implements the actual health endpoint.

The standard therefore remains independent of the mechanism.

Technology neutrality

Technology choices are implementation decisions unless deliberately elevated into a durable standard.

This repository should therefore avoid making philosophy dependent on:

* a particular programming language
* an AI provider or model
* an orchestration framework
* a vector database
* a cloud provider
* Kubernetes
* a monorepo
* a specific CI/CD provider

A useful distinction is:

PRINCIPLE
    ↓
REQUIREMENT
    ↓
ARCHITECTURAL DECISION
    ↓
TECHNOLOGY CHOICE

The lower layers may change without invalidating the higher ones.

Current foundation

The initial foundation consists of:

* Engineering Philosophy⁠￼
* Engineering Principles⁠￼
* Knowledge Model⁠￼
* Engineering Intelligence⁠￼
* Project Card Schema⁠￼
* Publishing Stages⁠￼

The project-card and publishing-stage concepts are retained because they form part of Relvanta’s emerging shared vocabulary.

They should evolve through actual use rather than being over-designed in advance.

How standards evolve

A proposed standard should normally emerge from evidence:

Problem / Question
       ↓
Experiment or Implementation
       ↓
Observation
       ↓
Evaluation
       ↓
Learning
       ↓
Documented Knowledge
       ↓
Standard (when justified)
       ↓
Automation (when valuable)

Not every idea becomes a standard.

Experiments may remain experimental, be rejected, or produce a more useful principle than the original proposal.

Engineering Intelligence

Engineering Intelligence is a consumer of this repository, not its replacement.

Standards answer:

What should we do?

Engineering Intelligence helps answer:

What is happening, what does it mean, what evidence supports that interpretation, and what should we consider doing?

The intelligence system should combine standards with:

* repository context
* historical context
* operational evidence
* deterministic analysis
* AI-assisted reasoning

Scope discipline

Do not add a document here simply because it sounds useful.

Before introducing a new standard, ask:

1. What recurring engineering problem does it address?
2. What evidence justifies it?
3. Is it durable enough to apply across repositories?
4. Can the expectation be stated clearly?
5. Should it be enforced, automated, or merely documented?
6. What trade-offs does it introduce?
7. What would make us reconsider it?

The standards repository should remain small enough that engineers can understand it and systems can consume it.

Status

This repository is intentionally at an early foundational stage.

More detailed standards should be added incrementally as Relvanta’s products, infrastructure, and experiments provide evidence for them.
