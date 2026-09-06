Relvanta Publishing Stages

Purpose

Publishing Stage describes the maturity and intended reuse state of a Relvanta project, experiment, capability, or piece of engineering knowledge.

It answers:

How far has this idea or implementation progressed, and what should others reasonably expect from it?

A publishing stage is not a quality score.

It communicates the level of confidence, validation, stability, and intended reuse that currently exists.

⸻

Core Principle

Relvanta distinguishes between:

* what is imagined
* what is being explored
* what has been implemented
* what has been validated
* what is intentionally reused
* what is publicly published

These states should not be conflated.

A project can be technically sophisticated while still being experimental.

A simple project can be highly validated and reusable.

Therefore:

Complexity does not determine maturity. Evidence and intended use do.

⸻

Stage Model

IDEA
  ↓
EXPERIMENT
  ↓
PROTOTYPE
  ↓
VALIDATED
  ↓
INTERNAL
  ↓
PRODUCT
  ↓
PUBLISHED

Progression is not necessarily linear.

Projects may:

* remain at a stage indefinitely
* move backwards
* branch into multiple projects
* be abandoned
* produce knowledge without becoming products
* skip stages when sufficient evidence already exists

The stages describe the current state, not a mandatory development process.

⸻

1. IDEA

Definition

A concept, hypothesis, problem, opportunity, or proposed direction that has not yet received meaningful implementation or validation.

Characteristics

* intent may be clear or incomplete
* assumptions may be largely untested
* implementation may not exist
* evidence is limited or absent
* exploration is the primary purpose

Expectations

Ideas should not be treated as validated engineering knowledge.

Claims about feasibility, usefulness, performance, or reliability should be understood as hypotheses.

Typical outputs

* concept documents
* sketches
* architectural hypotheses
* problem statements
* research questions

⸻

2. EXPERIMENT

Definition

An idea is actively being investigated through implementation, testing, research, or observation.

Characteristics

* a specific question or hypothesis exists
* implementation may be incomplete
* experimentation is intentional
* results may be positive, negative, inconclusive, or unexpected

Expectations

Experimental work is allowed to fail.

The primary output is knowledge, not necessarily software.

Typical outputs

* proof of concept
* technical experiment
* benchmark
* feasibility study
* architectural experiment
* failed approach with documented learning

⸻

3. PROTOTYPE

Definition

A working implementation exists and is sufficiently coherent to demonstrate a concept or intended experience.

Characteristics

* meaningful functionality exists
* the system can be demonstrated or tested
* architecture may still change substantially
* reliability and operational characteristics may be incomplete
* production suitability has not necessarily been established

Expectations

A prototype should not automatically be treated as production-ready.

Its purpose is to reduce uncertainty and enable evaluation.

Typical outputs

* functional prototype
* MVP candidate
* demonstrator
* experimental application
* early product implementation

⸻

4. VALIDATED

Definition

The project, capability, or approach has accumulated sufficient evidence to support the specific claims being made about it.

Validation is always contextual.

A project may be validated for one purpose while remaining unvalidated for another.

For example:

Validated:
"Works for the tested input set."
Not necessarily validated:
"Works reliably for all production workloads."

Characteristics

* important assumptions have been tested
* relevant behavior has been observed
* evidence is documented
* known limitations are understood
* confidence is substantially higher than during experimentation

Expectations

Validation claims should identify their scope.

Validation does not automatically imply production readiness.

Typical outputs

* validated architecture
* validated algorithm
* validated workflow
* validated library
* validated engineering pattern

⸻

5. INTERNAL

Definition

A validated capability intentionally used within Relvanta or its internal engineering ecosystem.

Characteristics

* intended users or consumers are known
* operational expectations exist
* maintenance responsibility is understood
* reuse is intentional
* limitations are sufficiently understood for the intended context

Expectations

Internal software may still evolve rapidly.

Internal does not mean production-grade for arbitrary external consumers.

Typical outputs

* internal platform capability
* reusable internal tool
* engineering service
* shared library
* internal workflow

⸻

6. PRODUCT

Definition

A project intentionally developed and maintained as a user-facing Relvanta product or product capability.

Characteristics

* a defined user or customer exists
* product intent is explicit
* operational and maintenance responsibilities exist
* reliability expectations are defined
* product-specific requirements are understood

Expectations

Product status implies intentional ownership and continued evolution.

It does not imply that every product is mature or commercially successful.

⸻

7. PUBLISHED

Definition

A project, capability, pattern, or body of knowledge has been intentionally exposed for external consumption.

Publication may mean:

