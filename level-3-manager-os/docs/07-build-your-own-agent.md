# Build your own agent

Do this only after the shared catalog is working.

## A new agent is justified only if

- a real workflow repeats often
- the current four custom agents do not fit it
- the workflow needs a persistent persona, not just a one-off prompt
- you can explain when to use it in one sentence

## Questions to ask before adding one

1. What problem does this solve?
2. Why can the current agents not solve it?
3. Should this be a template instead of an agent?
4. Should this be a short note in the team Space instead of an agent?
5. Who will maintain it?

## Design rules

- prefer read-only tools by default
- write the purpose in one sentence
- keep instructions specific
- keep the output shape predictable
- add handoffs only if they reduce confusion

## Strong warning

Agent count is a tax.

Every new agent increases:
- teaching cost
- maintenance cost
- user confusion
- overlap with existing agents

That is why the default answer should usually be **no**.
