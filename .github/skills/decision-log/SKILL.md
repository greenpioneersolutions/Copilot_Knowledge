---
name: decision-log
description: Turn a discussion or note set into a durable ADR-style decision log and related memory updates
---
Use this skill when the task involves:
- a meaningful decision
- tradeoffs or option analysis
- approval history
- architecture or delivery choices
- recurring questions that should be captured permanently

## Process
1. Review the provided notes, transcript, or discussion.
2. Create or update a decision log using the template in `templates/decision-log-template.md`.
3. Add glossary entries if durable terms were introduced.
4. Update `knowledge/manager-faq.md` if the discussion revealed repeat questions.
5. Recommend any Copilot Space updates if the decision should become shared context.

## Output location
Default destination: `knowledge/decisions/`

## Quality bar
- make the decision explicit
- capture options considered
- record the tradeoffs
- include consequences and follow-ups
- avoid vague language such as "we decided something like..."
