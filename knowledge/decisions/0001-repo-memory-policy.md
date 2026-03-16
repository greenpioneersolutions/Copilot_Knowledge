# ADR-0001: Repository memory policy

- Status: accepted
- Date: 2026-03-15
- Owners: manager enablement

## Context

Managers and engineering leaders need a durable way to reuse context across GitHub Copilot sessions. Raw source artifacts such as PDFs and meeting notes are often useful as inputs, but they are not the best long-term memory layer for reusable Copilot context.

## Decision

This repository will use **Markdown as the canonical memory layer**.

Raw artifacts such as PDFs may be kept only when policy allows and when the original remains useful. Durable content should be summarized into Markdown and placed in the appropriate area of `knowledge/`.

## Options considered

1. PDFs as the primary memory system
2. Markdown summaries as the primary memory system
3. Chat history plus ad hoc prompts only

## Tradeoffs

### Why Markdown won
- easier to diff and review
- easier to reference from prompts and instructions
- aligns with GitHub’s file-based customization model
- aligns with Microsoft’s Markdown/text indexing for GitHub knowledge

### What we give up
- perfect visual fidelity of source documents
- some up-front summarization effort

## Consequences

- the team must capture durable knowledge intentionally
- repeated questions should be turned into FAQs
- new durable terms should be added to the glossary
- source summaries should point back to the original artifact or system of record

## Follow-up actions

- [ ] Customize the AI usage policy
- [ ] Review what can be stored in Git
- [ ] Create the first shared Space
