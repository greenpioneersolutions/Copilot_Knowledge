# Repository purpose

This repository is a starter framework for helping managers and engineering leaders use GitHub Copilot effectively.

## Working rules

- Favor **Markdown** as the canonical knowledge format.
- Treat source documents such as PDFs as inputs that should usually be summarized into Markdown sidecars.
- Prefer curated context over broad dumps.
- When producing reusable guidance, write to `docs/` or `knowledge/`.
- Keep outputs structured and easy to skim.
- When summarizing a source artifact, preserve:
  - source path or link
  - date
  - owner
  - sensitivity notes
  - decisions / actions / glossary terms

## Output patterns to prefer

For manager workflows, default to one of these structures unless a better fit is obvious:

1. **Issue / task**
   - problem
   - goals
   - non-goals
   - scope
   - acceptance criteria
   - dependencies
   - risks
   - rollout
   - done definition

2. **Decision log**
   - context
   - decision
   - options considered
   - tradeoffs
   - consequences
   - follow-ups

3. **Status update**
   - what changed
   - current status
   - blockers
   - risks
   - asks / decisions needed
   - next steps

4. **Research brief**
   - question
   - findings
   - implications
   - recommendation
   - open questions

## Context behavior

- Use the smallest set of relevant files that answer the question.
- Prefer summaries, glossaries, FAQs, and decision logs over long raw documents.
- Suggest updates to repository memory when the result is likely to matter later.

## Style

- Be direct and practical.
- Call out assumptions explicitly.
- Avoid overstating confidence.
- If documentation appears inconsistent, note the discrepancy and recommend validation.
