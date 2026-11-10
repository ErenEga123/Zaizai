# Zaizai — Writing System

Zaizai is a single-book writing workspace built around a hybrid workflow: ChatGPT performs creative work, while repository-backed canon, explicit state records, and repeatable continuity checks constrain that work.

## Non-negotiable rules

- The author is the sole authority on canon. Nothing becomes canon merely because an assistant proposed or wrote it.
- The repository is the source of truth. Conversation memory is never authoritative.
- Separate established facts, hypotheses, proposals, and unresolved questions.
- Track what each character knows at a specific point in the timeline; never grant knowledge by authorial convenience.
- Every consequential event must produce explicit state changes and downstream consequences.
- Draft first, validate second, revise third. Do not silently hide unresolved contradictions.
- Preserve the author's voice and requested scope. Do not pad scenes or invent plot resolutions to fill gaps.

## Workflow

1. Read `SYSTEM/WORKFLOW.md` and `SYSTEM/WRITING_PROTOCOL.md`.
2. Load only the canon files and chapter records relevant to the requested scene, plus global constraints.
3. Prepare a scene brief and continuity assumptions. Ask the author only about blocking ambiguities.
4. Draft the requested text.
5. Run the continuity review defined in `SYSTEM/CONTINUITY_CHECK.md`.
6. Report findings separately: confirmed contradictions, likely issues, and author decisions required.
7. Apply accepted corrections. Update canon proposals in `WORK/PROPOSED_CANON_CHANGES.md`; do not silently edit authoritative canon.
8. The author explicitly approves canon changes. Only then are canonical records updated.

## Repository map

- `SYSTEM/` — operating rules and review procedure.
- `CANON/` — author-approved facts for this book.
- `CHAPTERS/` — chapter drafts and approved text.
- `WORK/` — temporary briefs, continuity reports, and proposed changes.
- `TEMPLATES/` — reusable chapter, character, event, and scene formats.

## Current status

The workspace is initialized. No story canon has been invented or imported. Populate canon from the author's source material before drafting story-specific scenes.
