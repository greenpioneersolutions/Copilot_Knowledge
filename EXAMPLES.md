# Examples

This file contains practical, in-depth examples of how to use this repository in real work.

The goal is not just to show prompts. The goal is to help a manager, technical lead, or enablement champion quickly answer:

- **What problem is this trying to solve?**
- **Does this apply to me?**
- **Which Copilot surface should I use?**
- **Which files in this repo should I reference?**
- **What should I save back into the repo so the work becomes reusable?**

Use these examples as starting patterns. Adapt the language, files, and outputs to your team.

---

## How to read these examples

Each example includes:

- **What this solves for** — the practical problem the example is meant to address
- **Who this is for** — the type of manager or user most likely to benefit
- **Best surface** — GitHub.com, VS Code, Copilot CLI, or a Copilot Space
- **Repo assets to use** — the files from this repository that improve the result
- **Suggested prompt or workflow** — a concrete starting point
- **Why this works** — how the repo structure helps Copilot produce a better answer
- **What to save back** — the durable memory you should capture instead of leaving it in chat
- **Common mistakes** — what to avoid

---

## Example 1 — Build a 30-60-90 day onboarding plan for a new engineering manager

### What this solves for
A new manager joins and needs a structured onboarding plan that is grounded in how your organization actually works, not a generic checklist.

### Who this is for
- directors onboarding new managers
- senior managers mentoring first-line managers
- technical leaders formalizing onboarding for the first time

### Best surface
- **GitHub.com + a shared Copilot Space** for non-technical managers
- **VS Code** for champions refining the plan as a saved artifact

### Repo assets to use
- `knowledge/team-charter.md`
- `knowledge/operating-model.md`
- `knowledge/glossary.md`
- `knowledge/space-manifests/onboarding-space.md`
- `.github/prompts/onboarding-plan.prompt.md`

### Suggested workflow
1. Update the team charter and operating model to reflect your real org.
2. Create or refine an onboarding Copilot Space using the onboarding manifest.
3. Use the onboarding prompt file or paste its structure into Copilot.
4. Ask Copilot to tailor the plan for the exact role.

### Suggested prompt
```text
Create a 30-60-90 day onboarding plan for a new engineering manager who inherits two teams,
one staff engineer, and one program manager relationship.

Use:
- knowledge/team-charter.md
- knowledge/operating-model.md
- knowledge/glossary.md
- knowledge/space-manifests/onboarding-space.md

Include:
- first day
- first week
- first 30 days
- first 60 days
- first 90 days
- key people to meet
- decisions to understand
- quick wins
- Copilot workflows they should practice
```

### Why this works
The repo gives Copilot a grounded view of your team language, operating rhythm, and expected workflows. That prevents the plan from sounding like a generic HR checklist.

### What to save back
- a role-specific onboarding plan under `knowledge/playbooks/`
- glossary updates if new role-specific terms appear
- Space updates if important repos, issues, or decisions were missing

### Common mistakes
- using only a generic onboarding prompt with no team context
- failing to include the actual team charter and operating model
- not saving the final onboarding plan as Markdown

---

## Example 2 — Turn a rough request into a structured GitHub issue

### What this solves for
A manager has a vague request such as “we need better deployment visibility” and wants to turn it into something engineers can actually execute.

### Who this is for
- managers who struggle to make requests implementation-ready
- product or program partners who need engineering-shaped issue drafts
- engineering leads helping peers write better work items

### Best surface
- **VS Code** if you want to save the result directly into the repo
- **GitHub.com** if the final destination is a GitHub issue

### Repo assets to use
- `.github/prompts/issue-intake.prompt.md`
- `knowledge/policies/delivery-policy.md`
- `knowledge/playbooks/pr-review-expectations.md`
- `knowledge/examples/good-prompts.md`

### Suggested prompt
```text
Turn this rough request into a well-structured issue:

"We need better deployment visibility because incidents take too long to triage.
We think dashboards and release correlation might help, but the exact scope is unclear."

Use:
- knowledge/policies/delivery-policy.md
- knowledge/playbooks/pr-review-expectations.md
- knowledge/examples/good-prompts.md

Output sections:
- Title
- Problem
- Goals
- Non-goals
- Scope
- Acceptance criteria
- Dependencies
- Risks
- Rollout / release notes
- Telemetry or validation
- Done definition
```

### Why this works
The issue-intake prompt pulls the request toward testable acceptance criteria, explicit assumptions, and reviewable scope. The delivery and PR expectations files help Copilot shape the issue the way your engineers actually need it.

