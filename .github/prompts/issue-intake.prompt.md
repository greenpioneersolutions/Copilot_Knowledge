---
name: issue-intake
description: Turn a rough request into a well-structured GitHub issue
agent: ask
---
Use the following files as context:

- [Delivery policy](../../knowledge/policies/delivery-policy.md)
- [PR review expectations](../../knowledge/playbooks/pr-review-expectations.md)
- [Good prompts](../../knowledge/examples/good-prompts.md)

Turn the user's rough request into a Markdown issue with these sections:

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

Rules:
- Ask only the minimum number of follow-up questions if key information is missing.
- If information is missing but the task can still move forward, state assumptions explicitly.
- Favor concrete, testable acceptance criteria.
- Keep the issue readable by managers and engineers.
