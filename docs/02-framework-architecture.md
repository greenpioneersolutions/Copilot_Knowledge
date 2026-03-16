# Framework architecture

Source key: see [`docs/SOURCES.md`](SOURCES.md).

## Goal

Create a reusable operating system for managers using GitHub Copilot without requiring every manager to become highly technical.

## Architecture overview

```text
Raw sources
  -> Durable Markdown memory
    -> Copilot repo customizations
      -> Shared Spaces
        -> Surface-specific workflows
          -> Measurement and governance
```

## Layer 1: raw sources

These are the original artifacts:
- PDFs
- Word docs
- spreadsheets
- slide decks
- meeting notes
- transcripts
- issue threads
- pull requests

These are inputs, not your best long-term memory format.

### Rule
Keep raw sources only when policy allows, and only when they add value later.

## Layer 2: durable Markdown memory

This is the core of the framework.

### What belongs here
- `knowledge/glossary.md`
- `knowledge/manager-faq.md`
- `knowledge/policies/*.md`
- `knowledge/playbooks/*.md`
- `knowledge/decisions/*.md`
- `knowledge/source-docs/summaries/*.md`
- `knowledge/space-manifests/*.md`

### Why Markdown
- GitHub’s customization model is file-based [S01][S11][S14]
- it diffs well
- it is easy to review in pull requests
- it is easy to reference from prompt files and instructions [S11][S14]
- it aligns with Microsoft’s GitHub knowledge indexing for Markdown and text [S08]

## Layer 3: repo customizations

This repo demonstrates four main customization layers.

### Repo-wide instructions
`.github/copilot-instructions.md`

Use for:
- stable guidance
- output structures
- repo purpose
- memory preferences

### Path-specific instructions
`.github/instructions/*.instructions.md`

Use for:
- file-type or folder-specific rules
- prompt authoring rules
- agent / skill authoring rules

### Prompt files
`.github/prompts/*.prompt.md`

Use for:
- repeatable tasks
- manager workflows with predictable structure
- “run once with different inputs” tasks [S01][S14]

### Custom agents and skills
- `.github/agents/*.agent.md`
- `.github/skills/**/SKILL.md`

Use for:
- specialized roles
- multi-step capabilities
- deeper automation or file updates [S24][S25][S26][S27]

## Layer 4: shared Spaces

GitHub Copilot Spaces are the shared retrieval and grounding layer.

Use Spaces for:
- a curated bundle of repos, issues, PRs, docs, notes, transcripts, and uploads [S02]
- onboarding
- architecture context
- delivery expectations
- repeat questions across managers

### Important Space rules
- curate aggressively
- do not dump everything in
- create a few Spaces with clear purpose
- use organization-owned Spaces where team sharing matters [S03]

### IDE limitation to remember
Spaces used from the IDE do not currently include repository context, and repository-only Spaces are limited for IDE access [S04][S39].

## Layer 5: surface-specific workflows

### GitHub.com
Best for:
- shared context
- lower-friction manager access
- issue and planning workflows
- team questions in a Space

### VS Code
Best for:
- technical managers
- file-targeted chat
- prompts, agents, and repo instructions
- faster customization iteration

### Copilot CLI
Best for:
- advanced users
- plan / research / automation flows
- terminal-native work
- controlled autonomous execution [S16][S17][S18][S19]

### Microsoft 365 Copilot
Best as a complement for:
- Outlook / Teams / docs / meetings
- M365-grounded work
- tenant knowledge retrieval
- agents for information workers [S07][S09][S10]

## Layer 6: governance and measurement

This framework should be managed like a product:
- curate context
- review changes
- measure adoption
- gather qualitative feedback
- tighten permissions only when necessary

Use GitHub’s usage metrics and dashboards as part of the stack, but combine them with internal success criteria and manager feedback [S32][S33][S34][S35].

## Memory capture loop

Use this loop after every significant interaction:

1. **Did we learn something durable?**
2. **Should it live in Markdown?**
3. **Where should it go?**
   - glossary
   - FAQ
   - playbook
   - decision log
   - policy summary
   - Space manifest
4. **Who owns it?**
5. **Does it need to be shared?**

## Anti-patterns

Avoid these:
- giant PDF dumps
- one enormous instruction file
- teaching “clever prompt tricks” without context discipline
- measuring success only by PR count
- leaving important decisions buried in chat history
- over-automating before basic curation exists

## Recommended default

For most manager teams, start with:

- one shared repo
- one repo-wide instructions file
- two or three path-specific instructions files
- five to seven prompt files
- one or two custom agents
- one shared Space
- a Markdown-first memory habit