### What to save back
- the final issue in GitHub
- a backlog playbook update if recurring issue patterns emerge
- a FAQ entry if managers commonly ask similar request-shaping questions

### Common mistakes
- asking Copilot to “write an issue” without giving acceptance criteria structure
- letting Copilot produce a giant umbrella issue with hidden work
- skipping rollout and validation sections

---

## Example 3 — Convert meeting notes into actions, decisions, and durable memory

### What this solves for
Managers often leave a meeting with good discussion but unclear follow-up, no durable decision record, and no shared memory for others.

### Who this is for
- managers running roadmap, architecture, or staffing meetings
- chiefs of staff or program managers supporting leadership meetings
- anyone who keeps losing important decisions in chat threads or notes

### Best surface
- **GitHub.com + shared Space** if the meeting is cross-team
- **VS Code** if you want to create or edit Markdown files immediately

### Repo assets to use
- `.github/prompts/meeting-notes-to-actions.prompt.md`
- `.github/prompts/decision-log.prompt.md`
- `knowledge/playbooks/meeting-to-decision-log.md`
- `.github/skills/decision-log/templates/decision-log-template.md`
- `docs/06-context-memory-strategy.md`

### Suggested workflow
1. Paste the notes into Copilot using the meeting-notes-to-actions prompt.
2. Review the resulting action list and open questions.
3. If a real decision was made, run the decision-log prompt or skill.
4. Save the decision under `knowledge/decisions/`.

### Suggested prompt
```text
Turn these meeting notes into:
1. a short summary
2. actions with owners and due dates if present
3. decisions made
4. open questions
5. recommended memory updates for this repo

Then tell me whether a decision log should be created.
Use:
- knowledge/playbooks/meeting-to-decision-log.md
- docs/06-context-memory-strategy.md
```

### Why this works
The repo distinguishes between ordinary notes and durable decisions. That helps managers avoid clutter while still preserving what matters.

### What to save back
- decision logs in `knowledge/decisions/`
- FAQ updates if the same question keeps coming up
- glossary updates if the meeting introduced new recurring terms

### Common mistakes
- saving every meeting as a decision log
- never capturing the decision at all
- leaving actions only in chat output instead of in a file or issue

---

## Example 4 — Convert an HR or policy PDF into Markdown memory

### What this solves for
Managers have a source document such as an HR policy, security guideline, or internal memo. They need the knowledge from it, but the original file is long, hard to reference, or should not become the primary memory system.

### Who this is for
- directors and managers working with policy-heavy environments
- enablement leads trying to reduce repeated policy questions
- teams trying to prevent “ask Copilot to read the PDF again” as the only workflow

### Best surface
- **GitHub.com** if you are working from uploaded files in a Space
- **VS Code** if you are creating the sidecar Markdown summary in the repo

### Repo assets to use
- `.github/prompts/capture-context.prompt.md`
- `.github/agents/context-curator.agent.md`
- `knowledge/source-docs/README.md`
- `knowledge/source-docs/summaries/source-summary-template.md`
- `knowledge/policies/hr-policy-summary.md`

### Suggested workflow
1. Keep the source file where your policy allows.
2. Use the capture-context prompt or context-curator agent.
3. Create a short Markdown sidecar summary.
4. Update the glossary and FAQ only if the terms or questions are durable.

### Suggested prompt
```text
I have a policy document about manager responsibilities during reorganizations.
Create a Markdown sidecar summary for this repo.

Use:
- knowledge/source-docs/README.md
- knowledge/source-docs/summaries/source-summary-template.md
- knowledge/manager-faq.md
- knowledge/glossary.md

Also tell me:
- whether the original should be added to a Copilot Space
- what glossary terms to add
- what FAQ entries to add
- whether any part of this belongs in a policy summary file
```

### Why this works
This repo is intentionally designed so that **PDF is a source artifact, not the primary memory layer**. The summary becomes easier for Copilot to reuse, easier for humans to review, and easier to version-control.

### What to save back
- a sidecar summary in `knowledge/source-docs/summaries/`
- updates to `knowledge/policies/`
- glossary and FAQ additions as needed

### Common mistakes
- committing a giant document set and expecting Copilot to infer the right parts every time
- copying long passages instead of summarizing durable meaning
- failing to record sensitivity and ownership notes

---

## Example 5 — Draft a concise manager status update from scattered notes

