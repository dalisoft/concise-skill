---
name: minimal-change
description: Make focused, correct code and file changes with minimal scope, duplication, and cleanup. Use for coding, setup, file transformations, dependency fixes, and repository cleanup. Use the durable agent-guidance workflow only when explicitly asked to create or reconcile project instructions and state files.
---

# Minimal change

Deliver the requested result with the smallest clear, maintainable change. Optimize correctness and clarity, not line count; do not code-golf or remove necessary checks.

## Focused work

- Identify the deliverable and actual project root. Read applicable project guidance, including parent instructions and `AGENTS.override.md`, then inspect the target and relevant callers.
- Edit the owning files in place. Preserve user changes, existing behavior, and project style. Add files, dependencies, wrappers, or abstractions only when requested or required.
- Keep research, validation, and cleanup proportional to the request. Avoid speculative refactors, optional follow-up work, and duplicate variants. Ask before making an assumption that could materially change scope or behavior.
- Use available tools and their declared interfaces. Do not write standalone Python or JavaScript for edits, searches, or analysis unless asked. Run code and checks when they materially improve correctness; prefer existing project commands.
- Preserve existing Git work. Do not reset, clean, stash, or create backups for convenience. Commit or publish only when requested.
- Remove only exact, verified task-created leftovers. Do not use broad deletion. Stop task-owned processes and resolve delegated work before finishing.
- Run the smallest meaningful check, inspect the final diff, and report what was actually changed and verified. Distinguish verified results from assumptions or blocked checks.

## Project guidance

For project setup or editing, follow existing guidance. If the actual project root has no applicable `AGENTS.md`, create one concise file with verified project structure, commands, and durable rules. Never replace existing guidance or create project files for chat-only answers.

## Durable agent-guidance setup

Only when explicitly asked to create, install, repair, or reconcile `AGENTS.md` or the related `.agents/` state files, read and follow [the agent-guidance protocol](references/agent-guidance-protocol.md). Do not inspect or rewrite those files for ceremony during ordinary work.
