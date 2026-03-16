# Copilot Agent Pack for Mixed Business + Engineering Personas

This pack includes:
- 7 custom agents in `.github/agents/`
- repository-wide Copilot instructions in `.github/copilot-instructions.md`
- 3 reusable skills in `.github/skills/`
- durable context templates in `docs/copilot/`

## Included agents
- `business-request-translator`
- `implementation-planner`
- `intake-triage`
- `change-explainer`
- `release-readiness`
- `delivery-risk-manager`
- `enterprise-workflow-assistant` (optional front door)

## Installation
For a single repository:
1. Copy `.github/agents/*.agent.md` into your repository.
2. Copy `.github/copilot-instructions.md` into your repository.
3. Copy `.github/skills/` if you want the reusable task skills.
4. Copy `docs/copilot/` if you want durable “memory-like” context files.

For organization / enterprise level rollout:
- Test agents in `.github/agents/` first.
- In a `.github-private` repository, move released agent profiles into `agents/` for broader org or enterprise availability.

## Suggested rollout order
1. `enterprise-workflow-assistant` (optional front door)
2. `business-request-translator`
3. `implementation-planner`
4. `change-explainer`
5. `release-readiness`
6. `intake-triage`
7. `delivery-risk-manager`

## CLI examples
```bash
copilot --agent business-request-translator --prompt "Turn this stakeholder request into a backlog-ready story: Sales wants a weekly list of accounts missing owner assignments so regional managers can follow up before forecast review."
```

```bash
copilot --agent implementation-planner --prompt "Create an implementation plan for the request in docs/copilot/intake/2026-03-16-missing-account-owners.md"
```

```bash
copilot --agent change-explainer --prompt "Explain PR #123 in plain English for an engineering manager and support lead."
```

## Notes on continuity
GitHub Copilot Memory is repository-scoped and auto-deletes memories after 28 days unless they are refreshed. This pack therefore treats `docs/copilot/*` as the durable continuity layer and uses skills plus repo instructions to keep those docs updated.
