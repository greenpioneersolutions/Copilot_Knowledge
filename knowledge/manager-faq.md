# Manager FAQ

## Should I store PDFs or Markdown?

Use **Markdown as the primary memory layer**.
Keep PDFs only as source artifacts when policy allows and when the original matters later.

## How do I reference files in prompts?

### GitHub.com
Use a Space when possible.
Use `@` mentions to attach relevant context.

### VS Code
Use:
- `#file`
- `#folder`
- `#symbol`

### Copilot CLI
Use:
- `@relative/path/to/file.md`

### Prompt files
Reference files with:
- relative Markdown links
- `#file:relative/path`

## Where should I put durable knowledge?

Usually in one of these:
- glossary
- FAQ
- policy summary
- playbook
- decision log
- source-doc summary

## What belongs in a Space?

Put in a Space the curated material that should ground repeated questions:
- key repos
- representative issues / pull requests
- glossary
- FAQ
- playbooks
- policy summaries
- selected notes or transcripts

## What should not be my main strategy?

- giant PDF dumps
- one huge instruction file
- depending on chat history as memory
- teaching only “prompt tips” without context discipline

## Is Copilot Memory enough?

No.
Copilot Memory is useful, but it is not your main durable memory system.
Use human-authored Markdown as the source of truth.

## How should I teach other managers?

Teach:
1. which Copilot to use
2. how context works
3. how to run a few repeatable workflows
4. how to save durable outputs back into the repo

## How many workflows should I start with?

Five to seven is a good first pack:
- issue intake
- onboarding plan
- status update
- meeting notes to actions
- decision log
- rollout plan
- research brief

## Where do I start if my peers are not very technical?

Start with:
- GitHub.com
- one shared Space
- prompt-file examples
- manager workflow demos
- no CLI at first
