# Architecture

## Operating model

Zaizai uses a supervised multi-agent pipeline for a single book. Agents are specialized reasoning roles, not independent authorities. The Supervisor owns task routing and quality gates; the author owns canon.

## Components

### Supervisor
Interprets the request, selects scope, assigns roles, tracks stage status, handles retries, and assembles the deliverable. It must not invent missing source facts.

### Archivist
Retrieves the minimum sufficient context from CANON, STATE, and MANUSCRIPT. Every factual item in its context packet carries a file path and, where possible, a heading or line range.

### Analysis agents
Continuity Analyst, Knowledge Auditor, and Canon Auditor operate independently against the same approved source packet. They report findings; they do not edit canon.

### Creative agents
Planner converts the request and context into scene beats. Writer produces prose from the approved brief and beats. Developmental Editor reviews narrative effectiveness and style.

### Author gate
Any change to canon, character state, timeline, relationship, resource inventory, or open-thread status is a proposal until the author explicitly approves it.

## State boundaries

- CANON is immutable to agents.
- STATE is a derived representation of canon and approved events; updates require author approval.
- MANUSCRIPT may contain drafts, but a draft is not automatically an approved event.
- WORK is disposable working material and has no canonical authority.
- DECISIONS records explicit author approvals and rejections.

## Execution modes

**Chat orchestration (current):** ChatGPT invokes the roles sequentially in one conversation, reading the repository before each task. This is not true parallel execution and does not run in the background.

**External orchestration (future):** a small application may call separate model sessions for each role, pass validated JSON packets, and enforce stage transitions. It must preserve the same authority model and repository contracts.

## Failure handling

If a required source is missing, mark it UNKNOWN. If sources conflict, mark CONTRADICTED and stop dependent decisions. If an audit finds a blocking defect, return to Writer or Planner. Never silently discard a finding.