### What this solves for
A manager has fragments from Slack, meetings, personal notes, and issue comments and needs one coherent update for leadership.

### Who this is for
- first-line and senior managers preparing weekly updates
- directors consolidating cross-team status
- program managers partnering with engineering leaders

### Best surface
- **GitHub.com** for quick drafting
- **VS Code** if the output should become a recurring artifact or template

### Repo assets to use
- `.github/prompts/status-update.prompt.md`
- `knowledge/operating-model.md`
- `knowledge/policies/delivery-policy.md`
- `knowledge/manager-faq.md`

### Suggested prompt
```text
Turn these notes into a concise status update for stakeholders.

Use this structure:
- Summary
- What changed
- Current status
- Risks / blockers
- Decisions needed
- Next steps

Use:
- knowledge/operating-model.md
- knowledge/policies/delivery-policy.md
- knowledge/manager-faq.md

Separate facts from assumptions and surface decisions early.
```

### Why this works
The prompt file already biases the answer toward visible risk and clear next steps. The operating model and delivery policy help avoid updates that are either too vague or too technical.

### What to save back
- if this becomes a repeatable pattern, save a team-specific status template under `knowledge/playbooks/`
- FAQ updates if managers repeatedly ask how to structure updates

### Common mistakes
- letting Copilot produce a wordy narrative with no decisions needed
- hiding uncertainty instead of separating fact from assumption
- treating status updates as memory instead of capturing only the durable parts elsewhere

---

## Example 6 — Create a shared Copilot Space for engineering managers

### What this solves for
Managers need a shared context layer so they do not have to repeat the same explanations every chat session.

### Who this is for
- directors enabling multiple managers
- platform or enablement leaders creating common AI context
- technical managers tired of re-explaining team language and expectations

### Best surface
- **GitHub.com + Copilot Spaces**

### Repo assets to use
- `knowledge/space-manifests/engineering-management-core.md`
- `knowledge/glossary.md`
- `knowledge/manager-faq.md`
- `knowledge/policies/delivery-policy.md`
- `knowledge/playbooks/pr-review-expectations.md`
- `docs/08-space-blueprints.md`

### Suggested workflow
1. Start from the engineering management core manifest.
2. Add only the most useful sources.
3. Exclude old, noisy, or sensitive material.
4. Test the Space with three common management questions.

### Suggested prompts to test the Space
```text
What should a new manager understand first about how this org delivers software?
```

```text
Summarize the current delivery risks visible from this context.
```

```text
Turn this initiative into a structured issue and identify missing information.
```

### Why this works
The manifest approach forces curation. It prevents the common failure mode where a team throws too much content into the system and then wonders why answers become noisy.

### What to save back
- improvements to the Space manifest
- notes about what sources improved or degraded answer quality
- a short champion guide for how your managers should use the Space

### Common mistakes
- adding entire repositories or huge historical dumps without curation
- including confidential originals that should not be stored there
- assuming Spaces replace durable repository memory

---

## Example 7 — Prepare a focused one-on-one agenda

### What this solves for
Managers want a sharper one-on-one that surfaces progress, blockers, growth, and decisions instead of turning into an unstructured conversation.

### Who this is for
- any people manager
- skip-level leaders preparing targeted check-ins
- new managers learning how to structure coaching conversations

### Best surface
- **GitHub.com** for quick use
- **VS Code** if you want a durable agenda template or note file

### Repo assets to use
- `knowledge/playbooks/one-on-one-prep.md`
- `knowledge/manager-faq.md`
- relevant decision logs or recent status notes if available

### Suggested prompt
```text
Help me prepare for a one-on-one with a senior engineer.
Use:
- knowledge/playbooks/one-on-one-prep.md
- knowledge/manager-faq.md

Based on these notes, create:
- a short agenda
- questions I should ask
- any follow-ups I should check from prior commitments
- risks or decisions I should not miss
```

### Why this works
The playbook gives Copilot a clear structure for the conversation, which leads to a more focused agenda and better coaching questions.

### What to save back
- a reusable one-on-one agenda template under `knowledge/playbooks/`
- follow-up actions in your normal task system if appropriate

### Common mistakes
- using Copilot to replace human judgment in a sensitive conversation
- asking for “feedback questions” with no role, context, or prior note history
- failing to separate coaching from performance-management specifics

---

## Example 8 — Produce incident updates that leadership can trust

### What this solves for
During incidents, managers need updates that are concise, calm, and consistent, especially for senior stakeholders.

