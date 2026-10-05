# Repository guidance

- This repository packages one portable skill. Keep `SKILL.md` provider-neutral; put installation details in `README.md`.
- Keep the agent-guidance protocol conditional and referenced from `SKILL.md`; avoid duplicating it in the entrypoint.
- This instructions-only package has no runtime dependencies or project test suite. Validate skill metadata, reference paths, install paths, and the final diff after edits.
