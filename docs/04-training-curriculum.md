# Training curriculum

Source key: see [`docs/SOURCES.md`](SOURCES.md).

## Training philosophy

Teach **scenarios and habits**, not abstract “prompt engineering.”

GitHub’s official examples already lean toward repeatable scenarios such as issue management, onboarding, implementation planning, and project planning [S22][S23][S28][S29]. That is the model to follow.

## Audience lanes

### Lane A — manager lane
For:
- engineering managers
- product / program managers working near engineering
- leaders who mostly use GitHub.com

### Lane B — champion lane
For:
- technical managers
- staff / principal engineers
- dev productivity leads
- early adopters who can support others

## Core modules

## Module 1 — choose the right Copilot

### Outcome
Participants know when to use:
- GitHub Copilot
- Microsoft 365 Copilot
- Microsoft 365 Copilot Chat
- Agent Builder / Copilot Studio

### Key lesson
- code-adjacent engineering work -> GitHub Copilot [S07]
- M365-grounded information work -> Microsoft 365 Copilot [S07][S10]
- broader or more advanced business agents -> Copilot Studio [S09]

## Module 2 — how context really works

### Outcome
Participants understand that quality comes from context, not just wording.

### Teach
- repo instructions [S11][S12]
- path-specific instructions [S11][S12]
- prompt files [S14]
- Spaces [S02][S03][S04]
- file references in IDE / CLI / prompt files [S11][S14][S16][S20]

### Exercise
Take one vague request and improve it by:
1. choosing the right surface
2. adding the right files
3. choosing the right output structure

## Module 3 — manager workflows

### Outcome
Participants can run repeatable workflows with prompt files.

### Teach these flows
- rough request -> issue
- new hire -> onboarding plan
- notes -> status update
- meeting -> actions
- discussion -> decision log

### Exercise
Use the provided prompt files in `.github/prompts/`.

## Module 4 — memory and capture

### Outcome
Participants learn how not to lose good work.

### Teach
- PDFs are not the primary memory layer
- summaries go in Markdown
- update glossary / FAQ / decisions
- Spaces are shared retrieval, not the whole memory system
- Copilot Memory is useful but secondary [S05][S06]

### Exercise
Convert a policy document or meeting note set into:
- a sidecar summary
- a glossary update
- a FAQ entry
- a Space recommendation

## Module 5 — GitHub.com, VS Code, and CLI

### Outcome
Participants know which surface to use and how to reference context.

### Teach
- GitHub.com: Spaces and `@` mentions [S42]
- VS Code: `#file`, `#folder`, `#symbol` [S20][S41]
- CLI: `@relative/path`, plan mode, `/research` [S16][S17]

### Exercise
Run the same workflow in two different surfaces and compare friction.

## Module 6 — review, verification, and governance

### Outcome
Participants learn to trust but verify.

### Teach
- review AI output
- keep tasks scoped [S18]
- understand CLI permissions and trusted directories [S18][S19]
- tie usage to specific business or engineering goals [S31][S35]
- measure adoption plus qualitative feedback [S32][S33][S34]

## Suggested workshop agenda (60 minutes)

### 0–10 min
Why this framework exists

### 10–20 min
Which Copilot to use when

### 20–35 min
Context techniques and memory model

### 35–50 min
Live demo:
- rough request -> issue
- notes -> decision log
- source doc -> Markdown summary

### 50–60 min
Q&A and next steps

## Suggested workshop agenda (90 minutes)

### Part 1
- product overview
- context and surfaces
- manager workflow examples

### Part 2
Hands-on breakout:
- one GitHub.com flow
- one VS Code flow
- one memory capture flow

### Part 3
Review, questions, and repo contributions

## Materials to hand out

- `README.md`
- `docs/05-surface-guide.md`
- `docs/06-context-memory-strategy.md`
- `.github/prompts/`
- `knowledge/manager-faq.md`

## Success markers

A manager has completed the training successfully when they can:
- choose the correct Copilot surface
- attach the correct context
- use at least two prompt files
- capture durable output back into the repo
- explain why Markdown beats PDF as primary memory