* open-source release
* public documentation
* public specification
* public engineering pattern
* published research
* publicly reusable tool

Characteristics

* external consumers are expected
* documentation is sufficient for the intended audience
* licensing or publication constraints are understood
* security and privacy considerations have been evaluated
* known limitations are communicated

Expectations

Published does not necessarily mean production-grade.

A published experiment can remain explicitly experimental.

⸻

Stage vs Status

Publishing Stage and Project Status are different dimensions.

Stage

Describes maturity and intended reuse.

Status

Describes whether work is currently active.

For example:

stage: prototype
status: active

means an actively developed prototype.

Whereas:

stage: validated
status: maintenance

means a validated capability that is no longer undergoing significant development.

And:

stage: experiment
status: archived

means an experiment that has ended but remains part of the engineering history.

⸻

Stage vs Confidence

Stage should not be interpreted as a universal confidence score.

Confidence belongs to specific claims.

For example:

Stage: PROTOTYPE
Claim:
"The architecture can process 10,000 events/minute."
Confidence:
High
Evidence:
Benchmark performed under documented test conditions.
Claim:
"The architecture is suitable for production."
Confidence:
Low
Evidence:
No production deployment yet.

This distinction prevents maturity labels from hiding uncertainty.

⸻

Stage Transitions

A stage transition should have a reason.

Where practical, the transition should be supported by evidence.

Example:

IDEA
  │
  │ question identified
  ▼
EXPERIMENT
  │
  │ working implementation
  ▼
PROTOTYPE
  │
  │ hypothesis tested
  ▼
VALIDATED
  │
  │ intentional internal reuse
  ▼
INTERNAL

A transition does not require success in every dimension.

It requires sufficient evidence that the project has changed state in a meaningful way.

⸻

Failed Experiments

Failure does not invalidate an experiment.

An experiment may produce valuable engineering knowledge even when its intended hypothesis is rejected.

For example:

Experiment
    ↓
Hypothesis rejected
    ↓
Approach documented
    ↓
Reason understood
    ↓
Knowledge retained

Such a project may remain:

stage: experiment
status: archived

while the resulting knowledge becomes part of Relvanta’s reusable engineering knowledge.

⸻

Knowledge Can Advance Independently

The publishing stage applies to the project or artifact being classified.

Knowledge produced by that project may have a different maturity.

For example:

Project:
stage = experiment
Knowledge:
"Pattern X consistently caused race conditions."
Knowledge status:
validated

This distinction is important.

Relvanta should be able to preserve useful knowledge from unfinished or abandoned projects.

⸻

Reclassification

Stages are not permanent.

A project may move:

PROTOTYPE → EXPERIMENT

if new evidence invalidates important assumptions.

Or:

INTERNAL → VALIDATED

if its internal implementation is no longer actively maintained but its underlying pattern remains validated.

Projects may also be archived without losing their historical knowledge.

⸻

What Stage Does Not Mean

A stage does not automatically guarantee:

* security
* reliability
* performance
* scalability
* correctness
* production readiness
* commercial viability

Those properties require their own evidence.

The stage communicates context, not certification.

⸻

Relationship to Project Cards

Project Cards reference the publishing taxonomy through the stage field.

Example:

name: example-project
type: experiment
status: active
stage: experiment

The Project Card records the project’s context.

This document defines the meaning of its stage.

⸻

Relationship to Engineering Intelligence

Publishing stages provide Engineering Intelligence with an important contextual signal.

An intelligence system should reason differently about:

IDEA

than:

VALIDATED

and differently again about:

PRODUCT

For example:

IDEA
→ challenge assumptions aggressively
EXPERIMENT
→ focus on evidence and learning
PROTOTYPE
→ identify technical and architectural risks
VALIDATED
→ evaluate reuse and generalization
INTERNAL
→ evaluate operational impact
PRODUCT
→ evaluate user, reliability, security, and maintenance impact
PUBLISHED
→ evaluate external usability, documentation, security, and compatibility

The stage therefore becomes contextual information rather than merely a label.

⸻

Governance

The taxonomy should remain small.

A new stage should only be introduced when existing stages cannot express an important distinction required by real projects.

Stages should not be added merely to represent every possible project state.

The governing principle is:

A taxonomy exists to improve understanding, not to create administrative overhead.

⸻

Initial Vocabulary

The initial publishing-stage vocabulary is:

idea
experiment
prototype
validated
internal
product
published

Project status remains separate:

idea
active
paused
maintenance
deprecated
archived

Both vocabularies may evolve as Relvanta gains experience.
