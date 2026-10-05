# Agent-guidance protocol

Read this reference only when the user explicitly asks to initialize, install, repair, or reconcile durable project-agent guidance.

## Required project record

At the actual project root, maintain one `AGENTS.md` plus these four related files:

- `.agents/mistakes.md`: verified recurring failure patterns and how to prevent them.
- `.agents/todo.md`: pending, in-progress, verified-complete, and blocked work.
- `.agents/track.md`: current goal, scope, facts, next action, blockers, and evidence.
- `.agents/consistency.md`: stable user and project invariants.

Treat these files as one normalized record. Keep each fact in its owning file; cross-reference stable IDs rather than duplicating prose. Update all affected files together, replace stale checkpoints, and do not make them append-only logs.

## Initialization and reconciliation

1. Locate the actual project root and read its applicable instructions, parent guidance, and existing record before editing.
2. Preserve existing rules. Current, specific instructions supersede older, general ones, subject to higher-priority system, safety, and current user instructions.
3. Use only durable, relevant, non-sensitive facts available in the current environment. Do not invent unavailable history or persist secrets, personal data, raw transcripts, large logs, generated output, or temporary implementation noise.
4. Create missing files with the minimal schemas below. Merge into existing files in place; never reset them to templates or duplicate already-recorded facts.
5. Read back changed files, verify required paths and cross-file consistency, review the diff, and safely clean up only verified task-created leftovers.

If history or files are unavailable, say what could not be inspected. If editing is unavailable, return a proposed patch and clearly state that nothing was written.

## Compact `AGENTS.md` contract

Adapt this contract to the project and merge it with existing instructions rather than replacing them:

```markdown
# Agent operating contract

## Context and continuity

Before work, after context loss, or after switching models, read this file,
`.agents/track.md`, and `.agents/todo.md`. Read `.agents/consistency.md` and
`.agents/mistakes.md` when the task touches their recorded rules. Before
changing this operating record, read all four state files.

Keep parent work visible across follow-ups. Use linked `T-###` IDs for
material concurrent tasks, and keep parent and child status synchronized.
Authorization for one task does not authorize another.

## Scope and change economy

Identify the requested deliverable and do only the work needed to complete
and proportionately verify it. Inspect and edit the owning files in place.
Preserve user work and existing behavior. Avoid speculative research,
refactoring, dependencies, scaffolding, duplicate copies, and optional
follow-up work. Ask before a materially behavior-changing assumption.

Use available tools and declared interfaces. Do not write standalone
Python/JavaScript helpers for edits, searches, or analysis unless requested.
Preserve Git work; do not use destructive reset or broad cleanup shortcuts.

## Record ownership

- `track.md`: current goal, scope, relevant facts, next action, blockers, and
  evidence. Use `NEED:` for a positive requirement and link related prevention
  rules where useful.
- `todo.md`: active, blocked, and recently verified work. Use `[ ]` pending,
  `[~]` in progress, `[x]` complete with evidence, and `[!]` blocked with the
  concrete blocker. Keep the parent active until its deliverable is verified.
- `mistakes.md`: verified recurring failures, their cause, impact, correction,
  and prevention. When the user corrects the same durable failure pattern for
  the third time, ask exactly: `ADD THIS MISTAKE?` Do not record speculation.
- `consistency.md`: stable preferences and project invariants: terminology,
  style, minimalism, structure, architecture, privacy, and verification.

## Execution and verification

Refresh relevant state before acting. After a failure, compare expected and
actual state before retrying; do not repeat an unchanged failing action. Run
the smallest meaningful check and distinguish verified behavior from
inference or blocked work. Never claim a read, edit, test, or tool call
succeeded without evidence.

Before finalizing changed work, verify the requested outcome, reconcile
`todo.md` with `track.md`, and review the diff and task-created artifacts.
Remove only exact, verified throwaways; stop task-owned processes and resolve
delegated work. Preserve user data and retained evidence. If safe ownership or
recovery is unclear, leave the item and report it. Keep cleanup notes in chat.
For answer-only work that changes no project state or durable memory, do not
rewrite or reread every state file solely for ceremony.
```

## Minimal state schemas

Create headings and status only; do not manufacture history.

### `.agents/track.md`

```markdown
# Track

## Current
- Goal: none
- Scope: none
- Next action: none
- Blockers: none

## Relevant facts
- None.

## Evidence
- None.
```

### `.agents/todo.md`

```markdown
# Todo

## Active
None.

## Blocked
None.

## Recently verified
None.
```

### `.agents/mistakes.md`

```markdown
# Mistakes

No verified durable mistakes recorded.
```

### `.agents/consistency.md`

```markdown
# Consistency

No additional stable invariants recorded.
```

## Size and completion discipline

Keep `AGENTS.md` compact and the state files current, deduplicated, and relevant. Load state by relevance during routine work; read all four for initialization, memory changes, or stateful finalization. Do not create a protocol report or duplicate guide.

Before declaring setup complete, verify all five paths, preserve existing rules, check linked tasks and statuses, and confirm no sensitive, duplicated, or noisy content was persisted. Report actual checks, remaining work, and verification limits concisely.
