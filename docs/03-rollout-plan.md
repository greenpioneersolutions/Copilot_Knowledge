# Rollout plan

Source key: see [`docs/SOURCES.md`](SOURCES.md).

## Objective

Roll out GitHub Copilot in a way that improves manager and engineer effectiveness without making the organization dependent on ad hoc prompting.

## Guiding ideas

GitHub’s enablement guidance recommends:
- defining success metrics early
- training champions
- sharing asynchronous resources
- hosting a workshop
- providing live support channels
- continuing to adapt enablement over time [S31]

GitHub’s trial and measurement guidance also recommends combining usage metrics with qualitative feedback [S32][S33][S34].

## Suggested rollout phases

## Phase 0 — sponsor alignment

### Outcomes
- clarify why the organization is rolling Copilot out
- identify two or three engineering goals
- define what “good” looks like

### Recommended goals
Do not start with “20% more productive” in the abstract.

Instead pick goals such as:
- faster issue refinement
- better onboarding
- improved test coverage
- fewer review loops
- clearer rollout plans
- lower time to decision for ambiguous work

### Artifacts
- updated `knowledge/team-charter.md`
- customized `knowledge/policies/ai-usage-policy.md`
- decision on what information can be stored in Git

## Phase 1 — foundation

### Outcomes
- stand up the repo
- publish the starter docs
- create first manager Space
- define the memory capture workflow

### Work
- customize `.github/copilot-instructions.md`
- finalize glossary and FAQ
- create first Space from `knowledge/space-manifests/engineering-management-core.md`
- run one “raw document -> Markdown summary” exercise

### Success criteria
- at least one shared Space is live
- at least five durable knowledge files exist
- at least one manager has used the repo to answer a real question

## Phase 2 — workflow pack

### Outcomes
- managers can perform repeatable tasks with less friction
- Copilot usage moves from generic chat to role-specific workflows

### Suggested workflows to package
- issue intake
- onboarding plan
- status update
- meeting notes to actions
- decision log
- feature / rollout planning

### Artifacts
- prompt files under `.github/prompts/`
- one or two custom agents
- one skill for context capture or decision logging

### Success criteria
- five to seven reusable workflows exist
- managers can complete those workflows without needing a champion every time

## Phase 3 — champion enablement

### Outcomes
- a small group of technical and manager champions can teach others
- training exists in live and async form

### Work
- run workshop(s)
- record examples
- collect frequently asked questions
- refine docs based on real friction

### Recommended champion mix
- 1 engineering manager
- 1 technical lead or staff engineer
- 1 platform / dev productivity representative
- 1 product or program manager if cross-functional use is expected

### Success criteria
- champions can demo at least three workflows end to end
- FAQ has been updated from real questions
- users know when to use GitHub.com vs VS Code vs CLI

## Phase 4 — measure and govern

### Outcomes
- adoption is visible
- value is tied to concrete goals
- context quality stays high

### What to measure
Use GitHub’s usage metrics for:
- active users
- engagement
- feature usage
- agent adoption
- model / surface trends
- pull request lifecycle trends [S32][S33][S34]

Add your own measures for:
- onboarding cycle time
- issue quality
- clarity of status updates
- reduction in repeated manager questions
- time to create a decision log or rollout plan
- user trust / satisfaction

### What not to over-index on
- raw PR throughput alone
- raw line counts
- vanity prompt counts
- one-off “wow” demos without durable adoption

## 30 / 60 / 90 day version

### First 30 days
- repo launched
- one Space live
- five common manager workflows documented
- first workshop run

### First 60 days
- champions active
- manager FAQ and glossary updated from real usage
- second Space live
- initial adoption and feedback review

### First 90 days
- governance refinements made
- metrics reviewed against goals
- rollout expanded or narrowed based on evidence
- advanced users begin using CLI / MCP / deeper customization where justified

## Communication plan

### Before launch
- explain why Copilot is being adopted
- explain what information is allowed
- explain that the repo is the memory layer

### At launch
- publish the repo
- publish the Space link(s)
- run a short workshop
- provide an office-hours channel

### After launch
- share examples
- answer FAQs publicly
- keep updating docs rather than repeating answers in chat

## Minimum viable rollout package

If you want the leanest useful version, launch with:
- this repo
- one shared Space
- five prompt files
- one custom agent
- one workshop
- one monthly adoption review
