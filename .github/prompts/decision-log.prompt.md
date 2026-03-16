---
name: decision-log
description: Convert a discussion into a durable decision log entry
agent: ask
---
Use the following files as context:

- [Decision log template](../../.github/skills/decision-log/templates/decision-log-template.md)
- [Memory policy decision](../../knowledge/decisions/0001-repo-memory-policy.md)
- [Meeting to decision-log playbook](../../knowledge/playbooks/meeting-to-decision-log.md)

Create a Markdown decision log entry using ADR-style structure.

Include:
- title
- status
- date
- context
- decision
- options considered
- tradeoffs
- consequences
- follow-up actions

If the material contains unresolved questions, add them under follow-up actions rather than hiding them.
