# Governance and metrics

Source key: see [`docs/SOURCES.md`](SOURCES.md).

## Governance objectives

- protect sensitive information
- keep context high quality
- measure real adoption
- tie usage to concrete goals
- avoid brittle process theater

## Governance baseline

## 1. Information handling
Customize `knowledge/policies/ai-usage-policy.md` before broad rollout.

At minimum define:
- what may be put into Git
- what may be attached to a Space
- what must stay in approved systems
- redaction expectations
- review requirements for AI-generated output

## 2. Context quality
Curate aggressively.
Do not assume “more context” is always better.

A small, well-maintained set of summaries, FAQs, decisions, and playbooks will generally outperform uncurated dumps.

## 3. CLI permissions
Copilot CLI has meaningful permission and scope controls:
- current working directory / subdirectory scope by default [S18][S19]
- trusted directories [S19]
- permission prompts before file modification and dangerous commands [S18]

This is a reason to treat CLI as an advanced lane rather than the default manager lane.

## 4. Hooks and automation
Hooks can support logging, guardrails, and policy enforcement [S30], but they should usually come **after** the team has a working baseline of:
- instructions
- prompt files
- Spaces
- memory capture

## What GitHub metrics can tell you

GitHub usage metrics provide visibility into:
- engagement
- activity
- code generation
- pull request lifecycle trends [S33]

The usage metrics dashboard can show:
- adoption trends
- feature trends
- model trends
- language trends [S32]

GitHub’s trial guidance recommends:
- define trial goals first
- review adoption and engagement
- add qualitative feedback
- decide whether to expand based on evidence [S34]

## Important caveats

### Dashboard freshness
The usage dashboard may lag by up to three full UTC days [S32].

### Coverage caveat
GitHub’s usage metrics are derived from multiple Copilot surfaces but some data depends on IDE telemetry, and GitHub.com chat activity is not included in every metrics view [S33].

### Implication
Do not build governance around a single dashboard number.

## Recommended measurement stack

## Adoption
- licensed users
- active users
- weekly active users
- first-use activation rate

## Engagement
- feature usage
- agent adoption
- breadth of workflow usage

## Workflow effectiveness
Pick a few concrete internal measures, for example:
- time from rough request to quality issue
- onboarding readiness after 30 days
- decision-log turnaround time
- reduction in repeated manager questions
- review-loop reduction on selected teams

## Quality and trust
- satisfaction survey
- manager confidence
- engineer confidence
- perceived usefulness of Spaces and repo memory
- output review burden

## What not to optimize blindly

Be careful with:
- PR throughput alone
- accepted lines alone
- raw prompt counts
- number of generated files
- “more AI usage” as a proxy for value

GitHub’s own engineering-goal guidance recommends starting with specific goals and monitoring results relative to those goals [S31][S35].

## Suggested review cadence

### Weekly
- collect friction points
- update FAQ and glossary
- identify failing prompts or stale docs

### Monthly
- review adoption trends
- compare against concrete goals
- inspect whether Spaces are being used well
- identify where more enablement is needed

### Quarterly
- revisit policy
- retire stale prompts
- archive stale summaries
- update training materials

## Lightweight governance checklist

- [ ] AI usage policy reviewed
- [ ] sensitive-content rules documented
- [ ] first Space curated
- [ ] repo memory structure in use
- [ ] champions identified
- [ ] at least one qualitative feedback loop active
- [ ] at least one monthly metric review in place
