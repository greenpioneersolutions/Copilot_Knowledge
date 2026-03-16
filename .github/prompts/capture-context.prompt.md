---
name: capture-context
description: Convert a raw document or note set into durable repository memory
agent: agent
---
Use the following files as context:

- [Context memory strategy](../../docs/06-context-memory-strategy.md)
- [Source document workflow](../../knowledge/source-docs/README.md)
- [Manager FAQ](../../knowledge/manager-faq.md)
- [Glossary](../../knowledge/glossary.md)

Given a raw document, transcript, policy, or note set:

1. create or update a sidecar summary in `knowledge/source-docs/summaries/`
2. propose glossary additions if new durable terms appear
3. propose FAQ updates if recurring questions are likely
4. recommend whether the content belongs in a Copilot Space
5. recommend whether a decision log should be created or updated

Keep summaries concise and structured.
Do not copy long passages from the source.