### Who this is for
- incident managers
- engineering managers supporting live response
- directors preparing executive-level summaries during a production issue

### Best surface
- **GitHub.com** for rapid drafting during active work
- **VS Code** if you want to save a repeatable incident communication template

### Repo assets to use
- `knowledge/playbooks/incident-comms.md`
- `knowledge/policies/delivery-policy.md`
- optionally a Space with incident issues or notes

### Suggested prompt
```text
Draft an incident update for leadership.
Use:
- knowledge/playbooks/incident-comms.md
- knowledge/policies/delivery-policy.md

Based on these incident notes, produce:
- incident summary
- current impact
- what is known
- what is not yet known
- current mitigation
- next update time
- asks / decisions needed

Separate facts from assumptions.
Do not overstate certainty.
```

### Why this works
The playbook biases Copilot toward stable, repeated communication patterns. That reduces the odds of vague, overly optimistic, or overly technical updates.

### What to save back
- incident communication templates under `knowledge/playbooks/`
- decision logs only if durable policy or architectural decisions were made

### Common mistakes
- asking for an “incident summary” with no structure
- letting the update hide uncertainty
- using the incident channel history itself as the only long-term memory

---

## Example 9 — Break down a big initiative into reviewable work

### What this solves for
A manager or lead has a large initiative that is too broad to assign or track effectively.

### Who this is for
- managers planning quarterly work
- staff-plus engineers partnering on implementation planning
- directors who want visible checkpoints rather than a single giant initiative

### Best surface
- **VS Code** for drafting a Markdown plan
- **GitHub.com** if the result will be turned into issues and milestones

### Repo assets to use
- `.github/agents/implementation-planner.agent.md`
- `knowledge/playbooks/backlog-breakdown.md`
- `knowledge/policies/delivery-policy.md`
- `docs/02-framework-architecture.md`

### Suggested prompt
```text
Use the implementation-planner agent mindset to break this initiative into:
- problem
- goals
- non-goals
- assumptions
- proposed approach
- work breakdown
- dependencies
- risks and mitigations
- validation strategy
- rollout plan
- ownership suggestions

Use:
- knowledge/playbooks/backlog-breakdown.md
- knowledge/policies/delivery-policy.md
- docs/02-framework-architecture.md
```

### Why this works
The implementation planner is tuned to produce manager-visible checkpoints and not just engineering task lists. That is useful for cross-functional alignment.

### What to save back
- a plan under `docs/` or `knowledge/playbooks/`
- individual issues in GitHub
- a decision log if scope or architecture tradeoffs become durable

### Common mistakes
- asking Copilot to “make a plan” without naming goals and non-goals
- skipping validation and rollout thinking
- accepting a plan with no dependency mapping

---

## Example 10 — Produce a research brief for a tooling or process decision

### What this solves for
A leader wants to compare options and make a recommendation, but needs a concise brief instead of a sprawling chat answer.

### Who this is for
- directors comparing AI workflows, tool rollout options, or process changes
- managers preparing a recommendation for leadership
- enablement leads evaluating training or governance models

### Best surface
- **GitHub.com** for fast comparison work
- **VS Code** if the brief will be stored and iterated in Markdown

### Repo assets to use
- `.github/prompts/research-brief.prompt.md`
- `docs/01-research-summary.md`
- `docs/02-framework-architecture.md`
- `docs/07-governance-metrics.md`

### Suggested prompt
```text
Create a research brief comparing two rollout options:
1. train managers first through GitHub.com + Spaces
2. train technical champions first through VS Code + CLI and then cascade to managers

Use:
- docs/01-research-summary.md
- docs/02-framework-architecture.md
- docs/07-governance-metrics.md

Output:
- Question
- Findings
- Implications
- Recommendation
- Risks / open questions
- Suggested next action
```

### Why this works
The research-brief prompt keeps the output decision-oriented. It also anchors the answer in the current framework and governance thinking already captured in the repo.

### What to save back
- the final brief under `docs/`
- a decision log if a real rollout decision is made

### Common mistakes
- asking for a recommendation before framing the decision question clearly
- not stating the options being compared
- failing to capture the recommendation in a durable document

---

## Example 11 — Build manager-friendly repository memory from repeated questions

### What this solves for
The same questions keep appearing: “How do we write issues?”, “What does this term mean?”, “What should I put in a status update?” The team needs durable answers.

### Who this is for
- enablement owners
- directors trying to scale management consistency
- technical leaders tired of answering the same questions repeatedly

