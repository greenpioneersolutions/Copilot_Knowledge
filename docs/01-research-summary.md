# Research summary

Source key: see [`docs/SOURCES.md`](SOURCES.md).

## Executive summary

The current official GitHub and Microsoft guidance points to a **stacked approach**, not a single feature:

- use **GitHub Copilot** for engineering-manager work that sits close to code, repositories, issues, pull requests, delivery planning, and implementation detail [S07]
- use **Microsoft 365 Copilot** as a complement for work grounded in Microsoft 365 content such as mail, meetings, chats, and documents [S07][S10]
- use **Markdown** as the canonical memory layer because GitHub Copilot customization features are file-based and Microsoft’s GitHub Cloud Knowledge connector currently indexes repository metadata plus Markdown and text files rather than issues, pull requests, and comments [S08][S11][S14]
- use **Copilot Spaces** as the shared context layer because Spaces can hold repositories, code, pull requests, issues, free-text notes, transcripts, images, and file uploads, and can be shared with teams [S02][S03][S04]
- treat **Copilot Memory** as helpful but secondary, because it is repository-level, automatically generated, validated against cited code locations, and memories auto-delete after 28 days [S05][S06]

## What GitHub officially offers now

GitHub’s current documentation describes a set of customization options rather than a single “knowledge base” feature:

- **custom instructions** for always-on context [S01][S11][S12]
- **prompt files** for repeatable tasks [S01][S14][S15]
- **custom agents** for specialized personas and tool access [S01][S24][S25]
- **agent skills** for bundled multi-step capabilities [S01][S26][S27]
- **MCP servers** for access to external tools and real-time systems [S01][S13][S40]
- **Spaces** for curated shared context [S02][S03][S04]
- **Copilot Memory** for repository-level learned memory [S05][S06]

VS Code’s current guidance is incremental:
1. initialize project instructions
2. add targeted instruction files
3. add prompt files for repeatable workflows
4. create custom agents for role-specific work
5. add skills and MCP servers only when needed [S13][S21]

## What Microsoft officially says

Microsoft’s current positioning is clear:

- GitHub Copilot is the Copilot for developers who need AI help with writing code [S07]
- Microsoft 365 Copilot is for organizational productivity and data grounded in Microsoft 365 [S07][S10]
- Copilot Chat is web-grounded by default and is not grounded in organizational content in the same way Microsoft 365 Copilot is [S10]
- Agent Builder in Microsoft 365 Copilot is a better fit for individuals or small teams, while Copilot Studio is the fit for broader audiences and more advanced workflows or integrations [S09]

For organizations that want GitHub repository knowledge to appear inside Microsoft 365 Copilot, Microsoft’s GitHub Cloud Knowledge connector currently indexes:
- repository metadata
- Markdown files
- text files

It does **not** index issues, pull requests, or comments in the GitHub Cloud Knowledge connector flow [S08].

## What this means for managers and non-specialists

There is not a single official “manager memory system” built into GitHub Copilot. Instead, the most supportable pattern from the current docs is:

1. **curate context in Spaces**
2. **store durable knowledge in Markdown**
3. **package repeatable manager workflows as prompt files**
4. **use agents for specialized tasks**
5. **measure adoption and enablement separately from raw PR throughput**

GitHub’s own examples now include issue management, onboarding plans, implementation planners, and project planning flows that turn ideas into epics, features, and tasks [S22][S23][S28][S29]. That is the strongest signal for how managers should be trained: **scenario playbooks, not generic prompt tricks**.

## Answer to the PDF question

The strongest recommendation from the combined GitHub and Microsoft documentation is:

> **PDF as source artifact. Markdown as durable memory.**

Why:
- Spaces can include file uploads and rich context, so PDFs can still be used when needed [S02][S03]
- GitHub customization features are built around Markdown files in the repository [S01][S11][S14]
- Microsoft’s GitHub Cloud Knowledge connector indexes Markdown and text files from repositories [S08]

So the best operating pattern is:
- keep the original PDF only when policy allows
- create a Markdown sidecar summary
- update glossary / FAQ / decisions / playbooks when the content is durable
- add the best of that material to a Space instead of dumping everything into one place

## Surface-by-surface implications

### GitHub.com
Best entry point for most managers because it is the easiest place to use:
- Spaces [S02][S03][S04]
- shared GitHub context
- issue creation and project planning [S29]
- chat attachments using `@` mentions [S42]

### VS Code
Best for technical managers and champions because it supports:
- `#file`, `#folder`, `#symbol` context references [S20][S41]
- project-wide and path-specific instructions [S12]
- prompt files [S14]
- custom agents [S13]
- incremental AI customization flows [S13][S21]

### Copilot CLI
Best for advanced users because it supports:
- plan mode [S16]
- `/research` [S17]
- file attachment with `@relative/path` [S16]
- trusted-directory and permission controls [S18][S19]
- custom instructions, agents, and skills [S16][S27][S43]

## A noteworthy documentation inconsistency

GitHub’s docs currently appear slightly inconsistent on **prompt-file support in Copilot CLI**:

- the customization cheat sheet shows prompt files as supported on GitHub.com and Copilot CLI [S01]
- the prompt files tutorial still says prompt files are in preview and only available in VS Code, Visual Studio, and JetBrains IDEs [S15]

Because of that inconsistency, the safest operational guidance is:
- treat prompt files as **IDE-first**
- verify GitHub.com / CLI support in your own environment before making it central to training

## Memory guidance

Use two layers:

### 1. Human-authored memory
This should be your source of truth:
- policies
- glossary
- FAQ
- decision logs
- playbooks
- onboarding docs
- space manifests

All in Markdown.

### 2. Copilot-authored memory
Useful, but secondary:
- Copilot Memory reduces repeated prompting [S05]
- memories are validated against cited code locations before use [S05]
- memories auto-delete after 28 days [S06]

That makes Copilot Memory a productivity feature, not a governance-ready knowledge system.

## Measurement guidance

GitHub’s usage metrics provide visibility into adoption, engagement, feature use, model use, and pull request lifecycle trends [S32][S33]. GitHub’s own trial guidance recommends defining goals, analyzing adoption and engagement, and incorporating qualitative feedback [S34]. GitHub also recommends leading rollout with specific engineering goals rather than generalized output pressure [S31][S35].

That means a mature measurement stack should include:
- active users
- feature adoption
- agent adoption
- qualitative feedback
- task-cycle improvements tied to concrete team goals

and should not rely on PR throughput alone.

## Recommended plan

1. Build a Markdown-first knowledge repo
2. Create one or two shared Spaces
3. Teach managers GitHub.com first, VS Code second, CLI third
4. Train using manager scenarios:
   - issue intake
   - onboarding plan
   - status update
   - meeting notes to actions
   - decision log
   - feature / rollout plan
5. Measure activation, adoption, and quality, not only throughput

## Bottom line

The best current framework for managers is not “a better prompt.” It is:

- **curated context**
- **Markdown memory**
- **repeatable workflows**
- **shared Spaces**
- **selective use of agents / skills / CLI**
- **measured rollout**
