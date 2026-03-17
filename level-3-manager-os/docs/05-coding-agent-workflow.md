# Built-in coding agent workflow

The coding agent is the fifth agent in the Level 3 system.

It is built in to GitHub Copilot, so it is not a file in this repository.

## Use it last, not first

The coding agent should enter the workflow only after:
- the problem is clear
- acceptance criteria exist
- dependencies are visible
- the issue is small enough to review

## Recommended flow

### Step 1
Use **Manager Analyst** to understand the area and likely risks.

### Step 2
Use **Delivery Planner** to shape the work into a better issue.

### Step 3
Submit or refine the issue using the issue template in `knowledge/templates/CODING_AGENT_ISSUE_TEMPLATE.md`.

### Step 4
Assign the issue to Copilot coding agent.

### Step 5
Review the resulting pull request carefully.

### Step 6
If changes are needed, leave follow-up comments on the pull request.

## Important behavior to remember

The coding agent uses the issue title, issue description, current comments, and any additional instructions you provide at assignment time.

Later comments on the issue are not picked up.

So if the requirement changes after the PR is raised, leave the follow-up on the pull request.

## Good uses

- bounded bug fix
- small refactor
- targeted test coverage increase
- documentation improvement linked to code

## Bad uses

- vague platform strategy
- architecture decisions not made yet
- high-ambiguity multi-team work
- anything nobody will review carefully
