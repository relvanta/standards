# My five-layer identity card format
Relvanta Project Card Schema

Purpose

A Project Card is the canonical identity and context record for a Relvanta project.

It provides a compact, structured description of what a project is, why it exists, what it is intended to become, what has been learned, and how confident we are in its current state.

A Project Card is not a README, technical specification, or project plan.

It exists to make project context understandable and reusable by:

* humans
* other Relvanta projects
* engineering workflows
* automation
* Engineering Intelligence

The Project Card should contain enough context to answer:

What is this, why does it exist, what is its current state, and what do we know about it?

⸻

Design Principles

1. Identity before implementation

The card describes the project’s purpose and identity before describing its technology.

2. Intent before execution

The reason a project exists is more important than how it currently happens to be implemented.

3. Evidence over assumption

Claims about maturity, capability, reliability, or validation should be supported by evidence where practical.

4. Current state must be distinguishable from intended state

A project may have ambitions that are not yet implemented.

The card must not represent planned capabilities as existing capabilities.

5. Technology is contextual

Technology choices may be recorded, but they do not define the project’s identity.

6. Knowledge should be reusable

The card should capture knowledge that may be useful beyond the project itself.

⸻

Schema

A Project Card consists of the following layers.

1. Identity

Basic identification of the project.

Field	Description
name	Project name
repository	Repository containing the project
type	Project classification
status	Current lifecycle status
stage	Publishing/maturity stage

Example:

name: txtr
repository: relvanta/txtr
type: product
status: active
stage: prototype

⸻

2. Intent

Describes why the project exists.

Field	Description
problem	Problem or opportunity being addressed
intent	What the project is intended to accomplish
users	Intended users or consumers
outcome	Desired outcome

The intent describes the reason for existence, not the implementation.

⸻

3. Current State

Describes what actually exists.

Field	Description
implemented	Capabilities currently implemented
architecture	Current architectural characteristics
technology	Important technology choices
limitations	Known limitations
unknowns	Important unresolved questions

This section should describe reality rather than aspiration.

⸻

4. Evidence

Records evidence supporting important claims about the project.

Field	Description
experiments	Experiments performed
observations	Important observations
validation	Validation performed
results	Relevant results
confidence	Confidence in important claims

Evidence may include:

* tests
* experiments
* benchmarks
* production observations
* user feedback
* operational data
* successful or failed prototypes
* documented investigations

⸻

5. Knowledge

Records what the project has taught Relvanta.

Field	Description
learnings	Important lessons
decisions	Significant engineering decisions
patterns	Reusable patterns discovered
invalidated	Assumptions or approaches shown to be ineffective
related_knowledge	Related standards, principles, or projects

This is one of the most important sections.

A project is not only an implementation. It can also be a source of engineering knowledge.

⸻

6. Relationships

Projects should be understood as part of a larger system.

Field	Description
depends_on	Projects or capabilities depended upon
used_by	Projects or systems consuming this project
related_to	Related projects
derived_from	Earlier projects or experiments
informs	Projects or standards influenced by this project

This allows project knowledge to form a graph rather than a collection of isolated documents.

⸻

Project Types

Project type describes the role a repository currently plays.

Suggested initial vocabulary:

* product
* platform
* library
* tool
* experiment
* research
* infrastructure
* documentation

This vocabulary may evolve.

A project should not be forced into a type merely for classification convenience. If classification is uncertain, that uncertainty should be explicit.

⸻

Status

Status describes the current operational state of the project.

Suggested values:

* idea
* active
* paused
* maintenance
* deprecated
* archived

Status describes activity, not maturity.

⸻

Stage

Stage describes how far the project or its ideas have progressed toward validated/reusable knowledge.

The authoritative stage taxonomy is defined separately in:

taxonomy/PUBLISHING_STAGES.md

Stage and status are intentionally separate.

For example:

status: active
stage: experiment

or:

status: maintenance
stage: validated

⸻

Minimal Project Card

A project does not need every field to be complete.

The minimum useful card is:

name:
repository:
type:
status:
stage:
problem:
intent:
outcome:
implemented:
limitations:
unknowns:
evidence:
learnings:
related_to:

Missing information should be left explicitly unknown rather than invented.

⸻

Extended Project Card

For projects where additional context is valuable:

name:
repository:
type:
status:
stage:
problem:
intent:
users:
outcome:
implemented:
architecture:
technology:
limitations:
unknowns:
experiments:
observations:
validation:
results:
confidence:
learnings:
decisions:
patterns:
invalidated:
related_knowledge:
depends_on:
used_by:
related_to:
derived_from:
informs:

⸻

Relationship to Other Relvanta Knowledge

The Project Card sits between projects and the broader engineering knowledge system.

                    ENGINEERING PHILOSOPHY
                              │
                              ▼
                         PRINCIPLES
                              │
                              ▼
                          STANDARDS
                              │
                              ▼
                    ARCHITECTURE / PATTERNS
                              │
                              ▼
                         PROJECT CARD
                              │
                 ┌────────────┼────────────┐
                 ▼            ▼            ▼
             Project       Evidence      Decisions
                 │            │            │
                 └────────────┼────────────┘
                              ▼
                    ENGINEERING KNOWLEDGE
                              │
                              ▼
                  ENGINEERING INTELLIGENCE

The Project Card therefore acts as a context boundary around an individual project.

It provides Engineering Intelligence with structured information about:

* project intent
* project identity
* current state
* evidence
* uncertainty
* decisions
* relationships
* accumulated knowledge

⸻

Evolution

The schema is intentionally small in its first version.

Fields should be added when real projects demonstrate a recurring need for information that cannot otherwise be represented clearly.

The schema should not grow merely because additional metadata is theoretically possible.

The governing principle is:

Capture information because it enables understanding, reasoning, validation, reuse, or action.

⸻

Relationship to README Files

A Project Card does not replace a README.

The two serve different purposes.

README

Optimized for people approaching a repository.

Answers:

How do I understand, use, run, or contribute to this project?

Project Card

Optimized for maintaining project identity and engineering context.

Answers:

What is this project, why does it exist, what do we know about it, and how does it relate to the rest of Relvanta?

A project may therefore have both.

⸻

Schema Governance

The schema itself is part of Relvanta’s engineering knowledge.

Changes should be driven by demonstrated needs from real projects.

When the schema changes, consideration should be given to:

* backwards compatibility
* existing Project Cards
* automation consuming the schema
* Engineering Intelligence
* documentation
* migration requirements

The schema should evolve deliberately rather than becoming an accumulation of arbitrary metadata.
