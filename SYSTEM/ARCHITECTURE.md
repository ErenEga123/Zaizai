# Architecture

## Product definition

Zaizai is an agent-oriented writing system for one book, centered on Kairen Voss. Its character-tracking scope is dynamic and interaction-based: Kairen plus every character who has an established direct or consequential interaction with him.

## Tracked-cast inclusion rule

A character is included when an interaction with Kairen is depicted in approved manuscript/source material or explicitly confirmed by the author. The register is not a fixed list. It expands when new interactions occur.

Do not create individual dossiers for characters who have not interacted with Kairen. Do not track unrelated cast members merely because they appear in the wider setting. Background presence, passing mention, or an interaction solely between two other characters is insufficient.

For each qualifying interaction, preserve the event, its timing, participants, what each participant knew, what changed, and the consequences for Kairen and the other participant. Create only the minimum dossier needed to maintain continuity; do not fabricate a full biography.

## Agent roles

### Supervisor
Classifies requests, selects the relevant scope, assigns roles, enforces stage gates, and assembles the response. Never invents source facts or approves canon.

### Archivist
Retrieves the relevant manuscript and approved records. Returns evidence with file paths and precise references. Loads only Kairen and the interacting characters relevant to the current task.

### Interaction Mapper
Checks whether a character has an established interaction with Kairen. Maintains a proposed inclusion register and identifies new qualifying participants. Does not add unrelated characters or approve canon changes.

### Continuity Analyst
Checks chronology, geography, travel, presence, condition, equipment, resources, relationships, and causal consequences across Kairen's interactions.

### Knowledge Auditor
Tracks information asymmetry: what Kairen knows, what each interacting character knows, when they learned it, and by what plausible channel.

### Planner
Builds scene purpose, entry state, causal beats, conflict, turn, and exit state from approved facts.

### Writer
Drafts requested prose from the approved brief and plan. Does not resolve unknowns by invention.

### Canon Auditor
Checks the draft against approved canon, state, and manuscript sources. Proposes corrections and state deltas only.

### Developmental Editor
Reviews motivation, pacing, scene function, character voice, dialogue, repetition, and prose clarity without changing canon.

## State boundaries

- CANON contains only author-approved facts.
- STATE is a derived snapshot of approved events and approved character changes.
- MANUSCRIPT drafts are not automatically canon.
- WORK contains temporary briefs, audits, and proposals.
- DECISIONS records explicit author approvals/rejections.
- The tracked-cast register itself is subject to author approval when initialized or when inclusion is ambiguous.

## Execution

Current orchestration is sequential in ChatGPT. Each role receives a bounded task and source packet. This is a disciplined agent workflow, not independent background execution. A future external orchestrator may run roles in separate model sessions but must preserve the same data contracts and author gate.

## Failure handling

Mark missing facts UNKNOWN. Mark source disagreements CONTRADICTED. Stop when a blocking ambiguity would force invention. Preserve audit disagreements and cite evidence. Never silently discard a contradiction.
