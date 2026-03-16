---
name: meeting-notes-to-actions
description: Convert meeting notes into actions, owners, risks, and memory updates
agent: ask
---
Use the following files as context:

- [Meeting to decision-log playbook](../../knowledge/playbooks/meeting-to-decision-log.md)
- [Manager FAQ](../../knowledge/manager-faq.md)
- [Context memory strategy](../../docs/06-context-memory-strategy.md)

Turn the supplied meeting notes into:

1. a short meeting summary
2. an action list with owners and due dates if present
3. decisions made
4. open questions
5. recommended memory updates for this repo

If the notes introduce durable terminology, propose glossary additions.
If the notes record a meaningful decision, recommend creating a new file in `knowledge/decisions/`.
