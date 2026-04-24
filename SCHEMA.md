# Wiki Schema

## Domain
AI/ML Engineering, Long-running Applications, and General LLM Knowledge.

## Conventions
- File names: lowercase, hyphens, no spaces (e.g., `transformer-architecture.md`)
- Every wiki page starts with YAML frontmatter
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`
- **Provenance markers:** Append `^[raw/articles/source-file.md]` at the end of paragraphs.

## Frontmatter
```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [from taxonomy below]
sources: [raw/articles/source-name.md]
confidence: high | medium | low
---
```

## Tag Taxonomy
- Models: model, architecture, benchmark, training
- Engineering: design, reliability, long-running, production
- People/Orgs: person, company, lab, open-source
- Techniques: optimization, fine-tuning, inference
- Meta: comparison, timeline, summary
