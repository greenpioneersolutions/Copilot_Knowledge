# Surface guide

Source key: see [`docs/SOURCES.md`](SOURCES.md).

## Goal

Choose the right Copilot surface for the job, then reference context correctly.

## Quick decision guide

| Surface | Best for | Primary context method | Recommended users |
|---|---|---|---|
| GitHub.com | shared repo questions, issues, PRs, project planning, Spaces | Spaces, repo context, `@` mentions | managers, leads, broad team |
| VS Code | technical planning, file-targeted work, prompt files, agents | `#file`, `#folder`, `#symbol`, repo instructions | technical managers, champions |
| Copilot CLI | plan / research / terminal-native work / automation | `@relative/path`, plan mode, `/research` | advanced users |
| Microsoft 365 Copilot | M365-grounded mail, meetings, docs, chats | tenant data and M365 grounding | managers and business users |

## GitHub.com

### Use when
- you want the easiest shared entry point
- you are working inside GitHub issues, pull requests, or repositories
- you want to use a shared Space
- you are answering a manager question with team-grounded context

### Context patterns
- work inside a **Space** whenever possible [S02][S03][S04]
- use `@` mentions to attach files, issues, pull requests, repositories, and other supported items in chat [S42]

### Example prompts
- `Use the Engineering Management Core space to summarize the current delivery risks.`
- `@repo-name @issue/123 turn this request into a structured issue with acceptance criteria.`
- `Review these pull requests and summarize what a manager should know for release readiness.`

## VS Code

### Use when
- you need file-level precision
- you want repo instructions, prompt files, agents, or skills
- you are a technical manager or champion
- you want to generate or update Markdown artifacts in the repo

### Context patterns
- `#file` for a specific file [S20]
- `#folder` for a focused folder [S41]
- `#symbol` for a specific code symbol [S41]
- prompt files and instructions stored in the repo [S12][S14]

### Example prompts
- `#file:knowledge/policies/delivery-policy.md convert this into a short onboarding briefing.`
- `#folder:knowledge/playbooks compare these playbooks and suggest what is missing for managers.`
- `/issue-intake create a GitHub issue from the active notes.`

## Copilot CLI

### Use when
- you prefer terminal workflows
- you want plan mode before changes
- you want `/research`
- you want to work with files using relative paths
- you are comfortable with permission boundaries

### Context patterns
- attach a file with `@relative/path/to/file` [S16]
- use **plan mode** before implementation [S16]
- use `/research` for deeper investigation [S17]
- check permissions / trusted directories when needed [S18][S19]

### Example prompts
- `Summarize @knowledge/policies/delivery-policy.md for a new engineering manager.`
- `Create a decision log from @notes/release-readiness-notes.md and save a draft under knowledge/decisions/.`
- `/research Compare the current guidance in this repo with the latest GitHub Copilot Spaces documentation.`

## Prompt files

### Best for
- recurring tasks
- standardized manager workflows
- repeatable outputs

### How to reference files inside prompt files
GitHub and VS Code docs allow prompt files to reference other workspace files using:
- relative Markdown links
- `#file:relative/path` syntax [S11][S14]

### Example
Inside a prompt file:

```md
Use [Delivery policy](../../knowledge/policies/delivery-policy.md)
and #file:../../knowledge/glossary.md as context.
```

## Spaces

### Best for
- shared context across managers
- onboarding
- architecture or delivery knowledge
- reducing repeated explanations [S02][S04][S39]

### Important limitation
When using Spaces in the IDE, repository context is not currently supported; other Space sources and instructions are available [S04]. Spaces that contain only a repository are also limited for IDE access [S39].

## Microsoft 365 Copilot

### Use when
- the question is mostly about meetings, mail, docs, or chat
- the grounding you need is in Microsoft 365 rather than GitHub [S07][S10]

### Keep in mind
The GitHub Cloud Knowledge connector for Microsoft 365 Copilot currently indexes repository metadata, Markdown, and text files—not issues, pull requests, or comments [S08].

## Model guidance

GitHub Copilot supports multiple AI models and an Auto model option [S36][S37][S38].

### Practical recommendation
- default to **Auto** unless a team has a specific reason not to [S37][S38]
- teach users to choose models based on task characteristics, not model branding [S36]
- avoid over-fitting training materials to a single named model because model availability and policy can change

## Recommended default order for manager enablement

1. **GitHub.com + Spaces**
2. **VS Code**
3. **Copilot CLI**

That order keeps the barrier to entry low while still giving advanced users room to grow.
