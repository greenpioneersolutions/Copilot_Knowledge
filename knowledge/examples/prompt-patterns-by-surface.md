# Prompt patterns by surface

## GitHub.com
- Use a Space when possible
- attach context with `@`
- ask for a structured output

Example:
`Use the Engineering Management Core space and summarize the current release risks.`

## VS Code
- use `#file`, `#folder`, `#symbol`
- run prompt files from `.github/prompts/`

Example:
`#file:knowledge/policies/delivery-policy.md turn this into an onboarding note for a new manager.`

## Copilot CLI
- use `@relative/path`
- use plan mode before implementation
- use `/research` for deeper work

Example:
`Summarize @knowledge/manager-faq.md into a short training handout.`
