# Three-level blueprint

## The pitch

This program should feel like a ramp, not a cliff.

- **Level 1 — Try It** removes choices and creates one fast win.
- **Level 2 — Work With It** adds deeper context and a little more control.
- **Level 3 — Scale It** adds repeatable agents, delegation, and governance.

The design principle is simple:

> do not teach a new user the backend of Copilot  
> teach them one surface, one habit, and a few jobs-to-be-done

## Why this structure is right

### Why Level 1 is web-only
GitHub.com already gives a beginner enough value:
- Copilot Chat on GitHub
- Copilot Spaces
- issue creation from natural language or screenshots
- pull request summaries
- Copilot code review

That means a new manager can get value without installing anything or learning editor workflows.

### Why VS Code starts at Level 2
VS Code is where the next set of valuable capabilities appears:
- Ask mode
- Plan mode
- Edit mode
- custom agents
- stronger file and workspace context

That is useful, but it is not beginner-simple.

### Why CLI is only light in Level 2
CLI is powerful, but it feels advanced to most managers. Keeping it inside the VS Code terminal makes it adjacent to the work instead of a separate world. The user only needs a few moves:
- `copilot`
- `@path/to/file`
- `/research TOPIC`
- `/model`

### Why delegation waits for Level 3
The built-in coding agent is useful only when the task is well scoped. If the issue is vague, the agent inherits that vagueness. So delegation should come after people know how to:
- state the problem clearly
- define acceptance criteria
- review output
- leave follow-up comments in the pull request

## The level model

| Level | Name | Surface | What the learner gets | What stays hidden |
|---|---|---|---|---|
| 1 | Try It | GitHub.com + one shared Space | three practical workflows | VS Code, CLI, prompt files, custom agents |
| 2 | Work With It | VS Code + light CLI | better planning, better summaries, deeper repo context | coding agent, too many agents, advanced automation |
| 3 | Scale It | VS Code + GitHub.com + small shared agent catalog | repeatable manager workflows and safe delegation | agent sprawl, heavy MCP work, over-engineered customization |

## The problems each level solves

### Level 1
**Solves for**
- I am new to Copilot and do not know where to start.
- I need the repo or workstream explained in plain English.
- I have rough notes and need a good issue.
- I need to understand a PR as a manager.

**Does not solve**
- deeper technical planning
- reusable custom agent patterns
- task delegation to the coding agent

### Level 2
**Solves for**
- I need more grounded answers from the actual codebase.
- I want better plans, briefs, and rollout notes.
- I sometimes need terminal help, but I do not want to live in a terminal.
- I want two shared personas so I do not have to re-teach Copilot every time.

**Does not solve**
- large-scale delegation
- org-wide governance
- a broad agent catalog

### Level 3
**Solves for**
- repeated manager work should be standardized
- status updates and communications should be faster
- decision capture should stop living in chat history
- well-formed work can be delegated safely
- champions need a simple agent catalog they can extend over time

## The Level 3 agent rule

Do not create an agent for every task.

Use a small catalog that maps to the real time sinks of engineering managers:
1. understanding context
2. planning delivery
3. drafting communication
4. capturing decisions
5. delegating bounded engineering work

That is why the Level 3 design uses **four custom agents plus the built-in Copilot coding agent**.

## Strong recommendation

- Most non-technical or GitHub-light managers should stop at **Level 1**.
- Technical managers who regularly answer repo, issue, or PR questions should move to **Level 2**.
- Champions, senior managers, directors, and platform leads should own **Level 3**.

## What not to do

- do not start new users in VS Code
- do not start new users with custom agents
- do not teach prompt files before the learner can explain when they would help
- do not judge Level 1 only through GitHub usage dashboards
- do not create more than a handful of shared agents

See `RESEARCH_FOUNDATION.md` and the level repos for the full rationale.
