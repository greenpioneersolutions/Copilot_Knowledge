# Manager Copilot Framework

A starter repository for teaching managers and engineering leaders how to use **GitHub Copilot** more effectively across GitHub.com, Visual Studio Code, and Copilot CLI—while storing durable team context in a form Copilot can reuse.

This repo is designed around one principle:

> **Use Markdown as the durable memory layer.**
>
> Keep PDFs and other rich files as source artifacts when needed, but convert what matters into concise, reviewable Markdown summaries, glossaries, FAQs, decision logs, and playbooks.

Source key: see [`docs/SOURCES.md`](docs/SOURCES.md).

## What this repository gives you

- A documented framework for using GitHub Copilot with managers and non-specialist users
- A starter knowledge structure for policies, playbooks, FAQs, and decision logs
- Example Copilot customizations:
  - repo-wide instructions
  - path-specific instructions
  - prompt files
  - custom agents
  - skills
- A rollout and training plan you can adapt for your organization
- A space blueprint for shared GitHub Copilot Spaces

## Recommended operating model

1. **Store durable knowledge in Markdown**
   - policies
   - playbooks
   - glossary
   - decisions
   - onboarding notes
   - FAQs

2. **Use GitHub Copilot Spaces for shared, curated context**
   - repositories
   - issues
   - pull requests
   - notes
   - transcripts
   - uploads

3. **Use the right surface for the job**
   - **GitHub.com + Spaces** for managers and light technical work
   - **VS Code** for technical managers and champions
   - **Copilot CLI** for advanced users who want plan / research / automation flows
   - **Microsoft 365 Copilot** for mail, meetings, and M365-grounded work

4. **Capture durable insights back into the repo**
   - never let important knowledge live only in chat history

## Start here

Read these in order:

1. [`docs/01-research-summary.md`](docs/01-research-summary.md)
2. [`docs/02-framework-architecture.md`](docs/02-framework-architecture.md)
3. [`docs/05-surface-guide.md`](docs/05-surface-guide.md)
4. [`docs/06-context-memory-strategy.md`](docs/06-context-memory-strategy.md)
5. [`docs/03-rollout-plan.md`](docs/03-rollout-plan.md)
6. [`docs/04-training-curriculum.md`](docs/04-training-curriculum.md)

## Repo map

```text
.github/
  copilot-instructions.md
  instructions/
  prompts/
  agents/
  skills/

docs/
  research, architecture, rollout, curriculum, governance, spaces, sources

knowledge/
  glossary, FAQ, policies, playbooks, decisions, examples, source-doc summaries, space manifests
```

## 7-day quick start

### Day 1
- Read the docs listed in **Start here**
- Rename the repo for your org/team
- Update [`knowledge/team-charter.md`](knowledge/team-charter.md)

### Day 2
- Customize [`knowledge/policies/ai-usage-policy.md`](knowledge/policies/ai-usage-policy.md)
- Decide what can and cannot be committed to Git
- Update [`knowledge/decisions/0001-repo-memory-policy.md`](knowledge/decisions/0001-repo-memory-policy.md)

### Day 3
- Create your first shared Space using [`knowledge/space-manifests/engineering-management-core.md`](knowledge/space-manifests/engineering-management-core.md)
- Add only curated context, not whole-repo dumps

### Day 4
- Copy or refine the prompt files in `.github/prompts/`
- Run one manager workflow end to end:
  - meeting notes -> actions
  - rough request -> issue
  - policy doc -> Markdown sidecar summary

### Day 5
- Test the custom agents in `.github/agents/`
- Have one technical manager and one non-specialist manager use the repo

### Day 6
- Run a short workshop using [`docs/04-training-curriculum.md`](docs/04-training-curriculum.md)
- Collect feedback on friction points

### Day 7
- Decide your initial rollout
- Track adoption and qualitative feedback with [`docs/07-governance-metrics.md`](docs/07-governance-metrics.md)

## How to use this repo in practice

### GitHub.com
- Open a shared Space
- Ask work questions grounded in that Space
- Use the knowledge docs as stable references
- Capture important outcomes back into `knowledge/` or `docs/`

### VS Code
- Let `.github/copilot-instructions.md` supply project-wide context
- Use prompt files for recurring tasks
- Use custom agents for specialized flows
- Use `#file`, `#folder`, and `#symbol` to sharpen context

### Copilot CLI
- Work inside the repo root
- Use `@relative/path/to/file.md` to attach files
- Use plan mode before execution on larger tasks
- Use `/research` for deeper investigation when appropriate

## What to customize first

- `knowledge/team-charter.md`
- `knowledge/policies/ai-usage-policy.md`
- `knowledge/policies/delivery-policy.md`
- `knowledge/glossary.md`
- `knowledge/manager-faq.md`
- `.github/copilot-instructions.md`
- the prompt files under `.github/prompts/`

## Important note on source documents

Do **not** make a giant folder of PDFs your primary Copilot strategy.

Instead:

- keep originals only when policy permits
- summarize them into Markdown
- link the summary to the original
- update glossary / FAQ / decision log when the content is durable
- add only the most useful artifacts to Spaces

See [`knowledge/source-docs/README.md`](knowledge/source-docs/README.md) and [`docs/06-context-memory-strategy.md`](docs/06-context-memory-strategy.md).