### Best surface
- **VS Code** for editing repo files
- **GitHub.com** when using a Space to identify repeated questions

### Repo assets to use
- `.github/agents/context-curator.agent.md`
- `knowledge/glossary.md`
- `knowledge/manager-faq.md`
- `knowledge/source-docs/summaries/`

### Suggested prompt
```text
Review these repeated manager questions and turn them into durable repo memory.
For each question:
- decide whether it belongs in the glossary, FAQ, or a playbook
- draft the Markdown update
- note whether a Space source should be added or refined

Use:
- knowledge/glossary.md
- knowledge/manager-faq.md
- knowledge/source-docs/README.md
```

### Why this works
This is how the repo stops being just a prompt collection and becomes an operating memory system. Repeated questions become shared documentation instead of recurring chat work.

### What to save back
- glossary entries
- FAQ entries
- new playbooks when a topic becomes procedural rather than definitional

### Common mistakes
- treating every question as FAQ material
- mixing glossary terms, procedural guidance, and one-off notes together
- never pruning stale entries

---

## Example 12 — Review a pull request from a manager lens

### What this solves for
Managers often need to review or discuss a PR without doing a full deep technical review. They need to understand what changed, why it matters, what risk it creates, and whether rollout and validation are visible.

### Who this is for
- engineering managers
- directors doing spot review on high-risk changes
- program or product partners who need a management-oriented summary

### Best surface
- **GitHub.com** on the PR itself or inside a Space with relevant PRs
- **VS Code** if reviewing linked files locally

### Repo assets to use
- `knowledge/playbooks/pr-review-expectations.md`
- `knowledge/policies/delivery-policy.md`
- relevant issue or decision log if available

### Suggested prompt
```text
Review this pull request from a manager perspective.
Use:
- knowledge/playbooks/pr-review-expectations.md
- knowledge/policies/delivery-policy.md

Answer:
- what changed
- why it changed
- what risk it introduces
- how it should be validated
- what rollout or release considerations are visible
- what still needs attention
```

### Why this works
The PR review expectations file reframes the review around manager-relevant outcomes instead of line-by-line implementation critique.

### What to save back
- if a durable tradeoff appears, capture it in a decision log
- if repeated review patterns appear, refine the PR playbook

### Common mistakes
- assuming a manager summary is a substitute for engineering review
- ignoring rollout risk because the code change looks small
- not tracing the PR back to acceptance criteria

---

## Example 13 — Teach a non-technical manager to use GitHub Copilot without the CLI

### What this solves for
Some managers will not use VS Code or CLI. They still need a useful, low-friction way to benefit from Copilot.

### Who this is for
- non-technical people managers
- program managers or chiefs of staff supporting engineering leadership
- directors rolling out Copilot across mixed technical skill levels

### Best surface
- **GitHub.com + one or two curated Spaces**

### Repo assets to use
- `knowledge/space-manifests/engineering-management-core.md`
- `knowledge/manager-faq.md`
- `knowledge/examples/prompt-patterns-by-surface.md`
- `docs/05-surface-guide.md`

### Suggested workflow
1. Give them one Space, not five.
2. Give them three starter questions they can safely use.
3. Show them where durable answers live in the repo.
4. Teach them to capture important outputs back into Markdown through a champion if needed.

### Suggested starter questions
```text
What are the most important delivery expectations I should understand as a manager?
```

```text
Turn this rough request into a structured issue and tell me what information is missing.
```

```text
Summarize these notes into a status update and highlight the decisions needed.
```

### Why this works
It removes the need for CLI syntax or IDE behavior and focuses on the problems managers actually face: shaping work, understanding context, and communicating clearly.

### What to save back
- a short internal quick-start guide for non-technical managers
- updates to the Space manifest if they routinely need additional context

### Common mistakes
- forcing every manager to learn CLI or IDE workflows on day one
- giving too many prompts and too many Spaces
- assuming prompt knowledge matters more than curated context

---

## Example 14 — Capture outputs from a workshop so they do not disappear

### What this solves for
A training session, leadership offsite, or team workshop produces useful insight, but the notes are messy and nobody turns them into durable assets.

### Who this is for
- directors running enablement sessions
- managers leading retrospectives or planning workshops
- champions gathering feedback during rollout

### Best surface
- **GitHub.com** for uploaded workshop notes or transcripts
- **VS Code** for converting the results into repo updates

