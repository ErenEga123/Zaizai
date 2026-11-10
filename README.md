# Zaizai — Kairen-Centered Writing System

Zaizai is an agent-oriented writing workspace for one book. ChatGPT coordinates specialized roles; the repository preserves approved facts and manuscript state.

## Scope: Kairen Voss and his interacting cast

Zaizai tracks Kairen Voss and every character who has an established direct or consequential interaction with him. This is a dynamic set, not a fixed whitelist. A new character enters the tracked cast when such an interaction is established in approved source material or explicitly confirmed by the author.

Characters who have not interacted with Kairen do not receive individual dossiers or independent state tracking. A passing mention, background appearance, or interaction solely with another character does not qualify. For tracked characters, record only information relevant to continuity with Kairen: interactions, chronology, location when relevant, condition, equipment/resources when relevant, knowledge, relationship changes, and consequences. Do not invent biographies.

## Authority

The author is the sole authority on canon. Agents may retrieve, analyze, plan, draft, and audit, but cannot silently promote generated material into canon. The repository is the source of truth, not chat memory.

## Agent pipeline

Supervisor routes the task and enforces approval gates. Archivist retrieves relevant source context. Interaction Mapper checks the dynamic tracked-cast boundary. Planner creates causal beats. Writer drafts from the approved brief. Continuity Analyst, Knowledge Auditor, and Canon Auditor independently inspect the result. Developmental Editor reviews prose. Supervisor consolidates findings and submits canon/state changes for author approval.

These are logical roles orchestrated by ChatGPT in sequence; they are not autonomous background processes.

## Repository map

- `SYSTEM/` — architecture, workflow, writing protocol, continuity checks.
- `AGENTS/` — specialist role contracts.
- `CANON/` — approved facts about Kairen and his interacting cast only.
- `CHAPTERS/` — chapter drafts and approved text.
- `TEMPLATES/` — reusable records and briefs.
- `WORK/` — proposals and temporary reports; never canon by default.

## Canon statuses

CANON = author-approved. DERIVED = unavoidable consequence with cited premises. PROPOSAL = awaiting approval. UNKNOWN = not established. CONFLICT = approved sources disagree.

## First use

Import the author's existing materials, identify all evidenced interactions with Kairen, flag conflicts, and present the initial tracked-cast register for approval. Do not invent story facts or prepopulate character dossiers.

## Runtime status

ChatGPT currently orchestrates the specialist roles sequentially. This repository defines the agent contracts and quality gates; it does not claim to run autonomous background agents.
