# Core workflows

## Workflow 1 — Repo to briefing

### Solves for
- I need a quick architecture or delivery briefing.
- I need to prepare for a leadership or product conversation.
- I need technical detail translated into manager language.

### Use
VS Code Ask mode or Manager Analyst.

### Prompt
> Explain this repo or feature area in plain English for a manager.  
> Focus on purpose, current patterns, likely risks, and what a leader should ask next.

### Save back
Capture the best summary in a short Markdown briefing note.

---

## Workflow 2 — Repo to plan

### Solves for
- I need a rollout plan.
- I need to break a fuzzy ask into smaller work.
- I need acceptance criteria and dependencies.

### Use
VS Code Plan mode or Delivery Planner.

### Prompt
> Create a delivery plan for this request.  
> Include scope, assumptions, dependencies, rollout steps, test or validation steps, risks, and open questions.

### Save back
Create or update an issue, epic note, or rollout plan Markdown file.

---

## Workflow 3 — Repo to status update

### Solves for
- I need a useful weekly update.
- I need to summarize changes without reading everything manually.
- I need a clean upward communication draft.

### Use
Manager Analyst first, then Communications pattern from the templates.

### Prompt
> Based on the current repo, issue, and PR context, draft a status update for leadership.  
> Include what changed, what's at risk, what decisions are needed, and what help is needed.

### Save back
Use the status template and review before sending.

---

## Workflow 4 — Terminal help without terminal overload

### Solves for
- I need a quick project overview from the current directory.
- I need research or a second opinion without leaving VS Code.

### Use
Integrated terminal with Copilot CLI.

### Prompt examples
- `Give me an overview of this project.`
- `@README.md summarize setup and known risks`
- `/research Compare the current auth flow with the repo's test coverage and likely weak spots`
