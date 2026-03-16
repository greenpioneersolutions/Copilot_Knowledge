# Source document workflow

Use this folder when you need to preserve the relationship between a raw source artifact and a durable Markdown summary.

## Recommended pattern

### Originals
Place committed originals in:
- `knowledge/source-docs/originals/`

Only do this when:
- policy allows it
- the repo is the right storage location
- the original is worth retaining here

### Summaries
Create a Markdown sidecar summary in:
- `knowledge/source-docs/summaries/`

That summary should capture what Copilot and humans are actually likely to reuse.

## Summary requirements

Each sidecar summary should include:
- source path or external location
- owner
- date
- sensitivity notes
- scope
- key points
- manager implications
- open questions
- links to glossary / FAQ / decisions if relevant

## If the original cannot be committed

- do not commit it
- create the summary anyway
- note the external source-of-truth location
- capture any sensitivity constraints in the summary

## Related files

- `knowledge/glossary.md`
- `knowledge/manager-faq.md`
- `knowledge/decisions/`
- `knowledge/space-manifests/`
