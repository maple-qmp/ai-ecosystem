---
version: 1
updated: 2026-11-04
auto_suggestion_count: 0
---

# Wiki Schema Configuration

This file governs how the LLM builds and maintains your Wiki. Edit it freely.
Ecosystem-specific rules live in [[conventions]] and take precedence where they add fields.

## Wiki Structure
- Entity pages: `entities/`
- Concept pages: `concepts/`
- Source pages: `sources/`
- Layer maps (human-curated, do not auto-generate): `maps/`
- Index: `index.md`
- Log: `log.md`

## Extra Frontmatter (AI ecosystem)
Every entity and concept page MUST also carry:
- `layer:` — one of L0, L1, L2, L3, L4, L5, X (see conventions)
Entity pages SHOULD also carry, when known:
- `kind:` — lab | company | model-family | model | infra | framework | app | dataset | benchmark | person
- `org:` — wiki-link to the owning organization entity
- `released:` — first release, "YYYY" or "YYYY-MM"
- `open_weights:` — true | false (models only)
- `competitors:` / `depends_on:` — arrays of wiki-links to entities
- `status:` — active | deprecated | rumor
Never remove these fields when merging. Never edit the `## 我的判断` section.

## Entity Page Sections
1. **描述**: 3-6 sentences with concrete facts, bidirectional links
2. **生态位置**: layer map link, upstream dependencies, competitors
3. **时间线**: dated bullets, oldest first — events go here, not on their own pages
4. **相关实体** / **相关概念**: links using `[[entities/...]]` / `[[concepts/...]]`
5. **我的判断**: human-only
6. **来源摘录**: verbatim quotes — "quote" — `[[sources/name|display]]`

## Concept Page Sections
1. **定义** 2. **关键特征** 3. **应用** 4. **生态位置** 5. **相关概念** 6. **相关实体** 7. **我的判断** 8. **来源摘录**

## Naming Conventions
- Filenames: lowercase-with-hyphens (slugified)
- Put Chinese / original names in `title` and `aliases`
- Wiki-links: `[[entities/page-name|Display Name]]` or `[[concepts/page-name|Display Name]]`

## Maintenance Policies
- Stale threshold: 90 days without updates
- Orphan page: no inbound links from other wiki pages
- Pages with `origin: claude-seed` and `reviewed: false` are unverified; prefer source facts over them and record contradictions under `## Contradictions`
