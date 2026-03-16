# AGENTS.md

This repository exists to help managers and engineering leaders use GitHub Copilot effectively and consistently.

## Default behavior for AI agents

- Prefer **Markdown** as the durable output format.
- Treat PDFs, slides, and spreadsheets as source artifacts unless a richer format is specifically needed.
- When new knowledge is likely to matter later, write or update a file under `knowledge/` or `docs/` instead of leaving it only in chat.
- Keep output concise, structured, and reusable.
- Preserve source traceability:
  - identify where information came from
  - link to official docs when documenting platform behavior
  - note assumptions and open questions
- Avoid inventing policy. If a policy is missing, create a template and label it as a draft.
- Prefer updating:
  - `knowledge/glossary.md` for stable definitions
  - `knowledge/manager-faq.md` for recurring questions
  - `knowledge/decisions/` for durable decisions
  - `knowledge/source-docs/summaries/` for sidecar summaries of raw source material

## Repository intent

This repo is a **framework and starter pack**, not a finished product. Favor examples that are:
- easy to copy
- easy to adapt
- safe for a managed enterprise environment

## File conventions

- `docs/` = research, architecture, rollout, governance
- `knowledge/` = durable operational memory
- `.github/prompts/` = reusable manager workflows
- `.github/agents/` = specialized Copilot personas
- `.github/skills/` = bundled multi-step capabilities

## If unsure where to place a new artifact

- reusable guidance -> `docs/`
- durable team knowledge -> `knowledge/`
- a repeatable chat workflow -> `.github/prompts/`
- a specialized behavior/persona -> `.github/agents/`
- a multi-step capability with instructions/resources -> `.github/skills/`
