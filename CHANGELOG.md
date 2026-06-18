# Changelog

All notable changes to Claude Code Dev Studio are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project aims to follow [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- `CONTRIBUTING.md`, issue templates, and a PR template.
- This changelog.

<!--
  NOTE: the git history references "v3" and "v4" feature sets, but the only
  tag is v1.0.0. Recommend collapsing those into a single tagged release
  (e.g. v2.0.0) and recording it below so users can tell what they're on.
-->

## [1.0.0] - 2026

Initial public release.

### Added
- **Studio Brain** — `/start` orchestration sequence taking a raw idea to a
  configured project (interview → challenge → track detection → documents →
  sprint roadmap).
- **Design phase** — `/design`, `/map-systems`, `/design-index` for taking an
  idea to a dependency-ordered sprint plan before writing code.
- **37 agents** across a three-tier hierarchy (Studio Brain → Directors →
  Department Leads → Specialists) covering software, game-dev, content, and
  research.
- **27 commands** spanning studio operations, sprints, building, quality, and
  knowledge management.
- **24 skills** that auto-load by file context (TDD, API design, SaaS/mobile/
  auth patterns, security review, systematic debugging, two-stage review, and
  engine-specific game-dev patterns).
- **Track system** — `software`, `game-dev`, `content`, `research`, and
  dynamically generated `custom:[name]` tracks.
- **Project + personal wiki** (Karpathy pattern) for compounding knowledge.
- **6 rescue prompts** for stuck-on-bug, scope-creep, handover, second-opinion,
  fresh-eyes, and session-reset moments.
- Hooks (dangerous-command guard, format-on-save, session start/end) and
  path-scoped rule sets.

[Unreleased]: https://github.com/marko-builds/Claude-Code-Dev-Studio/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/marko-builds/Claude-Code-Dev-Studio/releases/tag/v1.0.0
