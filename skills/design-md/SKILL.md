---
name: design-md
description: >-
  Use when building or restyling Shellui website or in-shell pages. Fetch
  design.md first, then compose with writing-guidelines and
  web-design-guidelines. Prefer this over inventing a new visual kit.
license: MIT
metadata:
  author: shellui
  version: '1.2.0'
---

# Design.md

When creating or restyling Shellui pages, load the public design file before writing markup.

Canonical composition rules: [shellui.com/design.md](https://shellui.com/design.md). This skill is a thin wrapper. It does not replace [`writing-guidelines`](../writing-guidelines/) or [`web-design-guidelines`](../web-design-guidelines/).

The HTML page at `/guidelines/design/` is a human visual handbook (swatches, type, surfaces). Do not scrape it. Fetch `/design.md`.

## How it works

1. Fetch `https://shellui.com/design.md` (do not scrape HTML)
2. If the work includes copy, also load [`writing-guidelines`](../writing-guidelines/)
3. If the work includes UI, a11y, or iframe chrome, also load [`web-design-guidelines`](../web-design-guidelines/)
4. Prefer shipped Tailwind Plus patterns and existing Shellui layouts over new components
5. Use the shadcn-compatible tokens named in design.md

## Source

Fetch before composing:

```
https://shellui.com/design.md
```

Fallback (GitHub):

```
https://raw.githubusercontent.com/shellui/website/main/content/guidelines/design.md
```

Use WebFetch (or equivalent). The YAML `version` field is the public label (for example `v1.2.0`).

## Usage

When asked to add, restyle, or review a Shellui page:

1. Fetch and read `design.md`
2. Follow its stack, tokens, and reuse table
3. Do not add multi-color blobs, equal-weight card grids, em dashes, or a parallel token system. Soft primary/amber hero ambient is allowed when design.md permits it.
4. Pair with writing and web-design skills when copy or a11y/chrome apply
