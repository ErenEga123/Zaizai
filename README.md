# Zaizai — Single-Book Agentic Writing System

Zaizai is an agent-oriented writing workspace for one book. ChatGPT acts as the creative interface and agent runtime; specialized roles perform bounded tasks in a controlled sequence. The repository is the source of truth.

## Authority and safety rules

- The author is the sole authority on canon. No agent may promote a proposal or generated prose into canon.
- The repository, not chat memory, is authoritative.
- Agents must cite the exact repository records supporting continuity claims.
- Unknown information stays unknown. Agents must not fill gaps with confident invention.
- Track character knowledge at a specific point in the timeline.
- Consequential events require explicit state-delta proposals and downstream consequence checks.
- Drafting, auditing, and canon approval are separate stages.
- If a blocking contradiction cannot be resolved from approved material, stop and ask the author one focused question.

## Agent pipeline

1. **Supervisor** classifies the request, assigns agents, enforces gates, and assembles the final response.
2. **Archivist** retrieves relevant canon and manuscript context, returning a source-backed context packet.
3. **Continuity Analyst** identifies constraints, contradictions, timeline risks, and knowledge boundaries.
4. **Planner** creates scene beats and causal transitions.
5. **Writer** drafts only from the approved brief and beat plan.
6. **Canon Auditor** checks facts, chronology, locations, character states, relationships, resources, and open threads.
7. **Knowledge Auditor** checks who knows what, when, and from whom.
8. **Developmental Editor** checks pacing, motivation, scene function, voice, repetition, and prose.
9. **Supervisor** reconciles findings, requests revision when needed, and presents proposed canon changes separately.

These are logical agent roles. In this initial version they are orchestrated sequentially by ChatGPT using the role contracts in `AGENTS/`; independent background model processes are not yet implemented.

## Repository map

- `SYSTEM/` — architecture, operating rules, workflow, quality gates.
- `AGENTS/` — bounded role prompts and output contracts.
- `CANON/` — author-approved facts only.
- `STATE/` — current timeline, character states, relationships, open threads.
- `MANUSCRIPT/` — chapter drafts and approved text.
- `WORK/` — task briefs, reports, and proposed changes; never canon by default.
- `SCHEMAS/` — machine-readable contracts.
- `TEMPLATES/` — reusable briefs and reports.
- `DECISIONS/` — explicit author decisions.

## Canon statuses

- `CANON`: author-approved or explicitly established in approved source material.
- `PROPOSED`: agent suggestion awaiting author approval.
- `UNKNOWN`: not established by available sources.
- `CONTRADICTED`: approved sources disagree; requires resolution.

## First-use rule

Do not invent a book, characters, setting, or plot. Import the author's existing materials first, reconcile duplicates and conflicts, then ask the author to approve the initial canon baseline.

## Current implementation

The repository contains the agent architecture, role contracts, schemas, and operating workflow. Runtime orchestration is currently performed by ChatGPT; a separate executable orchestrator can be added later without changing canon ownership rules.
