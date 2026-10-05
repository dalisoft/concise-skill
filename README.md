# Minimal Change

One portable Agent Skills package combining focused, low-overhead project work with an explicitly requested workflow for initializing or reconciling durable agent guidance.

The skill body is provider-neutral. It uses only the tools available in the current environment; it cannot grant missing filesystem access, tools, or model capabilities.

## Per-project installation

Add this repository as a submodule in the project where the skill should be available:

```sh
git submodule add git@github.com:dalisoft/concise-skill.git .agents/skills/minimal-change
git submodule update --init --recursive
```

The skill is then at `.agents/skills/minimal-change/SKILL.md`. Commit the submodule entry so teammates can initialize it with `git submodule update --init --recursive` or clone the project with submodules enabled.

## Harness discovery

These project locations are documented discovery paths for the same skill package:

| Harness | Project skill path | Extra setup |
| --- | --- | --- |
| Codex | `.agents/skills/minimal-change/SKILL.md` | None |
| OpenCode | `.agents/skills/minimal-change/SKILL.md` | None |
| Antigravity | `.agents/skills/minimal-change/SKILL.md` | None |
| Factory Droid | `.agents/skills/minimal-change/SKILL.md` | None |
| Command Code | `.agents/skills/minimal-change/SKILL.md` | None |
| Claude Code | `.claude/skills/minimal-change/SKILL.md` | Add the relative symlink below |

For Claude Code, which uses `.claude/skills`, point its project skill path at the canonical package:

```sh
mkdir -p .claude/skills
ln -s ../../.agents/skills/minimal-change .claude/skills/minimal-change
```

If symlinks are unavailable, install the same repository directly at `.claude/skills/minimal-change` and keep it updated from the canonical source.

Use each environment's skill picker or invocation method to load the skill. If it does not appear, check the path, repository permissions, and the current environment's skill discovery settings. The discovery paths are documented, but this repository has not been runtime-tested in every environment.

## Documentation

- [Codex skills](https://developers.openai.com/codex/skills)
- [OpenCode skills](https://opencode.ai/docs/skills)
- [Claude Code skills](https://code.claude.com/docs/en/skills)
- [Antigravity skills](https://antigravity.google/docs/skills?app=antigravity-ide)
- [Factory Droid skills](https://docs.factory.com/harness/skills)
- [Command Code skills](https://commandcode.ai/docs/skills)
