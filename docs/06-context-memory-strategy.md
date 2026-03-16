# Context and memory strategy

Source key: see [`docs/SOURCES.md`](SOURCES.md).

## Core decision

**Use Markdown as the canonical memory layer.**

### Why
- GitHub customization is built around files in the repository [S01][S11][S14]
- prompt files can reference other workspace files [S11][S14]
- instructions are Markdown files [S11][S12]
- Microsoft’s GitHub connector indexes Markdown and text files [S08]
- Markdown is diffable, reviewable, and easy to reorganize

## Storage policy

## 1. Source artifacts
Use for:
- original PDFs
- official exports
- slide decks
- spreadsheets
- attachments

Store only when:
- policy allows it
- the original has real future value
- the repo is an appropriate location for that data

Recommended location:
- `knowledge/source-docs/originals/`

## 2. Durable summaries
Use for:
- what Copilot should actually reuse later
- the condensed meaning of a source artifact

Recommended location:
- `knowledge/source-docs/summaries/`

## 3. Stable shared knowledge
Use for:
- terms
- FAQs
- policies
- playbooks
- decisions
- onboarding notes

Recommended locations:
- `knowledge/glossary.md`
- `knowledge/manager-faq.md`
- `knowledge/policies/`
- `knowledge/playbooks/`
- `knowledge/decisions/`

## Rule of thumb

### Use a PDF when
- formatting matters
- the original is the authoritative artifact
- you are attaching it to a Space for reference
- the content will not be edited collaboratively in Git

### Use Markdown when
- the content should be reused by Copilot
- you want version control and code review
- you want to link it from prompts or instructions
- you want easy future updates
- the content belongs in FAQ / glossary / playbooks / decisions

## Recommended memory objects

### Glossary
Capture stable definitions:
- product or platform terms
- internal acronyms
- role names
- recurring workflow labels

### Manager FAQ
Capture recurring questions:
- which surface do I use?
- where do I store this?
- how do I reference files?
- what belongs in a Space?
- what should not go in Git?

### Policy summaries
Capture:
- what the policy means operationally
- what managers need to do
- common mistakes
- escalation points

### Playbooks
Capture:
- how to run recurring workflows
- what “good” looks like
- example outputs

### Decision logs
Capture:
- context
- choice
- tradeoffs
- consequences
- follow-ups

## Memory capture workflow

Use this after:
- a new policy arrives
- a meeting produces decisions
- a rollout reveals repeat questions
- onboarding reveals confusion
- a good prompt or workflow proves reusable

### Workflow
1. Identify the raw source
2. Create or update a Markdown summary
3. Extract durable terminology into the glossary
4. Extract recurring questions into the FAQ
5. Create or update a decision log if a real choice was made
6. Recommend whether the material should be added to a Space

## Suggested summary structure for a source document

Use this structure in `knowledge/source-docs/summaries/`:

- Source
- Owner
- Date
- Sensitivity
- Scope
- Key points
- Manager implications
- Open questions
- Related glossary entries
- Related decisions
- Related Space manifest

See [`knowledge/source-docs/summaries/source-summary-template.md`](../knowledge/source-docs/summaries/source-summary-template.md).

## What to do when the source cannot be committed

If the original PDF or document should not live in Git:
- do **not** commit the original
- create the Markdown summary anyway
- note where the original is stored externally
- record any sensitivity constraints in the summary

## How this relates to Copilot Memory

Copilot Memory can reduce repeated prompting and retain repository-level insights [S05], but it is not the same as a durable knowledge base:
- it is automatically generated
- it is validated against citations in the codebase [S05]
- it auto-expires after 28 days [S06]

So use Copilot Memory as a helpful layer, not as your official operating memory.

## Practical recommendation for managers

If a manager asks, “Where should I put this?” the default order is:

1. **Glossary / FAQ / playbook / decision log** if the insight is durable
2. **Markdown sidecar summary** if it came from a raw document
3. **Space** if it should be shared as retrieval context
4. **Keep only the original artifact** if future reuse is unlikely

## Bottom line

The system you want is:

- **raw documents as inputs**
- **Markdown as memory**
- **Spaces as shared retrieval**
- **repo customizations as workflow accelerators**
