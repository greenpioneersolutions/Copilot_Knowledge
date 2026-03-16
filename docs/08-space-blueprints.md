# Space blueprints

Source key: see [`docs/SOURCES.md`](SOURCES.md).

## Why Spaces matter

GitHub Copilot Spaces organize the context that Copilot uses to answer questions [S02]. They can include repositories, code, pull requests, issues, notes, transcripts, images, and uploaded files [S02]. Shared Spaces help teams avoid repeated explanations and stay aligned [S39].

## Space design principles

- build a few Spaces with clear purpose
- curate, do not dump
- use organization-owned Spaces when team reuse matters [S03]
- refresh Space contents as decisions and docs evolve
- use the repo as the durable memory layer and Spaces as the shared retrieval layer

## Recommended Space 1 — Engineering Management Core

### Purpose
Shared context for managers who need answers about delivery, architecture, operating model, and expectations.

### Add
- the most relevant repositories
- a few representative issues and pull requests
- `knowledge/glossary.md`
- `knowledge/manager-faq.md`
- `knowledge/policies/delivery-policy.md`
- `knowledge/playbooks/pr-review-expectations.md`
- key architecture or operating notes
- curated transcripts or notes only if valuable

### Avoid
- every repository in the org
- large raw-doc dumps
- low-signal historical clutter

### Starter prompts
- Summarize current delivery risk for this team.
- What would a new manager need to understand first?
- Turn this rough initiative into an issue with acceptance criteria.

## Recommended Space 2 — Onboarding

### Purpose
Accelerate new manager or engineer ramp-up.

### Add
- team charter
- operating model
- glossary
- first-30 / first-90-day guidance
- key architecture docs
- common issues / examples
- onboarding-specific notes or transcripts

### Starter prompts
- Build a 30-60-90 day onboarding plan for a new engineering manager.
- What are the most important terms and decisions a new hire must understand?
- What are the recurring pitfalls for onboarding in this area?

## Recommended Space 3 — Delivery and Architecture Review

### Purpose
Support planning, tradeoff analysis, readiness reviews, and release decisions.

### Add
- delivery policy
- representative roadmap issues
- recent implementation plans
- decision logs
- risk notes
- release-readiness or incident-learning notes

### Starter prompts
- Summarize the main risks before release.
- What dependencies threaten the current plan?
- Which decisions should be formalized into ADRs?

## Important IDE limitation

When using Spaces in the IDE, repository context is not currently supported [S04]. Also, Spaces that contain only a repository are limited for IDE access through the GitHub MCP server [S39]. That is one reason to include notes, docs, or other non-repository sources in important Spaces.

## Space curation checklist

- [ ] name is specific
- [ ] purpose is explicit
- [ ] top files are curated
- [ ] stale or noisy content excluded
- [ ] related repo memory exists in Markdown
- [ ] starter prompts documented
- [ ] ownership is assigned
- [ ] quarterly review scheduled

## Relationship to this repo

This repository includes starter manifests under:
- `knowledge/space-manifests/engineering-management-core.md`
- `knowledge/space-manifests/onboarding-space.md`

Use those as templates, then create the actual Spaces in GitHub.
