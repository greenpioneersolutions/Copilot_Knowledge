---
applyTo: ".github/agents/**/*.agent.md,.github/skills/**/SKILL.md"
description: "Define custom agents and skills with least-privilege behavior and durable outputs."
---
# Agent and skill authoring rules

- Give the agent or skill a narrow, clear role.
- Prefer least-privilege tool access.
- Bias toward read / search before edit.
- When edits are appropriate, create or update Markdown artifacts that can be reviewed.
- Tell the agent what durable repo updates to make:
  - summary
  - glossary
  - FAQ
  - decision log
  - playbook
- Keep instructions explicit enough to reduce drift but short enough to stay readable.
- Avoid claiming certainty when the task involves missing or changing platform behavior.
