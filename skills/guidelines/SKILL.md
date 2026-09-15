---
name: guidelines
description: >-
  Use when reviewing or building Shellui website, docs, or in-shell UI.
  Fetch design.md first when composing pages. Load writing-guidelines for
  prose and web-design-guidelines for accessibility and chrome.
license: MIT
metadata:
  author: shellui
  version: '1.0.0'
---

# Shellui guidelines

Thin catalog entry for the public Shellui guidelines. Canonical long-form lives on [shellui.com/guidelines/](https://shellui.com/guidelines/). Do not scrape HTML pages.

When **building or restyling a page**, fetch design.md first:

```
https://shellui.com/design.md
```

| Topic | Skill | Fetch (agents) | Human page |
| ----- | ----- | -------------- | ---------- |
| Design (compose pages) | [`design-md`](../design-md/) | `https://shellui.com/design.md` | Visual handbook: `/guidelines/design/` (do not scrape) |
| Writing | [`writing-guidelines`](../writing-guidelines/) | `https://shellui.com/guidelines/writing.md` | `/guidelines/writing/` |
| Web design | [`web-design-guidelines`](../web-design-guidelines/) | `https://shellui.com/guidelines/web-design.md` | `/guidelines/web-design/` |

Published markdown:

```
https://shellui.com/design.md
https://shellui.com/guidelines/writing.md
https://shellui.com/guidelines/web-design.md
```

YAML `version` in each markdown file is the public "Guidelines v…" label. Logos stay on [Brand assets](https://shellui.com/brand-assets/).

Install siblings from this repo as needed:

```bash
npx skills add shellui/skills --skill guidelines
npx skills add shellui/skills --skill design-md
npx skills add shellui/skills --skill writing-guidelines
npx skills add shellui/skills --skill web-design-guidelines
```
