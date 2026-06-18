# Contributing to Claude Code Dev Studio

Thanks for being here. This studio gets better when people who actually build
with it report what works, what breaks, and what's missing. You don't need to be
an expert in Claude Code internals to help.

## Ways to contribute

- **Report a bug** — a command that misfires, an agent that goes off the rails, a
  hook that fails. Use the Bug Report issue template.
- **Request a feature** — a new agent, command, skill, or track. Use the Feature
  Request template.
- **Improve an agent or skill** — sharpen a prompt, fix a coordination handoff,
  add a missing pattern.
- **Add a track or template** — if you've built something the existing tracks
  don't cover well, a new `templates/<type>/CLAUDE.md` is welcome.
- **Improve docs** — the fastest path to a first contribution.

If you're not sure whether something fits, open a
[Discussion](../../discussions) before writing code.

## Before you start

1. Search [existing issues](../../issues) and
   [Discussions](../../discussions) — someone may already be on it.
2. For anything larger than a typo or a single-agent tweak, open an issue or
   Discussion first so we can agree on direction before you invest time.

## Making a change

The studio is plain Markdown and a few shell/Node hooks — there's no build step.

1. Fork the repo and create a branch: `git checkout -b fix/agent-handoff`.
2. Make your change. Keep the existing structure:
   - **Agents** live in `.claude/agents/` — one `.md` per agent, with the
     standard frontmatter (`name`, `description`, `tools`, `model`).
   - **Commands** live in `.claude/commands/` — one `.md` per command.
   - **Skills** live in `.claude/skills/<skill-name>/SKILL.md`.
   - **Rules** live in `.claude/rules/` and are path-scoped.
   - **Hooks** live in `.claude/hooks/scripts/`.
3. **Test it in a real session.** Clone your branch, open `claude`, and run the
   command or trigger the agent you changed. Describe what you tested in the PR.
4. If you changed counts (added an agent/command/skill) update the matching
   numbers in `README.md` — they're easy to leave stale.
5. Add an entry to `CHANGELOG.md` under `## [Unreleased]`.

## Conventions

- **Match the prose register of the existing files** — direct, prescriptive,
  second-person. Agents tell the user what to do next and why.
- **Collaborative, not autonomous** — every significant action follows
  Question → Options → Decision → Draft → Approval → Execute. New commands and
  agents should respect this (see `docs/COLLABORATIVE-DESIGN-PRINCIPLE.md`).
- **One concern per agent.** If an agent is doing two jobs, it's probably two
  agents.
- Commit messages: `type: short summary` (`feat:`, `fix:`, `docs:`,
  `refactor:`). Reference the issue when there is one.

## Opening the PR

- Fill in the PR template.
- Link the issue it closes (`Closes #123`).
- Note what you tested and in what kind of project (track, stack).

By contributing, you agree your contributions are licensed under the repo's
[MIT License](LICENSE).
