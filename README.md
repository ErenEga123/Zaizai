# Zaizai — Kairen-Centered Writing Agent System

Zaizai is an agent-oriented workspace for one book, built around the story of Kairen Voss. It tracks Kairen and **every character who actually interacts with him**. This is a dynamic inclusion rule, not a fixed cast list.

## Scope boundary

- Kairen Voss is the central reference character.
- A character enters the tracked cast when they directly interact with Kairen in the story or have a consequential, explicitly established interaction with him.
- The tracked cast may grow as the story develops. There is no hard-coded whitelist or maximum.
- Characters with no established interaction with Kairen do not receive individual dossiers and are not independently tracked.
- Incidental mentions, background crowds, and unrelated characters do not create character records.
- If a previously untracked character begins interacting with Kairen, create a record from that point and capture only relevant established history. Do not invent a biography.
- Track the interaction itself and its consequences for Kairen and the other participant.

## Authority

The author is the only canon authority. Agents may retrieve, analyze, plan, draft, and audit. They may propose facts and state changes, but cannot approve them or write them into authoritative canon. The repository is the source of truth, not chat memory.

## Agent pipeline

1. **Supervisor** routes the task and enforces approval gates.
2. **Archivist** retrieves relevant source material and tracked-cast records.
3. **Interaction Mapper** identifies which characters have established interactions with Kairen and updates the proposed tracked-cast scope.
4. **Continuity Analyst** checks chronology, causality, locations, conditions, resources, and relationships.
5. **Knowledge Auditor** checks what Kairen and each interacting character know, when, and how.
6. **Planner** creates causal scene beats.
7. **Writer** drafts from the approved brief.
8. **Canon Auditor** checks the draft against approved records.
9. **Developmental Editor** checks motivation, pacing, voice, and prose.
10. **Supervisor** consolidates findings and submits any canon/state changes for author approval.

These are logical roles orchestrated by ChatGPT in sequence. They are not autonomous background processes.

## Repository map

- `SYSTEM/` — architecture, workflow, writing protocol, quality gates.
- `AGENTS/` — specialist role contracts.
- `CANON/` — author-approved facts about Kairen and the tracked interacting cast.
- `STATE/` — timeline, current character states, relationships, and open threads relevant to Kairen and those interactions.
- `MANUSCRIPT/` — chapter drafts and approved text.
- `WORK/` — briefs, audit reports, and proposed changes; never canon by default.
- `SCHEMAS/` — data contracts.
- `TEMPLATES/` — scene briefs and reports.
- `DECISIONS/` — explicit author decisions.

## Record statuses

- `CANON`: author-approved.
- `PROPOSED`: awaiting author approval.
- `UNKNOWN`: not established.
- `CONTRADICTED`: approved sources disagree.

## First-use rule

Do not invent story facts or populate character dossiers from assumptions. Import the author's existing source material, identify all established Kairen interactions, flag conflicts, and present the proposed initial tracked-cast register for author approval.

## Implementation status

The current system uses ChatGPT as the orchestrator and specialist roles as bounded procedures. Repository-backed prompts and templates support the workflow; no autonomous runtime or background agents are claimed.
