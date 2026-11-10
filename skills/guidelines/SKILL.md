---
name: guidelines
description: >-
  Use when reviewing or building Shellui website, docs, in-shell UI, or any
  Shellui PDF, report, deck, or printed document. Fetch design.md first when
  composing pages. For print, start from the shellui skill templates and
  references/print.md. The brand kit PDF is the visual reference. Load
  writing-guidelines for prose and web-design-guidelines for accessibility
  and chrome.
license: MIT
metadata:
  author: shellui
  version: '1.1.0'
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
| Print (PDF, report, deck, one-pager) | [`shellui`](../shellui/) | [`references/print.md`](../shellui/references/print.md) and [`assets/print/`](../shellui/assets/print/). Public summary: `https://shellui.com/guidelines/print.md` | [Brand kit PDF](https://shellui.com/brand-assets/shellui-brand-kit-v1.pdf) |

Published markdown:

```
https://shellui.com/design.md
https://shellui.com/guidelines/writing.md
https://shellui.com/guidelines/web-design.md
https://shellui.com/guidelines/print.md
```

Any Shellui PDF or printed document starts from the matching template in [`assets/print/`](../shellui/assets/print/) and follows [`references/print.md`](../shellui/references/print.md). The [brand kit PDF](https://shellui.com/brand-assets/shellui-brand-kit-v1.pdf) (A4, 33 pages, v1, October 2026) is the visual reference. Where that file and the public print page disagree, follow the PDF.

YAML `version` in each markdown file is the public "Guidelines v…" label. Logos and the brand kit PDF stay on [Brand assets](https://shellui.com/brand-assets/).

Install siblings from this repo as needed:

```bash
npx skills add shellui/skills --skill guidelines
npx skills add shellui/skills --skill design-md
npx skills add shellui/skills --skill writing-guidelines
npx skills add shellui/skills --skill web-design-guidelines
```
