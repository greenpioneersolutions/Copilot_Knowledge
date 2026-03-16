---
name: context-capture
description: Convert raw source material into Markdown summaries, glossary updates, FAQ entries, and Space recommendations
---
Use this skill when the task involves:
- a new policy or guidance document
- a PDF or uploaded file
- meeting notes or transcript
- onboarding information
- operational knowledge that should outlive a single chat

## Process
1. Identify the source artifact and its owner / sensitivity / date.
2. Create or update a sidecar summary.
3. Extract durable terms and update the glossary if needed.
4. Extract recurring questions and update the manager FAQ if needed.
5. Decide whether the material should:
   - remain only as a source summary
   - become a playbook or policy
   - be added to a Copilot Space manifest
   - create or update a decision log

## Supporting resource
Use `templates/context-capture-checklist.md`.

## Output locations
- `knowledge/source-docs/summaries/`
- `knowledge/glossary.md`
- `knowledge/manager-faq.md`
- `knowledge/space-manifests/`
- `knowledge/decisions/`