### Repo assets to use
- `.github/prompts/capture-context.prompt.md`
- `.github/skills/context-capture/SKILL.md`
- `knowledge/source-docs/summaries/source-summary-template.md`
- `knowledge/manager-faq.md`
- `knowledge/glossary.md`

### Suggested prompt
```text
Use the context-capture workflow on these workshop notes.
Create:
- a source summary
- glossary additions
- FAQ additions
- recommended playbook updates
- recommended Space updates

Do not copy long passages.
Focus on durable knowledge that should outlive the workshop.
```

### Why this works
This workflow forces separation between ephemeral notes and lasting knowledge. That is one of the main design goals of the repository.

### What to save back
- a workshop summary under `knowledge/source-docs/summaries/`
- updated FAQ and glossary
- new or refined playbooks

### Common mistakes
- saving a transcript but never summarizing it
- mixing workshop commentary with approved operating guidance
- keeping conclusions only in slide decks or chat

---

## Example 15 — Use Copilot CLI with repo files for targeted analysis

### What this solves for
A technical manager or champion wants lightweight, file-grounded analysis without opening an IDE workflow.

### Who this is for
- technical managers comfortable in a terminal
- staff engineers helping enablement efforts
- champions experimenting with fast repo-grounded prompts

### Best surface
- **Copilot CLI**

### Repo assets to use
- any Markdown files relevant to the task
- especially `docs/06-context-memory-strategy.md`, `knowledge/glossary.md`, and `knowledge/policies/`

### Suggested workflow
Work from the repository root and reference the smallest useful file set.

### Suggested prompt pattern
```text
Summarize the practical rules in @docs/06-context-memory-strategy.md for a new manager.
Then propose updates to @knowledge/manager-faq.md based on those rules.
```

Another example:

```text
Compare @knowledge/policies/delivery-policy.md and @knowledge/playbooks/pr-review-expectations.md.
List any gaps or contradictions a manager would care about.
```

### Why this works
The CLI pattern is fast and disciplined. It nudges advanced users to attach concrete files rather than asking broad, context-free questions.

### What to save back
- the final FAQ or policy updates in Markdown
- notes on which file combinations give the best results

### Common mistakes
- attaching too many files at once
- using the CLI for audiences who would be better served by GitHub.com + Spaces
- leaving useful findings in terminal history instead of updating the repo

---

## Choosing the right example for your situation

Use this quick guide:

- If your problem is **onboarding**, start with **Example 1**.
- If your problem is **turning vague requests into executable work**, start with **Example 2**.
- If your problem is **capturing meeting outcomes**, start with **Example 3**.
- If your problem is **working from a PDF or policy document**, start with **Example 4**.
- If your problem is **communicating status**, start with **Example 5**.
- If your problem is **shared manager context**, start with **Example 6**.
- If your problem is **1:1 preparation**, start with **Example 7**.
- If your problem is **incident communication**, start with **Example 8**.
- If your problem is **initiative decomposition**, start with **Example 9**.
- If your problem is **making a recommendation from research**, start with **Example 10**.
- If your problem is **building durable memory**, start with **Example 11**.
- If your problem is **manager-oriented PR understanding**, start with **Example 12**.
- If your audience is **non-technical**, start with **Example 13**.
- If your problem is **preserving workshop outputs**, start with **Example 14**.
- If your audience is **CLI-capable**, start with **Example 15**.

---

## Recommended teaching order for managers

If you are teaching this repository to a group of managers, use this order:

1. **Example 13** — GitHub.com only, simple and accessible
2. **Example 2** — rough request to structured issue
3. **Example 5** — notes to status update
4. **Example 3** — meeting notes to actions and decision log
5. **Example 6** — how shared Spaces improve repeated work
6. **Example 4** — PDF or policy to Markdown memory
7. **Example 1** — onboarding plan
8. **Example 9** — initiative planning
9. **Example 12** — PR review from a manager perspective
10. **Example 11** — how the repo becomes durable memory
11. **Example 10** — research brief and recommendation
12. **Example 7** / **8** / **14** / **15** as advanced or role-specific modules

That order teaches the most transferable habits first:

- start with a curated surface
- ask grounded questions
- save durable outputs
- build memory instead of repeating work

---

## Final rule

A strong example is not just a good prompt.

A strong example does four things:

1. starts from a real management problem
2. uses the smallest, best context from the repo
3. produces a structured output another person can reuse
4. saves the durable part back into Markdown or a curated Space

That is how this repository becomes a working management system rather than a folder of prompts.
