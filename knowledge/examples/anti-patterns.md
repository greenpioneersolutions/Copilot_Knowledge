# Anti-patterns

## Giant context dump
“Here are 14 PDFs and a transcript. Tell me everything.”

Why it fails:
- poor signal-to-noise
- no durable structure
- hard to review later

## No output structure
“Can you help with this project?”

Why it fails:
- vague objective
- hard to compare outputs
- easy to miss risks and assumptions

## Chat-only memory
“We had a great answer last week but I didn’t save it.”

Why it fails:
- no durable knowledge
- no team reuse
- no review trail

## One mega instructions file
Putting everything into one giant instructions file can become noisy and hard to maintain.

Better:
- repo-wide instructions for defaults
- path-specific instructions for local rules
- prompt files for recurring tasks
