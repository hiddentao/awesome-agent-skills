# Awesome Agent Skills [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Agent Skills and Claude Code slash commands written and published by [hiddentao](https://github.com/hiddentao).

hiddentao wrote every skill and command on this list, except where an entry says otherwise. An [Agent Skill](https://agentskills.io) is a folder with a `SKILL.md` file and, often, reference files and scripts. A coding agent such as Claude Code, Codex CLI, Cursor or GitHub Copilot reads the skill when a task needs it.

## Contents

- [Skills](#skills)
  - [3D graphics and games](#3d-graphics-and-games)
  - [Code review and documentation](#code-review-and-documentation)
  - [Working with agents](#working-with-agents)
  - [Self-hosting](#self-hosting)
- [Slash commands](#slash-commands)
- [Installing](#installing)

## Skills

### 3D graphics and games

- [tripo3d-blender-aaa](https://github.com/hiddentao/tripo3d-blender-aaa-skill) - Turn concept pictures into AAA-quality 3D models and scenes that match them, with an image model for the art, Tripo3D for base meshes, Blender for the finish, and a measured pipeline that checks the final render against the concept.
- [3d-web-scene-performance](https://github.com/hiddentao/3d-web-scene-performance-skill) - Build 3D scenes for web pages that run at 60 fps on phones, tablets and desktops, show something within five seconds on a slow connection, and fall back to a normal page if the renderer fails.
- [sakurai](https://github.com/hiddentao/sakurai-skill-en) - Game-making principles from all 257 main episodes of Masahiro Sakurai's YouTube series "Masahiro Sakurai on Creating Games", for planning, reviewing and fixing a game. Translated into English by hiddentao from [kociden/sakurai-skill](https://github.com/kociden/sakurai-skill), which kociden wrote.

### Code review and documentation

- [review-rubric](https://github.com/hiddentao/claude-code-plugins/tree/main/plugins/code-review/skills/review-rubric) - Review dimensions, finding format, severity scale and verification steps for adversarial review of code and documentation. Part of the `code-review` plugin.
- [explore-code](https://github.com/hiddentao/claude-code-plugins/tree/main/plugins/docs/skills/explore-code) - Checklist for exploring a codebase: structure, conventions, libraries, error handling, logging, performance, security, build, scripts and tests. Part of the `docs` plugin.

### Working with agents

- [writing-skill-files](https://github.com/hiddentao/claude-code-plugins/tree/main/plugins/skill-files/skills/writing-skill-files) - The 28 rules for writing a skill file that an AI agent can follow. They cover structure, decision rules, named anti-patterns, code contracts, freshness and testing. Part of the `skill-files` plugin.

### Self-hosting

- [chatwoot-self-hosting](https://github.com/hiddentao/chatwoot-self-hosting-skill) - Deploy, harden and run a self-hosted Chatwoot installation. The admin console stays private, the widget script is patched, and each chat widget works only on the sites allowed to embed it.

## Slash commands

These work in Claude Code only.

- [/code-review:adversarial](https://github.com/hiddentao/claude-code-plugins/blob/main/plugins/code-review/commands/adversarial.md) - Review a codebase and its recent commits with up to 10 subagents in two rounds, where the second round tries to disprove each finding of the first. Part of the `code-review` plugin.
- [/docs:generate-markdown-retype](https://github.com/hiddentao/claude-code-plugins/blob/main/plugins/docs/commands/generate-markdown-retype.md) - Generate Markdown documentation for a codebase that works with [Retype](https://retype.com), with your approval at each stage. Part of the `docs` plugin.
- [/skill-files:audit](https://github.com/hiddentao/claude-code-plugins/blob/main/plugins/skill-files/commands/audit.md) - Audit a `SKILL.md`, `llms.txt`, `AGENTS.md` or other agent-facing document against the 28 rules, with an optional trial by a fresh agent. Part of the `skill-files` plugin.
- [/subagent:subagent](https://github.com/hiddentao/claude-code-plugins/blob/main/plugins/subagent/commands/subagent.md) - Find the subagents that match a task, pick one and launch it with your own prompt. Part of the `subagent` plugin.

## Installing

Each skill repo explains how to install its skill in each tool. In short, copy the skill folder into the folder where your agent looks for skills, for example `~/.claude/skills/` for Claude Code.

The `tripo3d-blender`, `3d-web-scene-performance` and `chatwoot-self-hosting` repos are also Claude Code plugin marketplaces. For example:

```bash
claude plugin marketplace add hiddentao/3d-web-scene-performance-skill
claude plugin install 3d-web-scene-performance@3d-web-scene-performance-skill
```

The skills and commands marked "Part of the ... plugin" come from the [claude-code-plugins](https://github.com/hiddentao/claude-code-plugins) marketplace. Add it once, then install the plugin you want:

```bash
claude plugin marketplace add hiddentao/claude-code-plugins
claude plugin install code-review@hiddentao-plugins
```

## Contributing

See the [contribution guide](contributing.md).
