# Research foundation

This document explains why the three levels look the way they do.

## Product facts that shape the design

### 1) GitHub.com already covers the beginner use cases
GitHub Copilot Chat is available on the GitHub website. On GitHub.com, managers can already:
- ask repository-level questions
- work inside repository, issue, PR, and Space context
- create or update issues from natural language or screenshots
- create pull request summaries
- request Copilot code review

That makes GitHub.com the correct beginner surface.

### 2) Spaces are the beginner memory layer
Spaces can include repositories, code, pull requests, issues, transcripts, notes, images, and file uploads. GitHub explicitly positions Spaces as a way to reduce repeated questions and support onboarding beyond chat history.

That makes one shared Space the right Level 1 memory model.

### 3) Spaces still need curation
GitHub warns that Spaces have context limits and Copilot only processes a portion of the content in a Space for a given response.

That is why this framework recommends:
- one Space per team or workstream
- a small curated source set
- short Markdown notes instead of giant dumps

### 4) VS Code is where the next real jump happens
In VS Code, Copilot Chat offers Ask, Edit, Agent, and Plan modes. VS Code also supports custom agents. This is the first place where it becomes worth teaching deeper workflow control.

That makes VS Code a Level 2 surface, not a Level 1 surface.

### 5) Prompt files are real, but not beginner material
Prompt files are still public preview and are only available in VS Code, Visual Studio, and JetBrains IDEs.

That is why this starter set does **not** make prompt files central. It keeps the learning path focused on fewer concepts.

### 6) CLI is powerful, but should be introduced carefully
Copilot CLI supports interactive and programmatic use, file mentions with `@`, slash commands, research mode, and model switching. It can work on your behalf, but GitHub stresses that you should review permissions, file edits, and risky commands carefully.

That is why CLI is kept light in Level 2 and deliberate in Level 3.

### 7) Delegation only works with clean task framing
When you assign an issue to Copilot coding agent, it gets the issue title, description, current comments, and your additional instructions at assignment time. Later issue comments are not picked up. Follow-up should happen on the pull request.

That means delegation is only safe after users learn how to shape a good issue and review the resulting PR.

## The manager time-sink research that shapes the design

### Communication and information hunting are huge
Microsoft reports that 62% of survey respondents struggle with too much time spent searching for information. The same Work Trend Index says the average employee spends 57% of time communicating and 43% creating.

Atlassian's 2025 State of Teams reports that leaders and teams waste 25% of their time just searching for answers.

Implication: the program must first solve **finding context** and **compressing communication work**.

### Managers are overloaded with decisions and bureaucracy
McKinsey reports that respondents spend 37% of working time making decisions and that more than half of that time is thought to be spent ineffectively. McKinsey also notes that middle managers are often pulled into nonmanagerial work and organizational bureaucracy instead of focusing on developing people and driving outcomes.

Implication: the program must help managers turn rough information into better plans, clearer decisions, and faster follow-through.

### Engineering managers lose focus time to meetings
Clockwise's engineering benchmark says the average engineering manager spends 17.9 hours per week in meetings and has only 10.4 hours of focus time left. Treat this as directional, not universal, because it is vendor research.

Implication: the program should aggressively reduce the work of:
- summarizing
- drafting updates
- translating technical detail for stakeholders
- turning notes into usable artifacts

### Change approval should move closer to the work
DORA says change approvals work better when they are implemented through peer review inside the development process and supported by automation, rather than heavyweight external gatekeeping.

Implication: managers should use Copilot to understand PRs, spot risk, and improve issue quality, but not become manual bottlenecks.

## What this means in practice

### Level 1 should solve:
- context finding
- issue shaping
- PR understanding

### Level 2 should solve:
- deeper repo-grounded analysis
- better plans
- faster technical-to-manager translation
- light research in the terminal

### Level 3 should solve:
- standardized communication
- decision logging
- repeatable planning
- safe delegation of bounded work

## Metrics caution

Do not judge the beginner program only by GitHub usage dashboards.

GitHub says the dashboard is based on IDE telemetry and may appear up to three full UTC days behind. GitHub also says Copilot Spaces are not fully recorded in the activity report. That means a web-first Level 1 rollout can be undercounted if you look only at those dashboards.

Use a mixed scorecard:
- workflow completion
- issue quality
- PR understanding quality
- repeated-question reduction
- self-reported time saved
- selected GitHub metrics where they actually apply

See the Level 1, 2, and 3 repos for suggested measures.
