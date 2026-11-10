# Zaizai Agent Architecture

## Product boundary
One book. Tracked focus character: Kairon Voss, an original secondary character added to the existing story. This tracking focus does not make him the original story's protagonist. Tracked cast: Kairon plus every character with an evidenced direct or consequential interaction with him. This is a dynamic set. Unrelated characters receive no dossiers or independent tracking.

## Orchestration
The Supervisor executes a staged pipeline. In the current implementation these are logical specialist roles run sequentially by ChatGPT, not independent background model processes.

## Roles
- Supervisor: classifies task, routes roles, enforces approval gates, assembles delivery.
- Archivist: retrieves minimal sufficient repository context with evidence paths.
- Interaction Mapper: detects qualifying Kairon interactions and proposes new tracked-cast entries.
- Planner: builds causal scene beats from approved context.
- Writer: drafts prose from approved brief and plan.
- Continuity Analyst: checks time, place, presence, physical/logistical state, causality.
- Knowledge Auditor: checks information boundaries for Kairon and interacting characters.
- Canon Auditor: checks draft against approved sources and proposes state deltas.
- Developmental Editor: reviews motivation, pacing, voice, scene function, and prose.

## Pipeline
Intake -> Retrieve -> Interaction-scope check -> Preflight -> Plan -> Draft -> Independent audits -> Revise -> Deliver -> Propose state changes -> Author approval -> Commit.

## Data ownership
CANON and approved chapters are the source of truth. WORK files are non-canonical. A generated draft does not prove that an event occurred. Only explicit author approval can change canon, state, or the tracked-cast register.

## Interaction inclusion test
A character qualifies when an approved source depicts or the author explicitly confirms a direct or consequential interaction with Kairon: dialogue, physical contact, coordinated action, conflict, information exchange, a decision that materially affects the other, or a relationship-changing event. Mere co-presence, passing mention, and interaction only with third parties do not qualify.

## Context packet
Each task packet includes Kairon's current approved state; only relevant interacting-character records; timeline slice; knowledge boundaries; relationship state; relevant resources/equipment; active consequences; source references; and unknown/conflicting facts.

## Failure policy
Never fill missing facts with invention. Mark UNKNOWN. Mark incompatible sources CONFLICT. Stop on blockers. Keep disagreements visible.
